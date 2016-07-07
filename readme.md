# Griss

Simple and modular grid system.

## Overview

*Griss* is a simple grid system built with modularity in mind to avoid
unnecessary bloat and help you develop with ease.

Key features:

- Fluid cells.
- Fixed gutters.
- Infinite nesting.
- Lightweight (~180 bytes minified and gzipped).
- Extensible using the different [available modules](#available-modules) or
  your own code.

## Installation

Install it using [npm](https://npmjs.com):

```sh
npm install griss
```

Or simply [download the minified file](dist/griss.min.css) and include it into
your project:

```html
<link href="griss.min.css" rel="stylesheet" />
```

## Usage

To create either a grid or a cell use whichever element makes sense for your
content, it could be a `div`, `span`, `ul`, `ol`, `li`, even `aside`, `article`
or `main`. If it makes sense, it will —*most certainly*— work just fine.

To define a grid use the base grid class —`Grid`— and as many cells as you
need using the base cell class —`Grid-cell`. *Grids can only have cells as
direct children.*

Cells by default are as wide as the grid. To define a different size combine
the base cell class with your own selector, or use the
[cells module](https://github.com/battaglr/griss-cells).

Gutters by default have a size of `10px` on each side of a cell, with the
exception of the first and last one which are compensated automatically so each
cell lines up with the content outside of the grid. To define a different size
combine the base grid class with your own selector or use the
[gutters module](https://github.com/battaglr/griss-gutters).

*To avoid horizontal scrolling, always compensate the gutter size of the grid
by applying `padding` to its parent element or by setting the `overflow` as
`hidden`.*

#### Examples

Some basic examples:

- A grid with two cells using `div`:

  ```html
  <div class="Grid">
    <div class="Grid-cell / Example-size(1/2)"> ... </div>
    <div class="Grid-cell / Example-size(1/2)"> ... </div>
  </div>
  ```

- A grid with three cells using `ul` and `li`:

  ```html
  <ul class="Grid">
    <li class="Grid-cell / Example-size(1/3)"> ... </li>
    <li class="Grid-cell / Example-size(1/3)"> ... </li>
    <li class="Grid-cell / Example-size(1/3)"> ... </li>
  </ul>
  ```

- A grid with two cells using `div` and a nested grid with two cells
  using `span`:

  ```html
  <div class="Grid">
    <div class="Grid-cell / Example-size(1/2)"> ... </div>
    <div class="Grid-cell / Example-size(1/2)">
      ...
      <span class="Grid">
        <span class="Grid-cell / Example-size(1/2)"> ... </span>
        <span class="Grid-cell / Example-size(1/2)"> ... </span>
      </span>
    </div>
  </div>
  ```

- Defining your own selectors:

  ```css
  .Example-size(1/2) {
    width: 50%;
  }

  .Example-size(1/3) {
    width: 33.33333%;
  }
  ```

  *To facilitate readability the CSS escape character is not included.*

For more examples, please check out the
[test page](https://battaglr.github.io/griss/test/test.html).

#### Available classes

- `Grid`
- `Grid-cell`

## Browser support

The following browsers are supported:

- Chrome *latest 5*
- Firefox *latest 5*
- Internet Explorer *8+*
- Edge *latest 5*
- Opera *latest 5*
- Safari *latest 5*
- iOS Safari *latest 5*
- Android Browser *2.1+*

## Available modules

- [Core](https://github.com/battaglr/griss)
- [Cells](https://github.com/battaglr/griss-cells)
- [Gutters](https://github.com/battaglr/griss-gutters)
- *More coming soon…*

## Contributing

Contributions are welcome! Please, read the
[contribution guidelines](contributing.md) first.

## License

Released under the [MIT license](license.txt).
