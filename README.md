# tiny-svg

[![Build Status](https://travis-ci.org/bpmn-io/tiny-svg.svg?branch=master)](https://travis-ci.org/bpmn-io/tiny-svg)

__tiny-svg__ is a minimal toolbelt for creating clean SVG applications.


## Features

* no wrapping magic, using native DOM elements instead
* modular, just use what you need
* `2kB` minified + gzipped
* `innerSVG` support
* simplified attribute handling
* geometry helpers

Checkout [provided utilities](./lib).


## Usage

```javascript
const {
  appendTo,
  classes,
  create,
  innerSVG
} = require('tiny-svg');

var container = document.createElement('div');
var element = appendTo(create('svg'), container);

var text = `
  <g class="foo bar">
    <rect x="0" y="0" width="0" height="0" rx="50" ry="50"/>
  </g>
`;

// set innerSVG
innerSVG(element, text);
```

Your favourite module bundler should apply tree-shaking to only include the components your application requires. If you're using CommonJS modules give [common-shake](https://github.com/indutny/common-shake) a try.


## License

MIT