# WYADVAVAXM1

## Overview

The Vault smart contract is designed to serve as a simple vault for managing deposits and withdrawals of an ERC-20 token. Users can deposit tokens into the vault, receiving shares in return, and later withdraw tokens based on the number of shares they hold.

## Smart Contract Functions

### `deposit(uint _amount) external`

The `deposit` function allows users to deposit ERC-20 tokens into the vault. Users receive shares in proportion to their deposit, and the total supply of shares increases accordingly.

### `withdraw(uint _shares) external`

The `withdraw` function enables users to withdraw ERC-20 tokens from the vault by burning a specified number of shares. The withdrawn tokens are proportional to the number of shares burned.

## Vault Math

The smart contract implements a simple formula for calculating shares and amounts based on the total supply of shares and the balance of tokens in the vault.

### Deposit Formula

\[ s = \frac{a \cdot T}{B} \]

Where:
- \( s \) is the number of shares to mint.
- \( a \) is the amount of tokens deposited.
- \( T \) is the total supply of shares.
- \( B \) is the balance of tokens before the deposit.
