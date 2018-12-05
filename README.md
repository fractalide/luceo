# luceo

The Luceo command line interface provides the following features:

* powerful blockchain manager: with download, explore, verify, and analyze functions
* ability to manage multiple wallets: Daedalus', Icarus' or custom wallets
* flexible transaction build engine

This command line interface is built upon the
[**Rust Cardano SDK**](https://github.com/input-output-hk/rust-cardano).

## Warning

* The software is currently still in alpha phase, please do not use for
  any other purpose than debugging and testing, until stable releases are available.
* While most of the operations in the CLI is in a reading state, and are thus
  relatively safe even in the presence of bugs, do take special note that
  `transaction send` will permanently change your state.
* It is advisable to trial testnet operations (depending on testnet availability),
  prior to completing mainnet operations.
* If you think something is suspicious, it may very well be the case.
  Check the documentation, or ask for help.
* Do not share your wallet mnemonics, passwords, cryptographic material, or pending signatures.

## Installation guide

While it is recommended to wait for official releases, it is also possible
to build the executable yourself by following these steps:

1. [install rust toolchain](;https://www.rust-lang.org/en-US/install.html);
2. clone the project repository
   ```sh
   mkdir luceo-project
   git clone https://github.com/fractalide/luceo.git
   ```
3. clone the project dependencies
   ```sh
   cd luceo-project
   git clone https://github.com/fractalide/luceo-common.git
   ```
4. build and install the binary:
   ```sh
   cd luceo
   cargo install
   ```
5. enjoy

## Usage

### Quick start

```sh
$ luceo blockchain new testnet
$ luceo blockchain pull testnet
$ luceo wallet create "My Wallet"
$ luceo wallet attach "My Wallet" testnet
$ luceo wallet sync   "My Wallet"
$ luceo wallet status "My Wallet"
```

### Complete documentation

[Command line documentation](./USAGE.md)

# License

This project is licensed under either of the following licenses:

 * MPLv2 license ([LICENSE](LICENSE) or
   https://opensource.org/licenses/MPL-2.0)
