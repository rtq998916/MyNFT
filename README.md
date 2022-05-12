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
Remember this address. We will use it later.

You can see the transaction on [Etherscan](https://etherscan.io/txs)

It will be something like this:
![Etherscan](https://github.com/rtq998916/MyNFT/blob/main/images/Etherscan.png)

The contract is now successfully deployed!

### Mint your NFT
You will need the alchemy library to interact with their API. Therefore, you should install this.

Run this in the command line:
```
npm install @alch/alchemy-web3
```
Remember the contract address in the previous part? Now paste it into the right position of the mint-nft.js file:
```
const contractAddress = "Your contract address";
```
Replace the "Your contract address" with the address you copied.

You now mint your NFT by running the mint-nft script in your terminal.

Run this in your terminal:
```
node scripts/mint-nft.js
```
If you followed all the steps correctly, you should receive a “Transaction receipt”. It will look something like this:
![transaction receipt](https://github.com/rtq998916/MyNFT/blob/main/images/transaction%20receipt.png)
You can also check the transaction on [Etherscan](https://etherscan.io/txs).

### View your NFT
You can download the Metamask app on your mobile phone and choose the Rinkeby Test Network, then press "import NFT". Paste the contract address, refresh a few times and your NFT will appear in your account!
![NFT in account](https://github.com/rtq998916/MyNFT/blob/main/images/NFT%20in%20account.jpg)

## Notice
This is the DAPP and NFT we created for demonstration. Please feel free if you want to:
### Use other test networks
There are many other networks available, many of them are test networks, such as Ropsten, Kovan...etc. You can easily get some test tokens on them. Of course, you can also use the mainnet!

### Create your own DAPP API URL
Feel free to create your own DAPP on [Alchemy](https://www.alchemy.com/)

### Create your own NFTs
It is easy to upload and make your own NFTs on [Pinata](https://www.pinata.cloud/)
