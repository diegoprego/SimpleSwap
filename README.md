# SimpleSwap

A minimalist implementation of an Automated Market Maker (AMM), inspired by Uniswap v2. This smart contract allows users to:

- Add/remove liquidity to a token pair pool
- Swap between two ERC-20 tokens
- Mint/burn LP tokens to track ownership in the pool

## Features

- Constant product pricing formula (`x * y = k`)
- First-time liquidity provision sets the token pair
- Slippage protection and deadline enforcement
- Price quoting and output estimation
- LP token tracking via ERC-20 standard

## Functions

### `addLiquidity(...)`

Provides liquidity to the pool and mints LP tokens to the user. If this is the first liquidity provision, the token pair is initialized.

### `removeLiquidity(...)`

Burns LP tokens in exchange for the user's proportional share of the pool’s tokens.

### `swapExactTokensForTokens(...)`

Performs a swap from one token to another using the pool's reserves, enforcing minimum output and deadline.

### `getPrice(tokenA, tokenB)`

Returns the spot price of token A in terms of token B.

### `getAmountOut(amountIn, reserveIn, reserveOut)`

Utility function to calculate output amount given input and reserves.

## Setup

Install dependencies:

```bash
npm install @openzeppelin/contracts
