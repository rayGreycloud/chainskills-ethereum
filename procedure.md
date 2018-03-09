# Procedure

## Genesis block creation 
### CLI > puppeth
* Specify network name> MyNetworkName
* What would you like to do? 2. Configure new genesis 
* Which consensus engine? 1. Ethash - proof-of-work
* Which accounts..? 0x (default)
* chain/network ID> 4224
* Choose: 2. Manage existing genesis 
* Choose: 2. Export genesis configuration
* Which file save genesis into? (default)

## Initialize private node 
CLI > geth --datadir . init ChainSkills.json

## Create accounts 
CLI > geth --datadir . account new  
Passphrase: pass1234  

## Account list 
geth --datadir . account list 

## Run cmd script file
D:\code\arbogast-ethereum\ChainSkills\private> ./startnode.cmd

## Attach new console  
In 2nd PowerShell terminal:  
D:\code\arbogast-ethereum\ChainSkills> geth attach ipc:\\.\pipe\geth.ipc 

## commands 
eth.accounts  
eth.coinbase  
eth.getBalance(eth.coinbase)
web3.fromWei(eth.getBalance(eth.accounts[0])) 

eth.sendTransaction({from:eth.coinbase, to:eth.accounts[1], value:web3.toWei(10,"ether")})
