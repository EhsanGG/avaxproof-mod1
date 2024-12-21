Setting Up an Avalanche Subnet and Deploying Smart Contracts

This guide shows you how to create a local Avalanche Subnet and deploy two smart contracts: token.sol and vault.sol using Remix and MetaMask.
What You Need

    Golang: Install it to build avalanche-cli.
    Node.js: Install it to run the Avalanche node.
    Avalanche CLI: Install it by following the Avalanche CLI Installation Guide.
    MetaMask: Set it up to connect to the local Avalanche node.
    Remix: Open Remix and create a new workspace.

Setting Up the Local Subnet
Create a Subnet:

    Run avalanche subnet create and follow the instructions to create a Subnet.
    Name your Subnet (e.g., mySubnet).
    Choose SubnetEVM for the VM.
    Pick a ChainID (e.g., 43113).
    Set any other options as needed.

Deploy the Subnet:

    Run avalanche subnet export to save the Subnet configuration.
    Deploy it locally using avalanche subnet deploy --local.

Deploying Smart Contracts
Compile the Contracts:

    In Remix, open token.sol and vault.sol.
    Compile both contracts.

Connect Remix to the Local Node:

    In Remix, go to the "Deploy" tab and select "Injected Web3" in the "ENVIRONMENT" dropdown.
    Make sure MetaMask is connected to the local Avalanche node.

Deploy the Contracts:

For each contract:

    Choose the contract in the "Deployer" section.
    If there are constructor arguments, enter them.
    Click "Deploy".
    Confirm the transaction in MetaMask.

Interacting with the Contracts:

Use Remix to call functions, read data, and watch events from the deployed contracts.
