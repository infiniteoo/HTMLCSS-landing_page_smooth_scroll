# HTML&CSS - Landing Page w/Smooth Scrolling Effect

### About

This project covers 3 simple ways to implement smooth scrolling effects for your web project:

- Basic CSS
- jQuery
- Smooth-Scroll (3rd party plugin)

![example_gif](./example.gif)

## Ways to Implement

#### Option 1: CSS

on .container:

```
  overflow-y: scroll;
  scroll-behavior: smooth;
  scroll-snap-type: y mandatory;

```

on section:

```

scroll-snap-align: center;

```

#### Option 2: jQuery

```

$(".navbar a").on("click", function (e) {
  if (this.hash !== "") {
    e.preventDefault();

    const hash = this.hash;

    $("html, body").animate(
      {
        scrollTop: $(hash).offset().top,
      },
      800
    );
  }
});

```

#### Option 3: Smooth-Scroll

after linking to the smooth-scroll CDN all you need in your JS is:

```
const scroll = new SmoothScroll('.navbar a[href*="#"]', {
  speed: 800,
});


```

### Acknowledgement

Thanks to Traversy Media on YouTube for another amazing tutorial.
