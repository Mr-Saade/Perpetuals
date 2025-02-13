# A Minimum Perpetuals Trading Protocol

## Overview

This is an on-chain perpetuals trading protocol that enables traders to open leveraged positions using a decentralized system. The protocol allows users to go long or short on an index token while ensuring risk management via collateralization, position tracking, and borrowing fees.

## Features

- **Leverage Trading**: Traders can open leveraged long or short positions.
- **Collateralized Positions**: Positions are backed by collateral deposits.
- **Oracle-based Pricing**: Real-time asset prices via Chainlink oracles.
- **Borrowing Fees**: Continuous funding fees are calculated based on open interest.
- **Liquidation Mechanism**: Positions are liquidated when they breach leverage limits.
- **Maximum Utilization Check**: Ensures protocol solvency by capping utilization ratio.
- **Fuzzing-based Test Suite**: Robust testing framework using fuzzing to cover edge cases.

## Smart Contract Architecture

### `MinimumPerps.sol`

The core perpetual trading contract, responsible for:

- Managing long and short positions
- Handling deposits and withdrawals
- Implementing borrowing fee calculations
- Enforcing liquidation conditions

### `Oracle.sol`

Provides price data for the index token and collateral token using Chainlink oracles.

### `Errors.sol`

Contains custom error definitions for gas-efficient reverts.

### `Calc.sol`

Utility library for rounding and arithmetic operations.

## Installation

```sh
git clone https://github.com/Mr-Saade/Perpetuals.git
cd Perpetuals
forge install
```

## Running Tests

```sh
forge test
```

## License

This project is licensed under the MIT License.

## Contributions

Contributions are welcome! Feel free to submit issues and pull requests.
