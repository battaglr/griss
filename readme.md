# Griss

Simple and modular grid system.

## Overview

*Griss* is a simple grid system built with modularity in mind to help you
develop with ease and avoid unnecessary bloat.

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

Use whichever element you need: `div`, `span`, `ul`, `ol`, `li`, even `aside`,
`article` or `main`. If the chosen element makes sense for your content it will
—most certainly— work just fine.

By default cells are as wide as its container and have a gutter of `10px`.

To define the size of each cell combine the base cell class —`Grid-cell`— with
your own selector —i.e. `Example-size(1/2)`.

*It’s very important to keep in mind that grids can only have cells as
direct children.*

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

- [Core](https://github.com/battaglr/griss) | 180 bytes
- Cells (*WIP*)
- Gutters (*WIP*)
- *More…*

*Size values are based on the minified and gzipped version.*

## Contributing

Contributions are welcome! Please, read the
[contribution guidelines](contributing.md) first.

## License

Released under the [MIT license](license.txt).
