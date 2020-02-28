# GO ASC
ASC Mainnet User Manual


## Steps

### 1. Run docker container
Install latest distribution of [Go](https://golang.org "Go") if you don't have it already.  
`# sudo apt-get install -y build-essential`  

### 2. Compile source code
`# cd /usr/local/src`  
`# git clone https://github.com/ascchain/AdanosChain_src.git`  
`# cd AdanosChain_src`  
`# make`  
`# ./build/bin/gasc version`  

### 3. Deploy
`# mkdir -p /usr/local/src/AdanosChain_src/gasc_bin/` 
`# cd /usr/local/src/AdanosChain_src/gasc_bin/`  
`# cp ../build/bin/gasc ./bin/gasc`  
`# ./backend.sh`

### 4. Enter console
`# cd /usr/local/src/AdanosChain_src/gasc_bin/`  
`# ./bin/gasc attach ./data/gasc.ipc`

### 5. View information of the connected node
`# admin.peers`

### 6. Create account
`# personal.newAccount()`  
`# ******`  ---- Enter new account password  
`# ******`  ---- Confirm the new account password  

### 7. Mine
`# miner.start()`

### 8. Query
`# eth.getBalance(eth.coinbase)`

### 9. Unlock account
`# personal.unlockAccount(eth.coinbase)`

### 10. Transfer
`# eth.sendTransaction({from: eth.accounts[0], to: eth.accounts[1], value: web3.toWei(1)})`

### 11. Exit console
`# exit`

### 12. View log
`# cd /usr/local/src/AdanosChain_src/gasc_bin/`  
`# tail -f gasc.log`

### 13. Stop gasc
`# cd /usr/local/src/AdanosChain_src/gasc_bin/`  
`# ./stop.sh` 


## Acknowledgement
We hereby thank:  
· [Ethereum](https://www.ethereum.org/ "Ethereum")




