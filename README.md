
# simple-duration

[![npm version](https://img.shields.io/npm/v/simple-duration-converter.svg)](https://www.npmjs.com/package/simple-duration-converter)

A JavaScript library to convert seconds to strings and back using a human readable format.

An updated version of https://github.com/nicolas-van/simple-duration

Examples:

```javascript
const sd = require('simple-duration');

const i = sd.parse('3h 10m 52s') // i = 11452

console.log(sd.stringify(i + 10)) // prints 3h 11m 2s
```

## Installation

```
npm install simple-duration-converter
```

## Usage

### `parse(str)`

Parses a string using the Simple Duration Format and returns the number of seconds corresponding to it.

### `stringify(seconds, rounding='ms')`

Formats a number of seconds. The rounding is using the milliseconds as default value but you can pass any
other unit as defined bellow.

## Format

Here are the possible units:

* **y** - A Julian year, which means 365.25 days.
* **w** - 7 days.
* **d** - 24 hours.
* **h** - 60 minutes.
* **m** - 60 seconds.
* **s** - A second according to the SI.
* **ms** - 10e-3 seconds.
* **µs** - 10e-6 seconds.
* **ns** - 10e-9 seconds.

You can specify any number of units in any order. As example `24s 3h` is perfectly valid. You can also specify
negative amounts of time like `-3m`.

When formatting the `stringify` function will always use a normalizing process.

## License

[See the license file](./LICENSE.md).