# Overview

This repository consists of an implementation of  "network democracy" as described in the Swarm Fund whitepaper and a proposal for a generic liquid democracy protocol that would be statebox-compatible, blockchain agnostic, and conform to theoretical advances in game theory and other fields.

## Protocol Spec

https://github.com/swarmfund/networkdemocracy/blob/master/docs/Liquid%20Democracy%20-%20Proposal.pdf

## Local deployment instructions

Download Ethereum Wallet from this link and install on your machine. Make sure that this is this version or with newer version some syntax changes in the contract are required. https://github.com/ethereum/mist/releases/tag/v0.8.10


Install node.js and follow the steps to install keytherum.js node

Install web3 libraries 

Runt geth on your machine with following command. This will create your own node and allow you on executing certain calls. Replace --datadir "some folder" with a folder name on your machine. 

geth --rpc --rpcaddr="0.0.0.0"  --datadir "some folder" --port 30301 --rpcport 8545 --networkid 999 --rpccorsdomain="*" --rpcapi="db,eth,net,web3,personal,web3"


Run node with following file. 
You will also need to update addresses in that file to your Ethereum address. 
node/userRegistration.js


Deploy contract using Ethereum Wallet which is found here. Copy address of this contract, you will need it when deploying second contract. 
../sol/SimpleToken.sol


Deploy contract using Ethereum Wallet which is found here. Use address from previous contract as input when deploying it. 
sol/DSociety.sol


Update addresses of these two contracts in this file. 
dist/js/interface.js

Run local web server to be able to resolve location stored in file in 8)

Now run the app ../pages/index.html




