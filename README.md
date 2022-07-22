# NFTs 🌁

NFTs are different from ERC-20 tokens, such as DAI or LINK, in that each individual token is completely unique and is not divisible. NFTs give the ability to assign or claim ownership of any unique piece of digital data, trackable by using Ethereum's blockchain as a public ledger. An NFT is minted from digital objects as a representation of digital or non-digital assets. For example, an NFT could represent:

An NFT can only have one owner at a time. Ownership is managed through the uniqueID and metadata that no other token can replicate. NFTs are minted through smart contracts that assign ownership and manage the transferability of the NFTs. When someone creates or mints an NFT, they execute code stored in smart contracts that conform to different standards, such as ERC-721. This information is added to the blockchain where the NFT is being managed. The minting process, from a high level, has the following steps that it goes through:

- Creating a new block
- Validating information
- Recording information into the blockchain

NFT's have some special properties:

- Each token minted has a unique identifier that is directly linked to one Ethereum address.
- They're not directly interchangeable with other tokens 1:1. For example 1 ETH is exactly the same as another ETH. This isn't the case with NFTs.
- Each token has an owner and this information is easily verifiable.
- They live on Ethereum and can be bought and sold on any Ethereum-based NFT market.

**ROYALTIES**

Some NFTs will automatically pay out royalties to their creators when they're sold. This is still a developing concept but it's one of the most powerful. For example, the original owners of [EulerBeats Originals](https://eulerbeats.com/)
 earn an 8% royalty every time their NFT is sold. And some platforms, like [Foundation](https://foundation.app/)
 and [Zora](https://zora.co/)
 support royalties for their artists.

**ENS**

The Ethereum Name Service uses NFTs to provide your Ethereum address with an easier-to-remember name like mywallet.eth. This means you could ask someone to send you ETH via mywallet.eth rather than 0x123456789......

This works in a similar way to a website domain name which makes an IP address more memorable. And like domains, ENS names have value, usually based on length and relevance. With ENS you don't need a domain registry to facilitate the transfer of ownership. Instead, you can trade your ENS names on an NFT marketplace.

Your ENS name can:

- Receive cryptocurrency and other NFTs.
- Point to a decentralized website, like [ethereum.eth](https://ethereum.eth.link/).
- Store any arbitrary information, including profile information like email addresses and Twitter handles.

### **The work in minting your NFT**

When you mint an NFT, a few things have to happen:

- It needs to be confirmed as an asset on the blockchain.
- The owner's account balance must be updated to include that asset. This makes it possible for it to then be traded or verifiably "owned".
- The transactions that confirm the above need to be added to a block and "immortalised" on the chain.
- The block needs to be confirmed by everyone in the network as "correct". This consensus removes the need for intermediaries because the network agrees that your NFT exists and belongs to you. And it's on chain so anyone can check it. This is one of the ways Ethereum helps NFT creators to maximise their earnings.

All these tasks are done by miners. And they let the rest of the network know about your NFT and who owns it. This means mining needs to be sufficiently difficult, otherwise anyone could just claim that they own the NFT you just minted and fraudulently transfer ownership. There are lots of incentives in place to make sure miners are acting honestly.

### **A greener Ethereum: Eth2**

Ethereum is currently going through a series of upgrades, known as Eth2, that will replace mining with [staking](https://ethereum.org/en/eth2/staking/). This will remove computing power as a security mechanism, and reduce Ethereum's carbon footprint by ~99.95%[1](https://ethereum.org/en/nft/#fn-1). In this world, stakers commit funds instead of computing power to secure the network.

The energy-cost of Ethereum will become the cost of running a home computer multiplied by the number of nodes in the network. If there are 10,000 nodes in the network and the cost of running a home computer is roughly 525kWh per year. That's 5,250,000kWh[1](https://ethereum.org/en/nft/#fn-1) per year for the entire network.

We can use this to compare Eth2 to a global service like Visa. 100,000 Visa transactions uses 149kWh of energy[2](https://ethereum.org/en/nft/#fn-2). In Eth2, that same number of transactions would cost 17.4kWh of energy or ~11% of the total energy[3](https://ethereum.org/en/nft/#fn-3). That's without considering the many optimisations being worked on in parallel to Eth2, like [rollups](https://ethereum.org/en/glossary/#rollups). It could be as little as 0.1666666667kWh of energy for 100,000 transactions.

### **Timelines**

The process has already started. [The Beacon Chain](https://ethereum.org/en/eth2/beacon-chain/), the first upgrade, shipped in December 2020. This provides the foundation for staking by allowing stakers to join the system. The next step relevant to energy efficiency is to merge the current chain, the one secured by miners, into the Beacon Chain where mining isn't needed. Timelines can't be exact at this stage, but it's estimated that this will happen sometime in 2022. This process is known as the merge (formerly referred to as the docking). 

## **Build with NFTs**

Most NFTs are built using a consistent standard known as [ERC-721](https://ethereum.org/en/developers/docs/standards/tokens/erc-721/). However, there are other standards that you might want to look into. The [ERC-1155](https://blog.enjincoin.io/erc-1155-the-crypto-item-standard-ac9cf1c5a226) standard allows for semi-fungible tokens which is particularly useful in the realm of gaming. And more recently, [EIP-2309](https://eips.ethereum.org/EIPS/eip-2309) has been proposed to make minting NFTs a lot more efficient. This standard lets you mint as many as you like in one transaction!

# Miniting NFT

```
mkdir elonNFT
cd elonNFT
npm init --yes
npm install --save-dev hardhat
npx hardhat
```

We will follow the guide and create a basic sample project. Something like HelloWorld! Just follow through the questions and answer them yes.

You will also install some more dependencies; hardhat ether and hardhat waffle in the project. The installation wizard will install those for you. If you haven’t received a prompt for that, run the following command:

```
npm install --save-dev @nomiclabs/hardhat-ethers ethers @nomiclabs/hardhat-waffle ethereum-waffle chai
```

We will also install a smart contracts library called OpenZeppelin. It will make it easy for us to develop, run and ship smart contracts.

```jsx
npx hardhat run scripts/sample-script.js
```

you've been successful in deploying your first smart contract to your local blockchain environment without having to code a single line. 😅 When you run the above command, your solidity code is converted into bytecode. A new local blockchain is created and your contract is deployed there. But this blockchain is not permanent, every time you build and run your smart contract, a new blockchain is created in your local environment and the contract is deployed. So it is more like a clean slate - start from scratch. We will get back to it later and figure out a way to deploy our contract permanently. For now, just a piece of information for you to digest.

Also the above long line of numbers is the address where your contract is deployed. Every contract has its own address. Because of hardhat we were able to create a local blockchain environment just like Ethereum where we can deploy contracts and play around with them free of cost.

Let's open your project in VSCode or Sublime or any other IDE your prefer

Do open the Greeter.sol file. The Greeter.sol is a contract written in Solidity and it is a very basic one

A constructor where we can pass a string type variable called _greeting. In our case, we passed Hello HardHat!. This is why we saw ‘Hello HardHat!’ on the terminal.
A function greet() which returns the greeting value. It is a readonly function. It just returns the current value of greeting variable.
A function setGreeting() where we can set the value of the greeting message. After deploying the contract, we can call this function to change the value of greeting.

Now let’s open the sample-script.js in the scripts folder. Hardhat always runs the compile task when running scripts with its command line interface. If this script is run directly using 'node' you may want to call compile manually to make sure everything is compiled.

****Creating an Elon Musk NFT locally****

In the contracts folder, create a new file named Elon.sol. This is your new contract file. 

```jsx
// SPDX-License-Identifier: UNLICENSED

pragma solidity ^0.8.0; //this is the version of the solidity we are using in this contract.

import "hardhat/console.sol"; //this is given to us by hardhat to debug our code. It is very helpful in local environment.

contract ElonNFT { 
	
	//this is our NFT contract and it has a constructor. As soon as the contract is deployed, the constructor is called and we will see a message on 
	//terminal. All thanks to the console log. 
	
    constructor() {
        console.log("This is my Elon Musk NFT contract!!");
    }
}
```

Now let's edit our scripts file to call this a contract. Also, you should know that for every contract you write, you must create a different contract file. This is the general convention used, it makes easy to manage the code and avoid coding mishaps!

First things first, I will rename the sample-script.js file to run.js and then I will make some changes to the file.

```jsx
const hre = require("hardhat");

async function main() {
  // We get the contract to deploy
  const ElonNFT = await hre.ethers.getContractFactory("ElonNFT");
  const elon = await ElonNFT.deploy();

  await elon.deployed();

  console.log("ElonNFT deployed to:", elon.address);
}

// We recommend this pattern to be able to use async/await everywhere
// and properly handle errors.
main()
  .then(() => process.exit(0))
  .catch((error) => {
    console.error(error);
    process.exit(1);
  });
```

****🍩 Minting an NFT****

OpenZeppelin is a reusable and secure smart contracts library, which means that you can import this library, inherit the contracts in your project and get started without having to worry about security issues and reinventing the wheel.

Since we had already created the Elon.sol file. We will just update it. Don't worry if you don't get anything. Just copy-paste it and I will explain it step by step.

```

// SPDX-License-Identifier: UNLICENSED

pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC721/extensions/ERC721URIStorage.sol";
import "@openzeppelin/contracts/utils/Counters.sol";
import "hardhat/console.sol";

contract ElonNFT is ERC721URIStorage {
   using Counters for Counters.Counter;
   Counters.Counter private _tokenIds;

   constructor() ERC721("ElonMusk", "ELON") {}

   function mintNFT()
       public
       returns (uint256)
       {
           _tokenIds.increment();
           uint256 newItemId = _tokenIds.current();
           _mint(msg.sender, newItemId);
           _setTokenURI(newItemId, "Hello World");
           console.log("The NFT ID %s has been minted to %s", newItemId, msg.sender);
           return newItemId;
       }
}
```

Here we are importing ERC721URIStorage contract, this contract contains ERC721 contracts. The metadata part of the NFT contract needs to be stored somewhere. so we are using an extension of base ERC721 contract which can have URI storage.

We are also importing a library called Counters.sol. This is also an OpenZeppelin utility to keep track of NFTs which are to be minted. Let's say our contract has minted 5 NFTs, and now someone makes a call to the contract to mint another NFT. How does the contract keep track that it's the 6th NFT? This happens via this utility.

## Adding image to NFT

Every NFT has some data linked to it in the form of JSON format that describes the NFT. We call it metadata. This metadata has a special JSON format and the format needs to be followed if we want our NFT to appear properly on platforms like OpenSea, Rarible, etc.

In the previous lesson, I shared how we wrote ‘Hello World’ instead of sharing the Uniform Resource Identifier, I mean, the data about the NFT. 😅

Now we will use the standard format required by NFT platforms to describe the data related to the NFT.

```

{
	"name":"Elon Musk",
	"description":"Making inter planetory travel possible and pushing the boundaries for mankind.",
	"image":"https://64.media.tumblr.com/242f308aee595552a0898e11b4bfb9a3/tumblr_pe1d49XUHB1tsqz3b_1280.jpg",

	"attributes":
	[
		{
			"trait_type":"Zodiac","value":"Cancer"
		},
		{
			"trait_type":"Height","value":"6'1"
		},
		{	"trait_type":"Personality Type","value":"INTJ"
		}
	]
}
```

I will use the [jsonkeeper](https://jsonkeeper.com/) website to convert my JSON into linkable URL. Here is the url: [https://jsonkeeper.com/b/JJJS](https://jsonkeeper.com/b/JJJS)

💁‍♀️ I will recommend you to keep your image hosted somewhere safe, the image can't be altered and it doesn't incur you costs. I am being lazy here and found a website where an image was already hosted. Please never do this for your real NFTs. If your server is down or compromised, the NFT will lose its value and important data.

***As NFTschool describes it,***

"When an NFT is created and linked to a digital file that lives on some other system, *how* the data is linked is critical. There are a few reasons why traditional HTTP links aren't a great fit for the demands of NFTs.

With an HTTP address like https://cloud-bucket.provider.com/my-nft.jpg, anyone can fetch the contents of my-nft.jpg, as long as the owner of the server pays their bills. However, there's no way to guarantee that the contents of my-nft.jpg are the same as they were when the NFT was created. The server owner can easily replace my-nft.jpg with something different at any time, causing the NFT to change its meaning.

This problem was demonstrated by an artist who [pulled the rug (opens new window)](https://cointelegraph.com/news/opensea-collector-pulls-the-rug-on-nfts-to-highlight-arbitrary-value) on NFTs he created by changing their images after they were minted and sold to others."

Coming back, we will pass on the JSON metadata url and deploy our contract.

```

_setTokenURI(newItemId, "https://jsonkeeper.com/b/JJJS");
```

****🚀 Launching your NFT on testnet****

There are three environments for a blockchain network: mainnet, devnet, and testnet.

