# sass-module-math

[![Release Version](https://img.shields.io/npm/v/sass-module-math.svg)](https://www.npmjs.com/package/sass-module-math)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

This Sass module provides more advanced math functions.

## Install

### Requires

Install the package:

```bash
npm install sass-module-math
```

Use the package like any other Sass module:

```scss
@use 'sass-module-math';
```

Depending on your setup, you may need to configure `node_modules` as include path:

```js
const sass = require('sass');

sass.render({
  file: scss_filename,
  includePaths: ['node_modules']
});
```

## Public API

### Bounding Functions

<dl>

  <dt><a href="//github.com/roydukkey/sass-module-math/tree/master/src/math/_gcd.sass"><code>gcd ( $numbers... )</code></a></dt>
  <dd>Returns the Greatest Common Divisor (GCD, GCF, HCF) of a set of numbers.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-math/tree/master/src/math/_lcm.sass"><code>lcm ( $numbers... )</code></a></dt>
  <dd>Returns the Least Common Multiple (LCM) of a set of numbers.</dd>

</dl>

### Exponential Functions

<dl>

  <dt><a href="//github.com/roydukkey/sass-module-math/tree/master/src/math/_exp.sass"><code>exp ( $number )</code></a></dt>
  <dd>Returns Euler's number to the specified power.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-math/tree/master/src/math/_fact.sass"><code>fact ( $number )</code></a></dt>
  <dd>Returns the factorial of the specified integer.</dd>

</dl>

### Unit Functions

<dl>

  <dt><a href="//github.com/roydukkey/sass-module-math/tree/master/src/math/_change.sass"><code>change ( $number, $units )</code></a></dt>
  <dd>Returns the given number with the same units as another specified number.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-math/tree/master/src/math/_unitless.sass"><code>unitless ( $number )</code></a></dt>
  <dd>Returns the unitless value of the specified number.</dd>

</dl>

Don't see the function you're looking for? Request a [new feature](//github.com/roydukkey/sass-module-math/issues/new) describing a use case.

## Combined API

In order to avoid constantly declaring both the native 'sass:math' module and this library, the combined API has been added which merges the two.

```scss
// Rather than using both modules separately...
@use 'sass-module-math';
@use 'sass:math';

// ...this statement will accomplish the same thing.
@use 'sass-module-math/math';
```
