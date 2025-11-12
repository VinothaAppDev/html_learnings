<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# picture tag

The HTML `<picture>` tag is used to provide multiple sources for an image, enabling you to serve different images depending on device characteristics such as screen width, resolution, or format support. It enhances responsive images by allowing art direction and different image versions for different situations.

### How the `<picture>` tag works:

```
- You put multiple `<source>` elements inside the `<picture>`.
```

- Each `<source>` specifies a media query (like CSS media queries) and a `srcset` for that condition.
- The browser evaluates the sources in order, picks the first matching `<source>` based on media conditions, and loads that image.

```
- There is a fallback `<img>` tag inside the `<picture>` that provides the default image if no `<source>` matches or for browsers that don't support `<picture>`.
```


### Basic `<picture>` structure example:

```html
<picture>
  <source media="(min-width: 800px)" srcset="large.jpg">
  <source media="(min-width: 400px)" srcset="medium.jpg">
  <img src="small.jpg" alt="Description of image">
</picture>
```

- If viewport width is 800px or wider, `large.jpg` loads.
- If viewport width is between 400px and 799px, `medium.jpg` loads.
- Otherwise, `small.jpg` loads.


### Benefits of `<picture>`:

- Art direction: Serve entirely different images for different screen sizes or contexts instead of just resizing.
- Format switching: Serve WebP or AVIF formats when supported, with fallback to JPEG/PNG.
- Fine-tuned responsive images beyond what `srcset` and `sizes` alone offer.


### When to use:

- You want to change cropping or composition for different screen sizes.
- You need to provide alternative formats for optimization.
- You want greater control over which image is loaded under which conditions.


### Reference:

The `<picture>` tag is part of responsive image techniques, complementing `srcset` and `sizes` but offering more flexible source selection based on media conditions.