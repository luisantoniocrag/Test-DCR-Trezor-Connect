# Test-DCR-Trezor-Connect

There are the results (responses) of Decred and Decred Testnet with Trezor-Connect.

For [Decred responses](./src/test-mainnet.js).

For [Decred Testnet responses](./src/test-testnet.js).

It was tested in this way.

```bash
$ mkdir dcr-trezor
$ pushd dcr-trezor
```

```bash
$ git clone https://github.com/rickmort/trezor-utxo-lib.git
$ pushd trezor-utxo-lib
$ git checkout adddecred
$ yarn link
$ yarn
$ git popd
```

```bash
$ git clone https://github.com/rickmort/connect.git
$ pushd connect
$ git checkout adddecred
$ yarn link @trezor/utxo-lib
$ yarn
$ yarn dev
```

now keep running this on: https://localhost:8088/
open a new terminal.

```bash
$ git clone https://github.com/rickmort/connect-explorer.git
$ pushd connect-explorer
$ git checkout adddecred
$ yarn
$ yarn dev:local
```

Now open: https://localhost:8082

