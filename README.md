<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# isStrictEqual

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> Test if two arguments are strictly equal.

<section class="installation">

## Installation

```bash
npm install @stdlib/assert-is-strict-equal
```

</section>

<section class="usage">

## Usage

```javascript
var isStrictEqual = require( '@stdlib/assert-is-strict-equal' );
```

#### isStrictEqual( a, b )

Tests if two arguments `a` and `b` are strictly equal.

```javascript
var bool = isStrictEqual( false, false );
// returns true

bool = isStrictEqual( '', '' );
// returns true

bool = isStrictEqual( {}, {} );
// returns false

bool = isStrictEqual( NaN, NaN );
// returns false
```

In contrast to the strict equality operator `===`, the function distinguishes between `+0` and `-0`.

<!-- eslint-disable no-compare-neg-zero -->

```javascript
var bool = ( 0.0 === -0.0 );
// returns true

bool = isStrictEqual( 0.0, -0.0 );
// returns false

bool = isStrictEqual( -0.0, -0.0 );
// returns true
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var isStrictEqual = require( '@stdlib/assert-is-strict-equal' );

var bool = isStrictEqual( true, true );
// returns true

bool = isStrictEqual( true, false );
// returns false

bool = isStrictEqual( 'beep', 'beep' );
// returns true

bool = isStrictEqual( 3.14, 3.14 );
// returns true

bool = isStrictEqual( null, null );
// returns true

bool = isStrictEqual( 0.0, 0.0 );
// returns true

bool = isStrictEqual( -0.0, 0.0 );
// returns false

bool = isStrictEqual( NaN, NaN );
// returns false

bool = isStrictEqual( {}, {} );
// returns false

bool = isStrictEqual( [], [] );
// returns false

bool = isStrictEqual( isStrictEqual, isStrictEqual );
// returns true
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/assert-is-strict-equal.svg
[npm-url]: https://npmjs.org/package/@stdlib/assert-is-strict-equal

[test-image]: https://github.com/stdlib-js/assert-is-strict-equal/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/assert-is-strict-equal/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/assert-is-strict-equal/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/assert-is-strict-equal?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/assert-is-strict-equal
[dependencies-url]: https://david-dm.org/stdlib-js/assert-is-strict-equal/main

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/assert-is-strict-equal/main/LICENSE

</section>

<!-- /.links -->