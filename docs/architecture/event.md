# Tron Event Subsystem

## Introduction

The TIP: [TIP-12: Tron event subscribes model](https://github.com/tronprotocol/TIPs/blob/master/tip-12.md).

TRON Event Subscription supports 4 types of event:

### Transaction Event

The parameters passed to Subscriber:

```
transactionId: transaction hash
blockHash: block hash
blockNumber: block number
energyUsage: energy usage
energyFee: energy fee
originEnergyUsage: origin energy usage
energyUsageTotal: total energy usage total
```

### Block Event

The parameters passed to Subscriber:

```
blockHash: block hash
blockNumber: block number
transactionSize: the number of transactions in a block
latestSolidifiedBlockNumber: the latest solidified block number
transactionList: the transactions hash list
```

### Contract Event

The parameters passed to Subscriber:

```
transactionId: transaction id
contractAddress: contract address
callerAddress: contract caller address
blockNumber: the number of the block contract related events recorded
blockTimestamp: the block time stamp
eventSignature: event signature
topicMap: the map of topic in solidity language
data: the data information in solidity language
removed: 'true' means the log is removed
```

### Contract Log Event

The parameters passed to Subscriber:

```
transactionId: transaction hash
contractAddress: contract address
callerAddress: contract caller address
blockNumber: the number of the block contract related events recorded
blockTimestamp: the block time stamp
contractTopics: the list of topic in solidity language
data: the data information in solidity language
removed: 'true' means the log is removed
```

Contract Event and Contract Log Even support event filter function which includes:

```
fromBlock: the start block number
toBlock: the end block number
contractAddress: contract adsresses list
contractTopics: contract topics list
```

!!! note
    Historical data query is not supported.

## New Features

1. Supporting event plug-ins, kafka & mongodb plug-ins have been released, developers can also customize their own plug-ins according to their own needs.
2. Supporting subscription of chain data, such as block, transaction, contract log, contract event and so on. For transaction events, developers can get information such as internal transactions, contract info and so on; for contract events, developers could configure the contract addresses list or contract topic list to receive the specified events, and event subscription has a very low latency. The deployed fullnode can receive event information immediately after the contract is executed.
3. Event query service tron-eventquery, online Event query service provided. Developers can query trigger information in the last seven days through https, and the query address is [https://api.tronex.io](https://api.tronex.io).

## Github project

- [tronprotocol/event-plugin](https://github.com/tronprotocol/event-plugin)
- [tronprotocol/tron-eventquery](https://github.com/tronprotocol/tron-eventquery)

### Event plugin

- [Kafka deployment](../developers/deployment.md#kafka)
- [MongoDB deployment](../developers/deployment.md#mongo)

### Event query

Tron Event Query Service

TronEventQuery is implemented with Tron's new event subscribe model. It uses same query interface with Tron-Grid. Users can also subscribe block trigger, transaction trigger, contract log trigger, and contract event trigger. TronEvent is independent of a particular branch of java-tron, the new event subscribes model will be released on version 3.5 of java-tron.

For more information of tron event subscribe model, please refer to [TIP-12](https://github.com/tronprotocol/TIPs/issues/12).

- [Event query deployment](https://tronprotocol.github.io/documentation-en/developers/deployment/#event-subscribe-plugin-deployment)
- [Event query HTTP API](https://github.com/tronprotocol/documentation-en/tree/master/docs_without_index/plugin/event-query-http.md)
