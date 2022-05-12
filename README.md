# MyNFT
ELEN6883 final project

## 1.Environment

hardhat

openzeppelin

dotenv

Ether.js library

Rinkeby Test Network

## 2.How to run
### Connect your Metamask to this project
First you need a Metamask account to start. Copy your public and private keys, then paste them into the right position of the .env file.

### Install the openzeppelin
Clone the repository and open it with an IDE you like(Visual Studio Code is recommended). Make sure you hve installed hardhat. Open a terminal and run the following in the command line:

```
npm install @openzeppelin/contracts
```
This will install the openzeppelin library in your folder. You will need these classes later.

### Install Ether.js
Run the following command in the command line:
```
npm install --save-dev @nomiclabs/hardhat-ethers "ethers@^5.0.0"
```
### Compile the contract
The contract will be compiled by calling the "compile" task

Run the following code in command line:
```
npx hardhat compile
```
### Deploy the contract
Run the folowing in command line:
```
npx hardhat run scripts/deploy.js --network rinkeby
```
You should see the following sresult but with a different address:
```
Contract deployed to address: 0x81c587EB0fE773404c473DFQDCQ1327C470eED
```
You can see the transaction on [Etherscan](https://etherscan.io/txs)
