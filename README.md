# deps-ok

Fast checking of top level NPM and Bower dependencies based on version numbers.

[![NPM info][nodei.co]](https://npmjs.org/package/deps-ok)

[![Build status][ci-image]][ci-url]
[![dependencies][dependencies-image]][dependencies-url]
[![endorse][endorse-image]][endorse-url]

There is also [grunt-deps-ok](https://github.com/bahmutov/grunt-deps-ok) for
integrating this task into grunt pipeline.

## Use

    npm install -g deps-ok
    // from the package's root folder execute
    deps-ok
    // prints first found error and exits with code 1
    // if one of the top level dependencies
    // is missing or out of date

    deps-ok --verbose
    // prints declared and installed version numbers

Checks both dependencies listed in your *package.json* and *bower.json*

If **deps-ok** finds a problem, then run `npm install` or `bower install`

## Use as 3<sup>rd</sup> party module

You can use **deps-ok** from another module

```javascript
npm install deps-ok --save
var depsOk = require('deps-ok');
var ok = depsOk(process.cwd(), false /* verbose */);
```

## Small print

Author: Gleb Bahmutov &copy; 2013

License: MIT - do anything with the code, but don't blame me if it does not work.

Support: if you find any problems with this module, email / tweet / open issue on Github

[ci-image]: https://travis-ci.org/bahmutov/deps-ok.png?branch=master
[ci-url]: https://travis-ci.org/bahmutov/deps-ok
[nodei.co]: https://nodei.co/npm/deps-ok.png?downloads=true
[dependencies-image]: https://david-dm.org/bahmutov/deps-ok.png
[dependencies-url]: https://david-dm.org/bahmutov/deps-ok
[endorse-image]: https://api.coderwall.com/bahmutov/endorsecount.png
[endorse-url]: https://coderwall.com/bahmutov
