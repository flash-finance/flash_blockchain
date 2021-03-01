# Flash_BlockChain
how to interact with ethereum、hecochain、binance smart chain and okex chain, including their smart contracts

# 1.Ethereum(Infura、JSON-RPC、Kavan)

## 1.1 查询当前区块高度(eth_blockNumber)

**Request** :

```shell script
curl https://kovan.infura.io/v3/your-project-id \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_blockNumber","params": [],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x16971db"
}
```

## 1.2. 查询当前gas价格(eth_gasPrice)

**Request** :

```shell script
curl https://kovan.infura.io/v3/your-project-id \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_gasPrice","params": [],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x218711a00"
}
```

## 1.3. 查询账户eth余额(eth_getBalance)

**Request** :

```shell script
curl https://kovan.infura.io/v3/your-project-id \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_getBalance","params": ["0x5bbF0971382Faa31ca55e74D89875a1F1531311e", "latest"],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x82178fc0fd8ce35"
}
```

## 1.4. 查询智能合约代币余额(eth_call)
UNI Token: 
0x1f9840a85d5aF5bf1D1762F925BDADdC4201F984

**Request** :

```shell script
curl https://kovan.infura.io/v3/your-project-id \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_call","params": [{"to": "0x1f9840a85d5aF5bf1D1762F925BDADdC4201F984","data": "0x70a082310000000000000000000000005bbF0971382Faa31ca55e74D89875a1F1531311e"}, "latest"],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x00000000000000000000000000000000000000000000000017959a3b65cd8d9c"
}
```


# 2. HecoChain(JSON-RPC、TestNet)

## 2.1. 查询当前区块高度(eth_blockNumber)

**Request** :

```shell script
curl https://http-testnet.hecochain.com \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_blockNumber","params": [],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x26c567"
}
```

## 2.2. 查询当前gas价格(eth_gasPrice)

**Request** :

```shell script
curl https://http-testnet.hecochain.com \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_gasPrice","params": [],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x3b9aca00"
}
```

## 2.3. 查询账户ht余额(eth_getBalance)

**Request** :

```shell script
curl https://http-testnet.hecochain.com \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_getBalance","params": ["0x5bbF0971382Faa31ca55e74D89875a1F1531311e", "latest"],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x14ce1bda7292d600"
}
```

## 2.4. 查询智能合约代币余额(eth_call)
DAI Token: 
0x60d64Ef311a4F0E288120543A14e7f90E76304c6

**Request** :

```shell script
curl https://http-testnet.hecochain.com \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_call","params": [{"to": "0x60d64Ef311a4F0E288120543A14e7f90E76304c6","data": "0x70a082310000000000000000000000005bbF0971382Faa31ca55e74D89875a1F1531311e"}, "latest"],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x0000000000000000000000000000000000000000000000000000000000000000"
}
```


# 3. Binance Smart Chain(JSON-RPC、TestNet)

## 3.1. 查询当前区块高度(eth_blockNumber)

**Request** :

```shell script
curl https://data-seed-prebsc-1-s1.binance.org:8545 \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_blockNumber","params": [],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x65f4dd"
}
```

## 3.2. 查询当前gas价格(eth_gasPrice)

**Request** :

```shell script
curl https://data-seed-prebsc-1-s1.binance.org:8545 \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_gasPrice","params": [],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x4a817c800"
}
```

## 3.3. 查询账户bnb余额(eth_getBalance)

**Request** :

```shell script
curl https://data-seed-prebsc-1-s1.binance.org:8545 \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_getBalance","params": ["0x5bbF0971382Faa31ca55e74D89875a1F1531311e", "latest"],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x5698084a8c85c000"
}
```

## 3.4. 查询智能合约代币余额(eth_call)
USDC Token: 
0x64544969ed7EBf5f083679233325356EbE738930

**Request** :

```shell script
curl https://data-seed-prebsc-1-s1.binance.org:8545 \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_call","params": [{"to": "0x64544969ed7EBf5f083679233325356EbE738930","data": "0x70a082310000000000000000000000005bbF0971382Faa31ca55e74D89875a1F1531311e"}, "latest"],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x0000000000000000000000000000000000000000000000000000000000000000"
}
```

# 4. Okex Chain(JSON-RPC、TestNet)

## 4.1. 查询当前区块高度(eth_blockNumber)

**Request** :

```shell script
curl http://okexchaintest.okexcn.com:26659 \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_blockNumber","params": [],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x102979"
}
```

## 4.2. 查询当前gas价格(eth_gasPrice)

**Request** :

```shell script
curl http://okexchaintest.okexcn.com:26659 \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_gasPrice","params": [],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x3b9aca00"
}
```

## 4.3. 查询账户okt余额(eth_getBalance)

**Request** :

```shell script
curl http://okexchaintest.okexcn.com:26659 \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_getBalance","params": ["0x5bbF0971382Faa31ca55e74D89875a1F1531311e", "latest"],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x4561f9440b431800"
}
```

## 4.4. 查询智能合约代币余额(eth_call)
ETHK Token: 
0x5bbc340ed9503228bdb0f72d4e21579a151d55c4

**Request** :

```shell script
curl http://okexchaintest.okexcn.com:26659 \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_call","params": [{"to": "0x5bbc340ed9503228bdb0f72d4e21579a151d55c4","data": "0x70a082310000000000000000000000005bbF0971382Faa31ca55e74D89875a1F1531311e"}, "latest"],"id":1}'
```
**Response** :
```shell script
{
    "jsonrpc":"2.0",
    "id":1,
    "result":"0x0000000000000000000000000000000000000000000000000477973a2100f9d1"
}
```