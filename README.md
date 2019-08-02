# RenVM SDK

[![CircleCI](https://circleci.com/gh/renproject/renvm-sdk-js.svg?style=shield&circle-token=6fc560c540eff6670e5675841d34b9769b887a49)](https://circleci.com/gh/renproject/renvm-sdk-js)
[![Testnet status](https://img.shields.io/endpoint?url=https://ren-status.herokuapp.com/api/shield/renproject/renvm-sdk-js/testnet)](https://ren-status.herokuapp.com)
[![Devnet status](https://img.shields.io/endpoint?url=https://ren-status.herokuapp.com/api/shield/renproject/renvm-sdk-js/devnet)](https://ren-status.herokuapp.com)

The official Javascript SDK for interacting with the [RenVM](https://renproject.io).

## Links

* [Official SDK Docs](https://app.gitbook.com/@renproject/s/developers)
* [Cloneable Examples](https://github.com/republicprotocol/dex-demo)

## Installation

Add the RenVM SDK using Yarn/npm:

```bash
yarn add @renproject/ren
```
or
```bash
npm install --save @renproject/ren
```

## Importing the SDK

Importing using the require syntax

```typescript
const RenVM = require("@renproject/ren").default;
```

Importing using the ES6 syntax

```typescript
import RenVM from "@renproject/ren";
```

## Usage

```typescript
const sdk = new RenVM("testnet");
```

For more information, [check out an example](https://app.gitbook.com/@renproject/s/developers/examples/bitcoin-payments).

<hr />

## Dev

### Building

```bash
yarn run watch
# or
yarn run build
```

### Tests

You'll need to create a `.env` file which contains the following exported variables:

```bash
export MNEMONIC="some mnemonic here"
export ETHEREUM_NODE="ethereum node url (e.g. Infura)"
```

Then just run the following command to execute the tests. Make sure there is sufficient Kovan ETH in the linked account before running tests.

```bash
yarn run test
```

### Update Typescript bindings

In order to update the bindings in `src/contracts/bindings`, you need to clone [`darknode-sol`](https://github.com/renproject/darknode-sol) and run:

```bash
yarn run bindings:ts
```
