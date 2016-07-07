# Griss gutters

Gutters module for [Griss](https://github.com/battaglr/griss/).

## Overview

Extends [Griss](https://github.com/battaglr/griss/) by adding a set of grid
classes to modify the default gutter with three available breakpoints to adjust
the size at different screen widths.

Key features:

- Responsive and mobile-first.
- Lightweight (~277 bytes minified and gzipped).
- Extensible using the different
  [available modules](https://github.com/battaglr/griss/#available-modules)
  or your own code.

## Installation

Install it using [npm](https://npmjs.com):

```sh
npm install griss-gutters
```

Or simply [download the minified file](dist/griss-gutters.min.css) and include
it into your project:

```html
<link href="griss-gutters.min.css" rel="stylesheet" />
```

*You will also need to install
[Griss core module](https://github.com/battaglr/griss/#installation).*

## Usage

*Make sure you have read
[Griss core documentation](https://github.com/battaglr/griss/#usage) first.*

Combine the base grid class —`Grid`— with the class that defines the gutter
size that you need for your content —i.e. `Grid--gutter(s)`.

To define the gutter size of each grid you can choose from five different
options:

- *None* represented as `n` for no gutter.
- *Small* represented as `s` for a gutter of `5px`.
- *Medium* represented as `m` for a gutter of `10px`.
- *Large* represented as `l` for a gutter of `15px`.
- *Extra large* represented as `xl` for a gutter of `20px`.

Using only the base grid class the default gutter will be of `10px`.

If you need to make adjustments at different screen widths use any of the
available breakpoint suffixes: `@s`, `@m` and `@l` —i.e. `Grid--gutter(s)@m`.

*To avoid horizontal scrolling, always compensate the gutter size of the grid
by applying `padding` to its parent element or by setting the `overflow` as
`hidden`.*

#### Examples

Some basic examples:

- A grid with no gutter:

  ```html
  <div class="Grid Grid--gutter(n)">
    <div class="Grid-cell"> ... </div>
    <div class="Grid-cell"> ... </div>
  </div>
  ```

- A grid using different gutter sizes at different breakpoints:

  ```html
  <div class="Grid Grid--gutter(s)@s Grid--gutter(m)@l">
    <div class="Grid-cell"> ... </div>
    <div class="Grid-cell"> ... </div>
  </div>
  ```

- A grid and a nested grid using different gutter sizes:

  ```html
  <div class="Grid Grid--gutter(m)">
    <div class="Grid-cell"> ... </div>
    <div class="Grid-cell">
      ...
      <div class="Grid Grid--gutter(l)">
        <div class="Grid-cell"> ... </div>
        <div class="Grid-cell"> ... </div>
      </div>
    </div>
  </div>
  ```

For more examples, please check out the
[test page](https://battaglr.github.io/griss-gutters/test/test.html).

#### Available classes

##### Base

- `Grid--gutter(n)`
- `Grid--gutter(s)`
- `Grid--gutter(m)`
- `Grid--gutter(l)`
- `Grid--gutter(xl)`

##### Breakpoints

- `Grid--gutter(sz)@s`
- `Grid--gutter(sz)@m`
- `Grid--gutter(sz)@l`

*`sz` should be replaced with an available size.*

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

*IE8 does not support media queries.*

## Contributing

Contributions are welcome! Please, read the
[contribution guidelines](contributing.md) first.

## License

Released under the [MIT license](license.txt).
