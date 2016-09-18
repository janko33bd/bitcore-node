Blackcore Node
============

A Blackcoin full node for building applications and services with Node.js. A node is extensible and can be configured to run additional services. At the minimum a node has native bindings to Blackcoin Core with the [Blackcoin Service](docs/services/bitcoind.md). Additional services can be enabled to make a node more useful such as exposing new APIs, adding new indexes for addresses with the [Address Service](docs/services/address.md), running a block explorer, wallet service, and other customizations.

Note: For your convenience, we distribute binaries for x86_64 Linux and x86_64 Mac OS X. Upon npm install, the binaries for your platform will be downloaded. For more detailed installation instructions, or if you want to compile the project yourself, then please see the [Build & Install](docs/build.md) documentation to build the project from source.

## Get Started
```
git clone -b blackcore-node https://github.com/janko33bd/bitcore-node.git blackcore-node
cd blackcore-node
npm install
```
## Keep going ;P
to create a node you will need blackcore-lib too, visit
https://github.com/janko33bd/bitcore-lib/tree/blackcore-lib
and build from source

use bitcore-node from previous compiled directory to create a node
```
./bitcore-node/bin/bitcore-node create black-node
```
now copy your compiled bitcore-node to black-node/node_modules/bitcore-node/build/Release
and replace the whole lib directory from blackcore-lib here black-node/node_modules/bitcore-lib
and copy module scryptsy from blackcore-lib/node_modules to black-node/node_modules

```
cd black-node
../bitcore-node/bin/bitcore-node start

info: Starting bitcoind
info: Bitcoin Daemon Ready
info: Starting db
info: Bitcoin Database Ready
info: Starting address
info: Starting web
info: Bitcore Node ready
info: Bitcoin Height: 16 Percentage: 0.00019133722526021302
info: Bitcoin Height: 32 Percentage: 0.0003714192716870457
info: Bitcoin Height: 48 Percentage: 0.0005515012890100479
...
...
```

## Prerequisites

- Node.js v0.12 or v4.2
- ~10GB of disk storage
- ~4GB of RAM
- Mac OS X >= 10.9, Ubuntu >= 12.04 (libc >= 2.15 and libstdc++ >= 6.0.16)

## Add-on Services

There are several add-on services available to extend the functionality of Bitcore:

- [Insight API](https://github.com/bitpay/insight-api/tree/v0.3.0)
- [Insight UI](https://github.com/bitpay/insight/tree/v0.3.0)
- [Bitcore Wallet Service](https://github.com/bitpay/bitcore-wallet-service)

## Documentation

- [Services](docs/services.md)
  - [Bitcoind](docs/services/bitcoind.md) - Native bindings to Bitcoin Core
  - [Database](docs/services/db.md) - The foundation API methods for getting information about blocks and transactions.
  - [Address](docs/services/address.md) - Adds additional API methods for querying and subscribing to events with bitcoin addresses.
  - [Web](docs/services/web.md) - Creates an express application over which services can expose their web/API content
- [Build & Install](docs/build.md) - How to build and install from source
- [Testing & Development](docs/testing.md) - Developer guide for testing
- [Node](docs/node.md) - Details on the node constructor
- [Bus](docs/bus.md) - Overview of the event bus constructor
- [Errors](docs/errors.md) - Reference for error handling and types
- [Patch](docs/patch.md) - Information about the patch applied to Bitcoin Core
- [Release Process](docs/release.md) - Information about verifying a release and the release process.

## Contributing

Please send pull requests for bug fixes, code optimization, and ideas for improvement. For more information on how to contribute, please refer to our [CONTRIBUTING](https://github.com/bitpay/bitcore/blob/master/CONTRIBUTING.md) file.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore-node/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc.

- bitcoin: Copyright (c) 2009-2015 Bitcoin Core Developers (MIT License)
