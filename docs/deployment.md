# Liquid Democracy Deployment

This document outlines the steps to run liquid democracy app on your own local network. 


## Steps 

1. Download Ethereum Wallet from this link and install on your machine. Make sure that this is this version or with newer version some syntax changes in the contract are required. https://github.com/ethereum/mist/releases/tag/v0.8.10
1. Install node.js and follow the steps to install keytherum.js node
1. Install web3 libraries 
1. Runt geth on your machine with following command. This will create your own node and allow you on executing certain calls. Replace --datadir "some folder" with a folder name on your machine. 
`geth --rpc --rpcaddr="0.0.0.0"  --datadir "some folder" --port 30301 --rpcport 8545 --networkid 999 --rpccorsdomain="*" --rpcapi="db,eth,net,web3,personal,web3"`
1. Run node with following file. You will also need to update addresses in that file to your Ethereum address. 
`https://github.com/fractastical/breathe/blob/master/node/userRegistration.js`
1. Deploy contract using Ethereum Wallet which is found here. Copy address of this contract, you will need it when deploying second contract. 
`https://github.com/fractastical/breathe/blob/master/sol/SimpleToken.sol`
1. Deploy contract using Ethereum Wallet which is found here. Use address from previous contract as input when deploying it. 
`https://github.com/fractastical/breathe/blob/master/sol/DSociety.sol`
1. Update addresses of these two contracts in this file. 
`https://github.com/fractastical/breathe/blob/master/dist/js/interface.js`
1. Run local web server to be able to resolve location stored in file in step 8)
1. Now run the app 
`https://github.com/fractastical/breathe/blob/master/pages/index.html`

If you have more questions contact me at bogdanfiedur@gmail.com 
