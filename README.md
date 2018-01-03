# postcss-color-hex-hsl [![CSS Standard Status](https://jonathantneal.github.io/css-db/badge/css-color-hex-notation.svg)](https://jonathantneal.github.io/css-db/#css-color-hex-notation) [![Build Status](https://travis-ci.org/DavidBrockmeier/postcss-color-hex-hsl.png)](https://travis-ci.org/DavidBrockmeier/postcss-color-hex-hsl)

> [PostCSS](https://github.com/postcss/postcss) plugin to transform [W3C RGBA hexadecimal notations (#RRGGBBAA or #RGBA)](http://dev.w3.org/csswg/css-color/#hex-notation) to more compatible CSS (rgba()).

## Installation

```bash
$ npm install postcss-color-hex-hsl
```

## Usage

```js
// dependencies
var fs = require("fs")
var postcss = require("postcss")
var colorHexAlpha = require("postcss-color-hex-hsl")

// css to be processed
var css = fs.readFileSync("input.css", "utf8")

// process css
var output = postcss()
  .use(colorHexAlpha())
  .process(css)
  .css
```

Using this `input.css`:

```css
body {
  background: #9d9c
}

```

you will get:

```css
body {
  background: rgba(153, 221, 153, 0.8)
}
```

Checkout [tests](test) for more examples.

---

## Contributing

Work on a branch, install dev-dependencies, respect coding style & run tests before submitting a bug fix or a feature.

    $ git clone https://github.com/DavidBrockmeier/postcss-color-hex-hsl.git
    $ git checkout -b patch-1
    $ npm install
    $ npm test

## [Changelog](CHANGELOG.md)

## [License](LICENSE)
