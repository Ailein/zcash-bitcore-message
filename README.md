<img src="http://bitcore.io/css/images/module-message.png" alt="bitcore message" height="35">
# Bitcoin Message Verification and Signing for Bitcore


[![NPM Package](https://img.shields.io/npm/v/zcash-bitcore-message.svg?style=flat-square)](https://www.npmjs.org/package/zcash-bitcore-message)
[![Build Status](https://img.shields.io/travis/bitmex/zcash-bitcore-message.svg?branch=master&style=flat-square)](https://travis-ci.org/bitmex/zcash-bitcore-message)
[![Coverage Status](https://img.shields.io/coveralls/bitmex/zcash-bitcore-message.svg?style=flat-square)](https://coveralls.io/r/bitmex/zcash-bitcore-message?branch=master)

zcash-bitcore-message adds support for verifying and signing zcash messages in [Node.js](http://nodejs.org/) and web browsers.

Forked for [Zcash](https://github.com/zcash/zcash) for use with [Bitcore](https://github.com/bitmex/zcash-bitcore).

Credit to @bitpay for the original implementation and @str4d for the Zcash fork.

See [the main bitcore repo](https://github.com/bitpay/bitcore) for more information.

## Getting Started

```sh
npm install zcash-bitcore-message
```

```sh
bower install zcash-bitcore-message
```

To sign a message:

```javascript
var bitcore = require('zcash-bitcore-lib');
var Message = require('zcash-bitcore-message');

var privateKey = bitcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/bitpay/bitcore/blob/master/CONTRIBUTING.md) on the main bitcore repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

