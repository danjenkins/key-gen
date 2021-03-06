key-gen
=======

A lightweight node.js key generation app.

## v0.0.1

## Info

**Note** There are 3 possible env vars that can be set in order to customise to suit your needs:

* process.env.APP_SALT
* process.env.APP_ENCRYPTION
* process.env.APP_ENCODING

Default values are used if these aren't set and they can be found in config/config.js.

###Note:
Prior to setting the env vars I encourage you to read on [crypto] (http://nodejs.org/api/crypto.html#crypto_crypto_createhmac_algorithm_key)
from the node.js documentation and especially on Hmac class which is used in generating the key here.

## Installation

```sh
$ npm install key-gen
```

## Usage

```js
var keyGen = require('key-gen');

var options = {
  prefix: ['identifier1', 'identifier2', 'identifier3'],
  data: {
    data1: 'data1',
    data2: 'data2',
    data3: 'data3'
  }
}

var key = keyGen.generate(options);
```
Provided the default config values remain unchanged the above key will equal:

**identifier1:identifier2:identifier3:4c0398bf4e511bef5355c32fd71bc9f1ffcde3b144cf3725dae9062cfaa1ab118d4c984855d38dea8efa00422de45e511c3da710541c7c578ee26037ff1d9a4a**


## Run tests

```sh
$ make test
```

## License

Released fully under [MIT license] (http://viktort.mit-license.org)
