# forge-es

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A ES module native implementation of [TLS][] (and various other cryptographic tools) in [JavaScript][].

Forked from [Forge](https://github.com/digitalbazaar/forge).

Converted only AES-GCM ([utility](https://github.com/taisukef/AES-GCM-es)).

## Introduction

The Forge software is a fully native implementation of the [TLS][] protocol in JavaScript, a set of cryptography utilities, and a set of tools for developing Web Apps that utilize many network resources.

## Performance

Forge is fast. Benchmarks against other popular JavaScript cryptography libraries can be found here:

* http://dominictarr.github.io/crypto-bench/
* http://cryptojs.altervista.org/test/simulate-threading-speed_test.html

## Installation

**Note**: Please see the [Security Considerations](#security-considerations) section before using packaging systems and pre-built files.

Forge uses a [CommonJS][] module structure with a build process for browser bundles. The older [0.6.x][] branch with standalone files is available but will not be regularly updated.

### Node.js

If you want to use forge with [Node.js][], it is available through `npm`:

https://npmjs.org/package/node-forge

Installation:

    npm install node-forge

You can then use forge as a regular module:

```js
var forge = require('node-forge');
```

The npm package includes pre-built `forge.min.js`, `forge.all.min.js`, and `prime.worker.min.js` using the [UMD][] format.

### Bundle / Bower

Each release is published in a separate repository as pre-built and minimized basic forge bundles using the [UMD][] format.

https://github.com/digitalbazaar/forge-dist

This bundle can be used in many environments. In particular it can be installed with [Bower][]:

    bower install forge

### jsDelivr CDN

To use it via [jsDelivr](https://www.jsdelivr.com/package/npm/node-forge) include this in your html:

```html
<script src="https://cdn.jsdelivr.net/npm/node-forge@0.7.0/dist/forge.min.js"></script>
```

### unpkg CDN

To use it via [unpkg](https://unpkg.com/#/) include this in your html:

```html
<script src="https://unpkg.com/node-forge@0.7.0/dist/forge.min.js"></script>
```

## Testing

### Prepare to run tests

    npm install

### Running automated tests with Node.js

Forge natively runs in a [Node.js][] environment:

    npm test

### Running automated tests with Headless Chrome

Automated testing is done via [Karma][]. By default it will run the tests with Headless Chrome.

    npm run test-karma

## Contributing

Any contributions (eg: PRs) that are accepted will be brought under the same license used by the rest of the Forge project. This license allows Forge to be used under the terms of either the BSD License or the GNU General Public License (GPL) Version 2.

See: [LICENSE](https://github.com/digitalbazaar/forge/blob/cbebca3780658703d925b61b2caffb1d263a6c1d/LICENSE)

If a contribution contains 3rd party source code with its own license, it may retain it, so long as that license is compatible with the Forge license.

[TLS]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[JavaScript]: https://www.javascript.com/
[CommonJS]: http://wiki.commonjs.org/wiki/CommonJS
[0.6.x]: https://github.com/digitalbazaar/forge/tree/0.6.x
[Node.js]: https://nodejs.org/
[UMD]: https://github.com/umdjs/umd
[Bower]: http://bower.io/
[webpack]: https://webpack.js.org/
[Browserify]: http://browserify.org/
[Karma]: https://karma-runner.github.io/