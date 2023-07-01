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

# Variance

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Exponential][exponential-distribution] distribution [variance][variance].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [variance][variance] for an [exponential][exponential-distribution] random variable is

<!-- <equation class="equation" label="eq:exponential_variance" align="center" raw="\operatorname{Var}\left( X \right) = \lambda^{-2}" alt="Variance for an exponential distribution."> -->

```math
\operatorname{Var}\left( X \right) = \lambda^{-2}
```

<!-- <div class="equation" align="center" data-raw-text="\operatorname{Var}\left( X \right) = \lambda^{-2}" data-equation="eq:exponential_variance">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@51534079fef45e990850102147e8945fb023d1d0/lib/node_modules/@stdlib/stats/base/dists/exponential/variance/docs/img/equation_exponential_variance.svg" alt="Variance for an exponential distribution.">
    <br>
</div> -->

<!-- </equation> -->

where `λ` is the rate parameter.

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

To use in Observable,

```javascript
variance = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-exponential-variance@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var variance = require( 'path/to/vendor/umd/stats-base-dists-exponential-variance/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-exponential-variance@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.variance;
})();
</script>
```

#### variance( lambda )

Returns the [variance][variance] of a [exponential][exponential-distribution] distribution with rate parameter `lambda`.

```javascript
var v = variance( 9.0 );
// returns ~0.012

v = variance( 0.5 );
// returns 4.0
```

If provided `lambda < 0`, the function returns `NaN`.

```javascript
var v = variance( -1.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-round@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-exponential-variance@umd/browser.js"></script>
<script type="text/javascript">
(function () {

var lambda;
var v;
var i;

for ( i = 0; i < 10; i++ ) {
    lambda = randu() * 20.0;
    v = variance( lambda );
    console.log( 'λ: %d, Var(X;λ): %d', lambda.toFixed( 4 ), v.toFixed( 4 ) );
}

})();
</script>
</body>
</html>
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

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-exponential-variance.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-exponential-variance

[test-image]: https://github.com/stdlib-js/stats-base-dists-exponential-variance/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/stats-base-dists-exponential-variance/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-exponential-variance/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-exponential-variance?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-exponential-variance.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-exponential-variance/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-exponential-variance/tree/deno
[umd-url]: https://github.com/stdlib-js/stats-base-dists-exponential-variance/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-base-dists-exponential-variance/tree/esm
[branches-url]: https://github.com/stdlib-js/stats-base-dists-exponential-variance/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-exponential-variance/main/LICENSE

[exponential-distribution]: https://en.wikipedia.org/wiki/Exponential_distribution

[variance]: https://en.wikipedia.org/wiki/Variance

</section>

<!-- /.links -->
