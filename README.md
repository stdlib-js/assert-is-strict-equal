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

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Test if two arguments are strictly equal.



<section class="usage">

## Usage

To use in Observable,

```javascript
isStrictEqual = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/assert-is-strict-equal@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var isStrictEqual = require( 'path/to/vendor/umd/assert-is-strict-equal/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/assert-is-strict-equal@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.isStrictEqual;
})();
</script>
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

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/assert-is-strict-equal@umd/browser.js"></script>
<script type="text/javascript">
(function () {

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

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/assert-is-same-value`][@stdlib/assert/is-same-value]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/assert-is-strict-equal.svg
[npm-url]: https://npmjs.org/package/@stdlib/assert-is-strict-equal

[test-image]: https://github.com/stdlib-js/assert-is-strict-equal/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/assert-is-strict-equal/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/assert-is-strict-equal/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/assert-is-strict-equal?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/assert-is-strict-equal.svg
[dependencies-url]: https://david-dm.org/stdlib-js/assert-is-strict-equal/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/assert-is-strict-equal/tree/deno
[umd-url]: https://github.com/stdlib-js/assert-is-strict-equal/tree/umd
[esm-url]: https://github.com/stdlib-js/assert-is-strict-equal/tree/esm
[branches-url]: https://github.com/stdlib-js/assert-is-strict-equal/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/assert-is-strict-equal/main/LICENSE

<!-- <related-links> -->

[@stdlib/assert/is-same-value]: https://github.com/stdlib-js/assert-is-same-value/tree/umd

<!-- </related-links> -->

</section>

<!-- /.links -->
