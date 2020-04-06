# tiny-version-compare [![Build Status](https://travis-ci.org/fregante/tiny-version-compare.svg?branch=master)](https://travis-ci.org/fregante/tiny-version-compare)

> Compare two software versions, with any number of points (<1KB)

Supports most version types, from `r12.3` to `1.03.4.234567-RC4`. Development versions are sorted as: `dev`, `alpha`, `beta`, `rc`

Also [used by Refined GitHub](https://github.com/sindresorhus/refined-github/pull/1218).

## Install

```
$ npm install tiny-version-compare
```


## Usage

```js
import versionCompare from 'tiny-version-compare';

switch (versionCompare('1.2.3', '2.3.4')) {
	case -1: console.log('Second one is greater'); break
	case 1:  console.log('Second one is lower'); break
	case 0:  console.log('Versions are equal'); break
}

['v2.0-beta', '1.0', 'v2.0', '1.0.1'].sort(versionCompare);
// ['1.0', '1.0.1', 'v2.0-beta', 'v2.0']
```


## API
### versionCompare(versionA, versionB)

Returns `-1` if `versionA` is greater, `1` if `versionB` is greater, `0` if the versions are equivalent.

#### versionA, versionB

Type: `string`

The versions to compare.

## License

MIT © [Federico Brigante](https://bfred.it)

