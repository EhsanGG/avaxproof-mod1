# Avalanche Local Subnet and Smart Contract Deployment

This guide demonstrates how to set up a local Avalanche Subnet and deploy two smart contracts (`token.sol` and `vault.sol`) using Remix and MetaMask.

## Prerequisites

Before you begin, make sure you have the following installed:

- **Golang**: Required for building `avalanche-cli`.
- **Node.js**: Required for running the local Avalanche node.
- **Avalanche CLI**: Follow the [Avalanche CLI Installation Guide](https://docs.avax.network/tooling/cli-guides/install-avalanche-cli) to install `avalanche-cli`.
- **MetaMask**: Install and configure MetaMask for connecting to the local Avalanche node.
- **Remix**: Use Remix for compiling and deploying smart contracts.

## Step 1: Set Up Local Subnet

### Create a Subnet Configuration

1. Run the command `avalanche subnet create` and follow the wizard.
2. Name your Subnet (e.g., `mySubnet`).
3. Choose `SubnetEVM` as the VM type.
4. Set a ChainID (e.g., `43113`).
5. Adjust any other options based on your needs.

### Deploy the Subnet Locally

1. Export the Subnet configuration by running `avalanche subnet export`.
2. Deploy the Subnet with the command `avalanche subnet deploy --local`.

## Step 2: Deploy Smart Contracts

### Compile Contracts in Remix

1. Open Remix and create a new workspace.
2. Import `token.sol` and `vault.sol`.
3. Compile both contracts.

### Connect Remix to the Local Node

1. In Remix, go to the "Deploy" tab.
2. From the "ENVIRONMENT" dropdown, select "Injected Web3".
3. Make sure MetaMask is connected to your local Avalanche node.

### Deploy the Contracts

For each contract:

1. Select the contract in the "Deployer" section.
2. Enter any constructor arguments if needed.
3. Click "Deploy".
4. Confirm the transaction in MetaMask.

## Step 3: Interact with the Contracts

You can use Remix to interact with your deployed contracts, including calling functions, reading data, and monitoring events.
