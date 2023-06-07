# Blockchain Based Systems Engineering
## Ethereum Basics: Setting Up a Development Environment

### Setup
In this exercise sheet, you are asked to set up an environment for developing smart contracts on the Ethereum blockchain. While we advise you to use the tools we propose, you are free to use any tool you want to.

**Recommended Software:**
- Node.js
- NPM
- Truffle
- Ganache by Truffle
- MetaMask
- Visual Studio Code
- Visual Studio Code Extension: Solidity

**Recommended Services:**
- Infura

### Setting Up a Sepolia Account
1. Install MetaMask.
2. Configure your MetaMask account (Write down your seed phrase! You will need it later).
3. Open MetaMask and switch the network to Sepolia.
4. Find some Sepolia Test Ether using a Faucet. One option is using the Faucet provided by Infura at https://faucet.infura.io/ or ask your fellow students for a small donation. For this exercise, 0.1 Sepolia Ether will be sufficient.
5. Send 0.001 Sepolia Ether to 0xaCb576A3f9F9ffa1e2276A1C06C0Ade4fE2197f8 (our address on Sepolia) and inspect your transaction on Sepolia Etherscan.

### Setting Up Your Local Development Environment
1. Install Visual Studio Code.
2. Install the Solidity extension inside Visual Studio Code.
3. Install Truffle globally on your computer: npm install -g truffle (Check your Node.js and NPM version if you face a problem during installment)
4. Create an empty working directory and initialize a bare Truffle project with no smart contracts in it.
5. Run `truffle init`.
    - Contracts: Directory for Solidity smart contracts.
    - Migrations: Directory for scriptable deployment files.
    - Test: Directory for test files for testing your application and contracts.
    - truffle-config.js: Truffle configuration file
6. Add the following Solidity smart contract (Greeter.sol) under your contracts directory. (TAKE Greeter.sol from the given github link)
7. Compile your smart contracts (greeter.sol) `truffle compile` (Make sure to use a 0.8 compiler version)
8. You should now see your contract’s ABIs under the build folder.
9. Add the following script (1_deploy.js from migrations folder from the given github link) [under your migrations folder](./migrations). This script tells Truffle how to deploy the Greeter.sol smart contract.

### Deploying to the Truffle Built-in Blockchain
1. Run `truffle develop`
2. Check the console output. See all the available accounts and their associated private keys.
3. Run `migrate` to deploy the Greeter contract.


### Folder structure

1. `build` - This folder contains build files of the smart contracts present in the contracts folder. These files are necessary to deploy the contracts on the blockchain network.
2. `contracts` - This folder contains the contracts which are to be deployed on the blockchain network. Here, you can find the smart contract source code of the Greeter contract.
3. `migrations` - This folder contains migration files in the form of JavaScript modules. These files are used to deploy the contracts to the blockchain network. The order of deployment of the contracts is defined by the migration files.
4. `test` - This folder contains test files for the contracts present in the contracts folder. These files are used to test the contracts to ensure that they function the way they are intended to.
5. `.gitignore` - This file specifies the files and folders which will be ignored by Git. It prevents certain files from being tracked by Git when changes are made to the repository.
6. `package-lock.json` - This file is automatically generated when you install packages via npm. It ensures that packages are installed with the same versions across different machines.
7. `package.json` - This file contains information about the project such as the project name, version, and dependencies. It also contains the scripts that can be run using npm.
8. `truffle-config.js` - This file contains the configuration details for the Truffle deployment process, such as the network settings, compiler settings, and other essential settings needed for deploying the contracts on the blockchain.
