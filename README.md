# Simple Storage Smart Contract

## Task
Create a Solidity smart contract that stores an unsigned integer and allows users to increment and decrement it.

## Contract
The contract is in `contracts/SimpleStorage.sol`.

- `value`: Public unsigned integer; its value can be read from outside the contract.
- `increment()`: Increases `value` by 1.
- `decrement()`: Decreases `value` by 1. It reverts if `value` is already 0.
- `getValue()`: Read-only function that returns the current value.

## Compile, deploy, and test with Remix IDE

1. Open https://remix.ethereum.org/.
2. Create a file named `SimpleStorage.sol` and paste the code from `contracts/SimpleStorage.sol`.
3. In the Solidity Compiler panel, select a compatible 0.8.x compiler and compile the file.
4. Open Deploy & Run Transactions.
5. Select Remix VM as the environment and click **Deploy**.
6. Expand the deployed contract.
7. Click `value` or `getValue` to read the current value (initially `0`).
8. Click `increment` three times. Read the value; it should be `3`.
9. Click `decrement` once. Read the value; it should be `2`.
10. Try `decrement` when the value is `0`; the transaction should revert with `Value cannot be negative`.

## Example test results

| Action | Expected value |
|---|---:|
| Initial read | 0 |
| increment() | 1 |
| increment() | 2 |
| increment() | 3 |
| decrement() | 2 |
| getValue() | 2 |

## Notes
- This project uses Solidity `^0.8.0`.
- Remix VM is a local test environment; deploying there does not publish the contract to a public blockchain.
"# task-1" 
