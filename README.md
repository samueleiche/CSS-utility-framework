# CSS-grid
Css grid based on bootstrap 4 grid system and BEM

## Basic class names

`.container`
`.grid`
`.grid__col-md, .grid__col-sm-6`
`.grid__col-sm-order-6`
`.grid__col-sm-offset-6`

`.grid--no-gutter`
`.hide, .invisible-sm`
`.show-lg, .visible`

## Demo

```html
  <div class="container container--extended">
    <div class="grid grid--no-gutter">
      <div class="grid__col-equal"></div>
      <div class="grid__col-equal"></div>
      <div class="grid__col-equal-break hide-md"></div>
      <div class="grid__col-equal"></div>
      <div class="grid__col-equal"></div>
    </div>

    <div class="grid">
      <div class="grid__col-4  grid__col-offset-4 grid__col-md-6 grid__col-md-offset-3"></div>
    </div>
  </div>
```
