<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Boolean

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Boolean][mdn-boolean] constructor.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/boolean-ctor
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var Boolean = require( '@stdlib/boolean-ctor' );
```

#### Boolean( value )

Returns a `Boolean` object, which is an object wrapper for a primitive boolean value.

<!-- eslint-disable no-new-wrappers -->

```javascript
var b = new Boolean( null );
// returns <Boolean>
```

When invoked without `new`, the function converts an input value to a primitive boolean value.

```javascript
var b = Boolean( null );
// returns false
```

* * *

### Methods

<a name="method-to-string"></a>

##### Boolean.prototype.toString()

Returns a string representation of the boolean value.

```javascript
var b = new Boolean( true );
var str = b.toString();
// returns 'true'
```

##### Boolean.prototype.valueOf()

Returns the primitive value of the boolean object.

```javascript
var b = new Boolean( true );
var val = b.valueOf();
// returns true

b = new Boolean();
val = b.valueOf();
// returns false
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   When invoked without `new`,

    -   if provided `false`, `null`, `undefined`, `-0`, `0`, `NaN`, or an empty string, the function returns `false`.
    -   if provided any other value, including an empty object, an empty array, the string `'false'`, or a `Boolean` object (including a `Boolean` object whose value is `false`), the function returns `true`.

-   When invoked with `new`, the value of the returned `Boolean` object adheres to the same conversion semantics as when the constructor is invoked without `new`.

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

<!-- eslint-disable new-cap -->

```javascript
var format = require( '@stdlib/string-format' );
var Bool = require( '@stdlib/boolean-ctor' );

var values = [
    '5',
    5,
    0,
    NaN,
    true,
    false,
    null,
    void 0,
    [],
    {}
];

var i;
for ( i = 0; i < values.length; i++ ) {
    console.log( format( '%s => %s', JSON.stringify( values[ i ] ), ( Bool( values[ i ] ) ) ? 'true' : 'false' ) );
}
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

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

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/boolean-ctor.svg
[npm-url]: https://npmjs.org/package/@stdlib/boolean-ctor

[test-image]: https://github.com/stdlib-js/boolean-ctor/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/boolean-ctor/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/boolean-ctor/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/boolean-ctor?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/boolean-ctor.svg
[dependencies-url]: https://david-dm.org/stdlib-js/boolean-ctor/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/boolean-ctor/tree/deno
[deno-readme]: https://github.com/stdlib-js/boolean-ctor/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/boolean-ctor/tree/umd
[umd-readme]: https://github.com/stdlib-js/boolean-ctor/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/boolean-ctor/tree/esm
[esm-readme]: https://github.com/stdlib-js/boolean-ctor/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/boolean-ctor/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/boolean-ctor/main/LICENSE

[mdn-boolean]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean

</section>

<!-- /.links -->
