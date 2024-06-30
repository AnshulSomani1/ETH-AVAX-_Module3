# CustomCoin ERC-20 Token Contract

CustomCoin is an ERC-20 compliant token contract implemented in Solidity. It allows the creation, transfer, and management of tokens, including minting and burning functionalities.

## Features

- **Token Transfers:** Send tokens between accounts.
- **Allowance Management:** Approve and transfer tokens on behalf of other accounts.
- **Minting:** Create new tokens and increase total supply.
- **Burning:** Destroy tokens and decrease total supply.
- **Events:** Emit logs for transfers, approvals, minting, and burning.

## Contract Details

- **Name:** CustomCoin
- **Symbol:** Specify during deployment
- **Decimals:** Specify during deployment
- **Initial Supply:** Specify during deployment
- **Admin:** The account that deploys the contract

## Functions

### Public Functions

#### `sendCoins(address _receiver, uint256 _amount)`
- **Description:** Transfer tokens to another address.
- **Parameters:**
  - `_receiver`: The recipient's address.
  - `_amount`: The amount of tokens to transfer.

#### `authorizeSpender(address _spender, uint256 _amount)`
- **Description:** Approve another address to spend tokens on your behalf.
- **Parameters:**
  - `_spender`: The address authorized to spend tokens.
  - `_amount`: The maximum amount of tokens that can be spent.

#### `transferFromAccount(address _from, address _to, uint256 _amount)`
- **Description:** Transfer tokens from one account to another using allowance.
- **Parameters:**
  - `_from`: The sender's address.
  - `_to`: The recipient's address.
  - `_amount`: The amount of tokens to transfer.

#### `mintCoins(address _recipient, uint256 _amount)`
- **Description:** Mint new tokens (admin only).
- **Parameters:**
  - `_recipient`: The recipient's address.
  - `_amount`: The amount of tokens to mint.

#### `burnCoins(uint256 _amount)`
- **Description:** Burn tokens from the caller’s account.
- **Parameters:**
  - `_amount`: The amount of tokens to burn.

#### `increaseSpendingLimit(address _spender, uint256 _addedValue)`
- **Description:** Increase the allowance for a spender.
- **Parameters:**
  - `_spender`: The address whose spending limit is increased.
  - `_addedValue`: The additional amount to approve for spending.

#### `decreaseSpendingLimit(address _spender, uint256 _subtractedValue)`
- **Description:** Decrease the allowance for a spender.
- **Parameters:**
  - `_spender`: The address whose spending limit is decreased.
  - `_subtractedValue`: The amount to decrease from the spending limit.

### Modifiers

#### `onlyAdmin`
- **Description:** Restricts function access to the contract admin.

### Events

#### `Sent(address indexed sender, address indexed receiver, uint256 amount)`
- **Description:** Emitted on token transfer.
- **Parameters:**
  - `sender`: The address sending the tokens.
  - `receiver`: The address receiving the tokens.
  - `amount`: The amount of tokens transferred.

#### `Authorized(address indexed owner, address indexed spender, uint256 amount)`
- **Description:** Emitted on allowance approval.
- **Parameters:**
  - `owner`: The owner of the tokens.
  - `spender`: The address authorized to spend tokens.
  - `amount`: The amount of tokens approved.

#### `Created(address indexed recipient, uint256 amount)`
- **Description:** Emitted on token minting.
- **Parameters:**
  - `recipient`: The address receiving the minted tokens.
  - `amount`: The amount of tokens minted.

#### `Destroyed(address indexed holder, uint256 amount)`
- **Description:** Emitted on token burning.
- **Parameters:**
  - `holder`: The address burning the tokens.
  - `amount`: The amount of tokens burned.

## Usage

1. **Deploy the Contract:** Provide the initial parameters (name, symbol, decimals, initial supply).
2. **Interact with Functions:** Use a compatible Ethereum wallet or interface to interact with the contract functions.

## Requirements

- **Solidity version:** ^0.8.0
- **Ethereum wallet (e.g., MetaMask)** to interact with the contract.

## License

This project is licensed under the MIT License.
