# MVP_contract

A minimal SimpleStorage smart contract built with Hardhat.

## Overview

This project demonstrates a basic Ethereum smart contract development workflow using Hardhat. It includes a simple storage contract that can store and retrieve a value.

## Features

- SimpleStorage contract with set/get functionality
- Hardhat development environment
- Ignition deployment framework
- Local blockchain for testing

## Prerequisites

- Node.js and npm installed
- Basic knowledge of Solidity and JavaScript

## Installation

1. Clone the repository
2. Install dependencies:
```bash
npm install
```

## Usage

### Compile the contract

```bash
npx hardhat compile
```

### Start a local blockchain

```bash
npx hardhat node
```

### Deploy the contract using Ignition

```bash
npx hardhat ignition deploy ignition/modules/simple-storage.js --network localhost
```

### Interact with the contract

```bash
npx hardhat console --network localhost
```

In the console:
```javascript
// Get the contract factory
const SimpleStorage = await ethers.getContractFactory("SimpleStorage");

// Connect to the deployed contract (replace with your contract address)
const simpleStorage = await SimpleStorage.attach("YOUR_CONTRACT_ADDRESS");

// Set a value
await simpleStorage.set(42);

// Get the value
const value = await simpleStorage.get();
console.log(value.toString());
```

## Project Structure

- `contracts/`: Smart contract source files
- `ignition/`: Deployment modules for Hardhat Ignition
- `test/`: Test scripts for the smart contract
