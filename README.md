# @taktikorg/earum-id-asperiores <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Set a function’s name.

Arguments:
 - `fn`: the function
 - `name`: the new name
 - `loose`: Optional. If true, and the name fails to be set, do not throw. Default false.

Returns `fn`.

## Usage

```javascript
var setFunctionName = require('@taktikorg/earum-id-asperiores');
var assert = require('assert');

const obj = {
    concise() {},
    arrow: () => {},
    named: function named() {},
    anon: function () {},
};
assert.equal(obj.concise.name, 'concise');
assert.equal(obj.arrow.name, 'arrow');
assert.equal(obj.named.name, 'named');
assert.equal(obj.anon.name, 'anon');

assert.equal(setFunctionName(obj.concise, 'brief'), obj.concise);
assert.equal(setFunctionName(obj.arrow, 'pointy'), obj.arrow);
assert.equal(setFunctionName(obj.named, ''), obj.named);
assert.equal(setFunctionName(obj.anon, 'anonymous'), obj.anon);

assert.equal(obj.concise.name, 'brief');
assert.equal(obj.arrow.name, 'pointy');
assert.equal(obj.named.name, '');
assert.equal(obj.anon.name, 'anonymous');
```

[package-url]: https://npmjs.org/package/@taktikorg/earum-id-asperiores
[npm-version-svg]: https://versionbadg.es/ljharb/@taktikorg/earum-id-asperiores.svg
[deps-svg]: https://david-dm.org/ljharb/@taktikorg/earum-id-asperiores.svg
[deps-url]: https://david-dm.org/ljharb/@taktikorg/earum-id-asperiores
[dev-deps-svg]: https://david-dm.org/ljharb/@taktikorg/earum-id-asperiores/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@taktikorg/earum-id-asperiores#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@taktikorg/earum-id-asperiores.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@taktikorg/earum-id-asperiores.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@taktikorg/earum-id-asperiores.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@taktikorg/earum-id-asperiores
[codecov-image]: https://codecov.io/gh/ljharb/@taktikorg/earum-id-asperiores/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@taktikorg/earum-id-asperiores/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@taktikorg/earum-id-asperiores
[actions-url]: https://github.com/taktikorg/earum-id-asperiores/actions
