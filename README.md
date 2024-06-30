# ETH-AVAX-_Module3
Overview
CustomCoin is an ERC-20 compliant token contract implemented in Solidity. It allows the creation, transfer, and management of tokens, including minting and burning functionalities.

Features

Token Transfers: Send tokens between accounts.
Allowance Management: Approve and transfer tokens on behalf of other accounts.
Minting: Create new tokens and increase total supply.
Burning: Destroy tokens and decrease total supply.
Events: Emit logs for transfers, approvals, minting, and burning.

Contract Details

Name: CustomCoin
Symbol: Specify during deployment
Decimals: Specify during deployment
Initial Supply: Specify during deployment
Admin: The account that deploys the contract

Functions
Public Functions
sendCoins(address _receiver, uint256 _amount): Transfer tokens to another address.
authorizeSpender(address _spender, uint256 _amount): Approve another address to spend tokens on your behalf.
transferFromAccount(address _from, address _to, uint256 _amount): Transfer tokens from one account to another using allowance.
mintCoins(address _recipient, uint256 _amount): Mint new tokens (admin only).
burnCoins(uint256 _amount): Burn tokens from the caller’s account.
increaseSpendingLimit(address _spender, uint256 _addedValue): Increase the allowance for a spender.
decreaseSpendingLimit(address _spender, uint256 _subtractedValue): Decrease the allowance for a spender.

Modifiers
onlyAdmin: Restricts function access to the contract admin.

Events
Sent(address indexed sender, address indexed receiver, uint256 amount): Emitted on token transfer.
Authorized(address indexed owner, address indexed spender, uint256 amount): Emitted on allowance approval.
Created(address indexed recipient, uint256 amount): Emitted on token minting.
Destroyed(address indexed holder, uint256 amount): Emitted on token burning.

Usage
Deploy the Contract: Provide the initial parameters (name, symbol, decimals, initial supply).
Interact with Functions: Use a compatible Ethereum wallet or interface to interact with the contract functions.
