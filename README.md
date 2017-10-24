karma-chai-json-schema
================

Based on [karma-chai-things](https://github.com/solatis/karma-chai-things)
as recommended in https://github.com/chaijs/chai-json-schema/issues/35

  * [Chai](http://chaijs.com)
  * [chai-json-schema](http://chaijs.com/plugins/chai-json-schema)

for [Karma](http://karma-runner.github.io)

Known issues
------------

**This plugin is in development. Definitely not for production.**

In testing I get this error:

```sh
AssertionError: tv4 dependency: expected undefined to be truthy
  at http://localhost:8080/_karma_node_modules/chai/chai.js:9320
PhantomJS 2.1.1 (Mac OS X 0.0.0): Executed 0 of 0 ERROR (0.12 secs / 0 secs)
```

I have gotten as far as I can take it at the moment.
Any help appreciated :)


Requirements
------------

This Karma plugin requires Karma `~1.0` or higher.

Installation
------------

Install the module via npm

```sh
$ npm install --save-dev karma-chai-json-schema
```

Add `chai-json-schema` to the `frameworks` key in your Karma configuration:

```js
module.exports = function(config) {
  'use strict';
  config.set({
    frameworks: ['mocha', 'chai-json-schema', 'chai'],
    #...
  });
}
```

Keep in mind that, since Karma loads its frameworks in reverse and `chai-json-schema` depends on `chai`, you should declare it accordingly as done above.


AMD/RequireJS support
------------

Like karma-chai-things from which it’s forked, karma-chai-json-schema currently does not support AMD/RequireJS.
And, like [solatis](https://github.com/solatis), this is mainly because I can’t figure out how this dependency should be injected.

Please feel free to make it work!