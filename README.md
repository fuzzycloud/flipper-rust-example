# Flipper Contract

This project contains a simple smart contract written in Rust using the `ink!` framework.

## Prerequisites

Ensure you have the following tools installed and set up before running these commands:

- Rust and Cargo (with `cargo-contract` installed)
- Substrate Contracts Node (installable via Cargo)
- A running instance of the Substrate contracts node

### Installing Required Tools

To install `cargo-contract` and the Substrate contracts node, use the following commands:

```sh
cargo install cargo-contract --force
cargo install contracts-node --git https://github.com/paritytech/substrate-contracts-node.git --tag <latest-tag> --force --locked

To build the contract, use the following command:
cargo contract build


Running the Substrate Contracts Node
To run a local Substrate contracts node with detailed logging, use the following command:
substrate-contracts-node --log info,runtime::contracts=debug 2>&1


Instantiating the Contract
To instantiate the contract with an initial argument and a unique salt value, use the following command:
cargo contract instantiate --constructor new --args "false" --suri //Alice --salt $(date +%s) --execute
