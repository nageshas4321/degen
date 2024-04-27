# DegenToken Contract

This Solidity smart contract implements a custom ERC20 token called DegenToken, with additional functionality such as minting, burning, and redeeming "guns".

## Overview

The `DegenToken` contract is based on the ERC20 standard and extends functionality from the OpenZeppelin `ERC20`, `Ownable`, and `ERC20Burnable` contracts. It allows for the creation of a custom token with a specified name, symbol, initial supply, and owner. Additionally, users can redeem "guns" using their token balance.

### Features

- Customizable token name and symbol
- Initial token supply specified during deployment
- Ownership functionality provided by the `Ownable` contract
- Minting of new tokens by the contract owner
- Burning of tokens by any token holder
- Redeeming "guns" using tokens

## Deployment

The contract can be deployed to any Ethereum-compatible blockchain network. During deployment, no additional parameters are required. The token name and symbol are hardcoded as "DEGEN" and "DGN" respectively.

## Usage

Once deployed, the contract provides the following functions for interacting with the token:

- `mintTokens`: Mint new tokens and assign them to a specified address. Only the contract owner can call this function.
- `burnTokens`: Burn a specified amount of tokens from the caller's balance.
- `transferTokens`: Transfer tokens from the caller's address to a specified recipient.
- `redeemGun`: Redeem a specified amount of "guns" by burning tokens. Guns have different prices and enumerate values, and can be redeemed using tokens.

## Security Considerations

- Ensure that the contract owner address is securely set during deployment to prevent unauthorized access to administrative functions.
- Exercise caution when calling the `burnTokens` and `redeemGun` functions, as they involve token burning which cannot be reversed.

