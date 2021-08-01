# Supply chain & data auditing - Project write-up

## Libraries used? Include why these libraries

```
"devDependencies": {
    "lite-server": "2.4.0",
    "truffle-hdwallet-provider": "^1.0.17"
}
```

## IPFS used? Include how IPFS is used in this project

N/A as IPFS was not used for this project

## Program version numbers

| Program | Version |
|---|---|
| Node | v16.3.0 |
| web3 | v1.4.0 |
| Truffle | v4.1.14 |
| Solidity | v0.4.24 |

## Contract Address
Rinkeby contract address is: [0xf3c87c4ad6278660eab5c354c9f179aa52d8d9cd](https://rinkeby.etherscan.io/address/0xf3c87c4ad6278660eab5c354c9f179aa52d8d9cd)

```
Using network 'development'.

Running migration: 1_initial_migration.js
  Deploying Migrations...
  ... 0x3ec86b4e991fedf210c2b8778dca4f095ccdf0f2a537d65675e4e19bcf467ba7
  Migrations: 0xb067b77f3d01d9202bf4f65406b0e314ddb2cece
Saving successful migration to network...
  ... 0x01f52fb27e59a270c0033d56a11798ff36f595ed4dfcd37ca0d9eb73337f69a1
Saving artifacts...
Running migration: 2_deploy_contracts.js
  Deploying FarmerRole...
  ... 0x1b1dd54010d7d16ce0421c2d9dca35c8f6eaf968f477ef1f6f0b34bc041adbf7
  FarmerRole: 0xa4722696eeac5b2238ee76890ca6c8e29829bfd1
  Deploying DistributorRole...
  ... 0x7b53e3ccbc040c2dfb011b7c8717dcb632621e69379fbc0a6edcd39295ca98d3
  DistributorRole: 0xb1a717d1783462d9547f972231fd5f7edd59e60d
  Deploying RetailerRole...
  ... 0xc5a0035c63c3bd741625e611394e68a1e5e2a7ce3b013ce5e6730891fe9457ce
  RetailerRole: 0xe3b1044730bc139662efc2ec16b67a3d08a77144
  Deploying ConsumerRole...
  ... 0x9124a72f491bb532580386840bf43410a6b336cffe04511ae9669508d9106aaa
  ConsumerRole: 0x04551329ea0f114947c61dde0bc8e39a75b6638c
  Deploying SupplyChain...
  ... 0x247bc0a15b09089854ce5f6c6c531d2bfc741997d02ab043635bb930d1f9bf94
  SupplyChain: 0xce76cda9ffea4f74069734fbd813b0f553d94609
Saving successful migration to network...
  ... 0x86925fe74eedfcbefd6944f1eb2460947d355d1a0378d61ec6bb25dcfd3e3dc9
Saving artifacts...
```

## Testing
```
truffle test
```

Resulting in 10 passing test

```
Using network 'development'.

ganache-cli accounts used here...
Contract Owner: accounts[0]  0x27d8d15cbc94527cadf5ec14b69519ae23288b95
Farmer: accounts[1]  0x018c2dabef4904ecbd7118350a0c54dbeae3549a
Distributor: accounts[2]  0xce5144391b4ab80668965f2cc4f2cc102380ef0a
Retailer: accounts[3]  0x460c31107dd048e34971e57da2f99f659add4f02
Consumer: accounts[4]  0xd37b7b8c62be2fdde8daa9816483aebdbd356088


  Contract: SupplyChain
    ✓ Testing smart contract function harvestItem() that allows a farmer to harvest coffee (168ms)
    ✓ Testing smart contract function processItem() that allows a farmer to process coffee (66ms)
    ✓ Testing smart contract function packItem() that allows a farmer to pack coffee (64ms)
    ✓ Testing smart contract function sellItem() that allows a farmer to sell coffee (66ms)
    ✓ Testing smart contract function buyItem() that allows a distributor to buy coffee (69ms)
    ✓ Testing smart contract function shipItem() that allows a distributor to ship coffee (65ms)
    ✓ Testing smart contract function receiveItem() that allows a retailer to mark coffee received (78ms)
    ✓ Testing smart contract function purchaseItem() that allows a consumer to purchase coffee (73ms)
    ✓ Testing smart contract function fetchItemBufferOne() that allows anyone to fetch item details from blockchain
    ✓ Testing smart contract function fetchItemBufferTwo() that allows anyone to fetch item details from blockchain


  10 passing (932ms)

```