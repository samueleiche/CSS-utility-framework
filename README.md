# A light CSS utility-first toolkit

Inspired by [Tailwindcss](https://github.com/tailwindcss/tailwindcss).

Build layouts without writing CSS, prototype or use as a boilerplate for your applications.

## Usage Examples


### Variables

A deep map helper function `get()` ([source](https://itnext.io/advanced-use-of-sass-maps-bd5a47ca0d1a))
allows us to retrieve nested map keys easily:
```scss
$font: (
    'heading': (
        ...
        'size': (
            'h1-display': 96px,
            ...
        ),
    ),

);

.display-h1 {
    font-size: get('heading.size.h1-display', $font);
}
```


### Responsive Classes

The classes are designed for a mobile first breakpoint system, similar to  Bootstrap, Foundation, Tailwind.  

To add a utility but only have it take effect at a certain breakpoint, all you  need to do is prefix the utility with the breakpoint name,  
followed by the `:` character:
```html
<!-- .w-{1/11}/12 -->
<div class="flex flex-wrap justify-center">
    <div class="w-full md:w-6/12 lg:w-4/12"></div>
    <div class="w-full md:w-6/12 lg:w-4/12"></div>
</div>

<!-- .w-{1/4}/5 -->
<div class="flex">
    <div class="w-2/5"></div>
    <div class="w-3/5"></div>
</div>
```
**This does not work for every utility class in the framework**
You can add or extend your own responsive class groups -  
see [Extending responsive classes](#extending-responsive-classes)


### Included Components

Images with ratios:
```html
<figure class="image image-1x1 lg:image-16x9">
    <img src="..." alt="...">
</figure>
```

Buttons:
```html
<button type="button" class="btn btn-icon-left btn-primary">
    <i class="fa fa-pencil"></i>
    Iconed
</button>

<a href="#" class="btn btn-primary btn-outlined">
    Outlined
</a>
```


### Typography

Basic text utilities:
```html
<article>
    <header>
        <h2 class="text-black font-bold text-4xl md:text-6xl">...</h2>
        <p class="text-black font-semibold uppercase italic">...</p>
    </header>

    <p>...</p>

    <footer class="text-xs border-t">
        ...
    </footer>
</article>
```

### Extending Responsive Classes

1. Create a mixin which accepts an argument `$prefix` and add it in your new classes you want to make responsive:
```scss
// e.g. _visibility.scss

@mixin responsive-visibility($prefix) {
    .#{$prefix}invisible {
        visibility: visible;
    }
}
```

2. Add the created mixin to the `responsive-factory` mixin in `index.scss` 
```scss
// index.scss

@mixin responsive-factory($prefix: '') {
    // ...
    @include responsive-visibility($prefix);
}

// Result:
//
// .invisible
// .sm:invisible
// .md:invisible
// .lg:invisible
// .xl:invisible
```