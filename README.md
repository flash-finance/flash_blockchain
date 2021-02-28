# Flash_BlockChain
how to interact with ethereum、hecochain and binance smart chain, including their smart contracts

# Ethereum(Infura、JSON-RPC、Kavan)

## 1. 查询当前区块高度(eth_blockNumber)

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

## 2. 查询当前gas价格(eth_gasPrice)

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

## 3. 查询账户eth余额(eth_getBalance)

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

## 4. 查询智能合约代币余额(eth_call)
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


# HecoChain(JSON-RPC、testNet)

## 1. 查询当前区块高度(eth_blockNumber)

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

## 2. 查询当前gas价格(eth_gasPrice)

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

## 3. 查询账户ht余额(eth_getBalance)

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

## 4. 查询智能合约代币余额(eth_call)
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