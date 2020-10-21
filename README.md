# RareLink Node

This is the implementation of RareLink Node. It is still in development and not ready for use.

Once it connects as a parachain to Polkadot, it will act as a bridge between the Polkadot and the Ethereum networks.

It consists of the following parts:(in development)

* [pallet-commodities](https://docs.rs/pallet-commodities/1.0.0/pallet_commodities/index.html)
* [chainlink-polkadot](https://github.com/smartcontractkit/chainlink-polkadot)
* Bridge oracle implementation with **Off-Chain Workers** 


## Setup

Setup instructions can be found at the
[Substrate Developer Hub](https://substrate.dev/docs/en/knowledgebase/getting-started).

## Build

Once the development environment is set up, build the node template. This command will build the
[Wasm](https://substrate.dev/docs/en/knowledgebase/advanced/executor#wasm-execution) and
[native](https://substrate.dev/docs/en/knowledgebase/advanced/executor#native-execution) code:

```bash
cargo build --release
```

## Run

### Single Node Development Chain

Purge any existing dev chain state:

```bash
./target/release/node-template purge-chain --dev
```

Start a dev chain:

```bash
./target/release/node-template --dev
```

Or, start a dev chain with detailed logging:

```bash
RUST_LOG=debug RUST_BACKTRACE=1 ./target/release/node-template -lruntime=debug --dev
```

### Multi-Node Local Testnet

If you want to see the multi-node consensus algorithm in action, refer to
[our Start a Private Network tutorial](https://substrate.dev/docs/en/tutorials/start-a-private-network/).
