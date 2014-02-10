
# koa-request-body [![Build Status](https://travis-ci.org/thomseddon/koa-request-body.png?branch=master)](https://travis-ci.org/thomseddon/koa-request-body)

Parse the request body in koa like ya' used to in express

## Installation

```
npm install koa-request-body
```

## Options
 - `empty` whether to throw a 415 if the client has indicated there is a body but it cannot be parsed (default: `true`)

## Example



```js
var bodyParser = require('koa-request-body');
var koa = require('koa');

var app = koa();

app.use(bodyParser());

app.use(function *() {
  this.body = this.request.body; // Echo request back
  this.status = 200;
});

app.listen(3000);
```

## License

MIT
