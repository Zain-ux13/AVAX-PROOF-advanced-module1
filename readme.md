Easy Guide to Set Up a Local Avalanche Subnet and Deploy Smart Contracts

This guide will walk you through setting up a local Avalanche Subnet and deploying smart contracts with Remix and MetaMask.
What You Need

    Golang: Install Golang to use avalanche-cli. Install it here.
    Node.js: Required for running the local Avalanche node. Download Node.js.
    Avalanche CLI: Install avalanche-cli by following the installation guide.
    MetaMask: A browser extension for managing your Avalanche assets. Install MetaMask and set up your wallet.
    Remix IDE: A web tool for writing and deploying smart contracts. Open Remix.

Setting Up Your Local Subnet
Step 1: Create the Subnet

    Open Terminal: Start your terminal or command prompt.

    Run the Command: Type this command to create your Subnet:

    sh

    avalanche subnet create

    Follow the Prompts:
        Name: Enter a name like mySubnet.
        VM Type: Choose SubnetEVM.
        ChainID: Pick a number like 151511.
        Additional Options: Set any other options if needed.

    Check Configuration: A configuration file will be generated. Make sure everything looks right.

Step 2: Deploy the Subnet

    Export Configuration: Use this command to export your Subnet setup:

    sh

avalanche subnet export

Deploy Locally: Start your local Avalanche node with:

sh

    avalanche subnet deploy --local

Deploying Your Smart Contracts
Step 1: Compile Contracts

    Open Remix: Go to Remix IDE.

    Upload Contracts:
        Create a new workspace or use an existing one.
        Drag your token.sol and vault.sol files into Remix or use the "Upload File" button.

    Compile Contracts:
        Click on the "Solidity Compiler" tab.
        Choose the right compiler version.
        Hit "Compile" for each contract.

Step 2: Connect MetaMask to Your Local Node

    Set Up MetaMask:
        Open MetaMask and add a new network with these details:
            Network Name: Local Avalanche
            RPC URL: http://localhost:9650/ext/bc/C/rpc (or the URL where your local node is running)
            Chain ID: 151511 (or your chosen ChainID)

    Connect Remix:
        In Remix, go to the "Deploy & Run Transactions" tab.
        Choose "Injected Web3" from the "ENVIRONMENT" dropdown.
        Ensure MetaMask is connected to your local Avalanche network.

Step 3: Deploy Your Contracts

    Deploy Each Contract:
        In Remix, select the contract you want to deploy.
        Add any constructor arguments if needed.
        Click "Deploy."
        Confirm the transaction in MetaMask.

    Check Deployment:
        After deploying, you'll see the contract address in Remix.
        Verify the contract is deployed by checking the address on your local node or in Remix.

Step 4: Interact with Contracts

    Use Remix:
        You can interact with your deployed contracts directly in Remix.
        Test functions, read data, and check events using the "Deployed Contracts" section.
