# Lightweight CSS utility-first framework
## Boilerplate

`_typography.scss`, `_theme.scss`, `_utility.scss` and `_base.scss` are fully customizable
for the projects needs with a few pre made classes to help get started.

## Framework
Every class includes a breakpoint abbreviation, from `sm` to `xl`. Classes without an abbrevation are
applied from `min-width: 0` and are not bound by media queries.

### Containers

```css
.container {
    /* ... */
}
.container-half {
    /* ... */
}
```

### Layout
The grid includes the following helpful classes to build layouts

```css
.hidden {
    display: none !important;
}

.block {
    display: block !important;
}

.inline-block {
    display: inline-block !important;
}

.full-height {
    height: 100% !important;
}

.full-width {
    width: 100% !important;
}

.auto-height {
    height: auto !important;
}

.auto-width {
    width: auto !important;
}

.relative {
    position: relative !important;
}

.absolute {
    position: absolute !important;
}
```

Flex classes require the elements `display` to be `flex`, you can do so by adding
the class `.flex` to allow the use of the flex utilities.

A list of all flex utilites:
```
.flex

.flex-auto
.flex-equal
.flex-order-first
.flex-order-last
.flex-*
.flex-order-*
.flex-offset-*

.flex-column
.flex-row

.flex-top
.flex-bottom
.flex-right
.flex-left

.space-between
.flex-y-center
.flex-x-center
.flex-center

.flex-wrap
.flex-nowrap

.flex-shrink
.flex-noshrink
.flex-grow
.flex-nogrow
.flex-self-start
.flex-self-end
.flex-self-center
```

Text alignment is also supported:

```
.align-center
.align-left
.align-right
```


### Spacing
The classes are named using the format {property}{sides}-{size} for xs
and {property}{sides}-{breakpoint}-{size} for sm, md, lg, and xl.

* Property stands for

    **m** - margin

    **p** - padding

* Sides stands for

    **t** - top

    **b** - bottom

    **l** - left

    **r** - right

    **x** - left and right

    **y** - top and bottom

    **blank** - all sides

* Size stands for

    **0** - 0

    **1** - 1rem * .25

    **2** - 1rem * .5

    **3** - 1rem

    **4** - 1rem * 1.5

    **5** - 1rem * 3

    **6** - 1rem * 6

    **7** - 1rem * 12

    **auto** - applies auto margin to 'mx', 'ml' or 'mr'

    **n** - negative margin for every non-zero integer e.g. `.mt-n5`

**Example**

`<div class="my-3 mx-2 mx-md-4 my-md-5"></div>`

A list of all spacing utilites:
```
.mx-auto
.ml-auto
.mr-auto

.m-*

.mt-*
.mr-*
.mb-*
.ml-*

.mt-n*
.mr-n*
.mb-n*
.ml-n*

.mx-*
.my-*

.p-*

.pt-*
.pr-*
.pb-*
.pl-*

.px-*
.py-*
```
