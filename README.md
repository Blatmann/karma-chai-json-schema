karma-chai-json-schema
================

Based on [karma-chai-things](https://github.com/solatis/karma-chai-things)
as recommended in https://github.com/chaijs/chai-json-schema/issues/35

  * [Chai](http://chaijs.com)
  * [chai-json-schema](http://chaijs.com/plugins/chai-json-schema)

for [Karma](http://karma-runner.github.io)

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

karma-chai-json-schema currently does not support AMD/RequireJS, mainly because I cannot figure out the way this dependency should be injected. I encourage other people to look into this and hack it to make it work!
