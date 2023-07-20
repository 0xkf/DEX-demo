BNBchain DEX

USDC TOKEN
https://bscscan.com/tx/0xed733d05dc189db867e64718907a371d0ed379c9a88a45f26241607a0abb9e2b

JOE TOKEN
https://bscscan.com/tx/0xc526bee2b8a7dded10fa6db4d587ca91a69e180ddf065470a16175fc8325b175

AMM .sol
https://bscscan.com/tx/0xadcefcbfb09be3b44d1fd68aca6bc34888bd05462b66e7f3cab62af1a83da1bc



Approve USDC
https://bscscan.com/tx/0x67efa879125cf37ba71c54b103ee96cd43445e4b827c650e4bd61f1c3e628e27

Approve JOE
https://bscscan.com/tx/0xb375fe526b6e791001c71673bd6f0685b7765d3fd8823ef30ff3767a86ee39f5

provide Liquidity
https://bscscan.com/tx/0xf07eabe208d19aa5ec1d4e8f3982796f6d396f877e1e976dffa46e995c3b096c

swap
(approve)https://bscscan.com/tx/0xe6b1a2eccacbe9632b9537d360d9ff9f5cb1d2d946ec6555280e52f46cb304f6
(swap)https://bscscan.com/tx/0xadb829574771802c476bcf09020d4d8be1a9c3fe3dcb30e7ba98d62c1d1fcbf8 


# About This Project

`Miniswap` is a amm dapp that allows tokens to be exchanged like `Uniswap`.


# Usage

### Connect wallet

Add the following network before:

```
Network Name: BNB C-Chain
Symbol: BNB
```

# Build & run

```
git clone [this_repository]
cd [this_repository]
yarn install
yarn client dev
```

After executing the above command, access `localhost:3000` in your browser.

# Description

## Chain deployed to: `Avalanche`

## Contract

### Stack description

contract

- Solidity

test & deploy

- hardhat
- typescript

### Directory structure

Root: `package/contract`

- `AMM.sol`  
  Implementing AMM contract code.
- `ERC20Tokens.sol`  
  Implementing ERC20 contracts To simulate the AMM

### Walk-through of `AMM`'s code

- function: `provide`  
  Provide liquidity with the address and quantity of the token as arguments.  
  The contract records share (like `LP token`) for the user who calls this function.

- function: `withdraw`  
  Withdraw tokens deposited with share as an argument.

- function: `swap`  
  Swap tokens.  
  Using the formula:`k = x * y` for calculation, and there is a 0.3% fee for swapping.

## Client

### Stack description

- typescript
- React.js
- Next.js

### Directory structure

Root: `package/client`

- `components`, `hooks`, `pages`, `styles`, `public`  
  Contains client side code
- `utils`  
  Contains the contracts ABI and utility functions.
