# Burnable Token Smart Contract

This project implements a burnable token smart contract using the MultiversX (formerly Elrond) blockchain platform. The smart contract is written in Rust and compiled to WebAssembly (WASM) for execution on the blockchain.

## Overview

The Burnable Token contract allows users to create a token with an initial supply and burn tokens from their balance. The contract is designed to be simple and efficient, utilizing the MultiversX smart contract framework.

### Key Features

- **Token Initialization**: Set up an initial supply of tokens for the deploying address.
- **Burn Functionality**: Users can reduce their token balance by burning tokens, effectively removing them from circulation.
- **Balance Management**: View the token balance of any address.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Rust](https://www.rust-lang.org/tools/install) (with `wasm32-unknown-unknown` target)
- MultiversX SDK and CLI tools

## Project Structure

burnable_token/
│
├── src/
│ └── lib.rs # Main Rust source file with the smart contract code
│
├── tests/
│ └── integration_test.rs # Integration tests for the contract
│
├── Cargo.toml # Rust project manifest file with dependencies
├── Cargo.lock # Lockfile for dependency versions
│
├── multiversx.json # MultiversX-specific configuration file
│
├── README.md # Documentation for the project
│
├── LICENSE # License file for the project
│
└── .gitignore # Git ignore file to exclude unnecessary files

Copy

## Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/burnable_token.git
   cd burnable_token
Install Rust and Add WASM Target

Ensure Rust is installed, and add the target for WebAssembly:

rustup target add wasm32-unknown-unknown
Build the Contract

Compile the contract to WASM using Cargo:

cargo build --release --target wasm32-unknown-unknown
Running Tests
To test the functionality of the contract, run the integration tests:

bash
Copy
cargo test
Usage
Initializing the Contract
Deploy the contract and initialize it with an initial supply of tokens for the deploying address. The deployer will have full control over the initial token supply.

Burning Tokens
Users can burn tokens from their balance by calling the burn endpoint. This reduces the total token balance they hold.

Viewing Balances
The get_balance view function allows users to check the token balance of any address.

Configuration
The multiversx.json file contains metadata and configuration for the contract, such as its name, version, and description. Ensure this file is properly configured before deploying the contract.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue.

Acknowledgments
MultiversX Documentation
Rust Programming Language
This README provides all the necessary details to understand, set up, and use the burnable token smart contract on the MultiversX blockchain. Adjust the content as needed to reflect any additional features or changes you make to the project.
