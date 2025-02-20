# Solidity Transfer Function Error

This repository demonstrates a common error in Solidity smart contracts: an unhandled exception in a transfer function. The `transfer` function does not handle cases where the sender's balance is insufficient to cover the transfer amount, leading to a failed transaction and potential loss of funds.

The `bug.sol` file contains the erroneous code. The `bugSolution.sol` file demonstrates a corrected version.

## How to reproduce

1. Compile the contract in `bug.sol`.
2. Deploy the contract to a test network.
3. Attempt to transfer more tokens than the sender has in their balance. The transaction will revert.

## Solution

The solution involves adding an appropriate `require` statement to verify that the sender's balance is sufficient before proceeding with the transfer.