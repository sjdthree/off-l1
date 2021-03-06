# 🐰 Off L1

![](./hero.png)

1 click cross chain Uniswap clone arbitrage app.

- [Explainer video](https://www.youtube.com/watch?v=LELEh4aOzM4&)
- [Slide](https://speakerdeck.com/makoto_inoue/off-l1)
- [Demo site](http://surge.xyz)

## How to set up

```
git clone https://github.com/makoto/off-l1
cd  off-l1/packages/react-app
yarn
yarn start
```

## Chains and exchanges supported

- [PancakeSwap](https://pancakeswap.finance) on [Binance Smart Chain](https://www.binance.org/en/smartChain)
- [QuickSwap](https://quickswap.exchange) on [Matic/Polygon](https://polygon.technology)
- [HoneySwap](http://honeyswap.org) on [xDAI](https://www.xdaichain.com)

## API used

- [Connext](https://connext.network/) = State channel based cross chain bridge technoloy.
- [TheGraph](https://thegraph.com/) to call each chain's token prices
- [Web3 Modal]() = to allow you to connect via Metamask, Walletconnect, and Portis. WARNING: Do you access via smartcontract based wallet like Argent and Gnosis safe, as their wallet address is not compatible across different chains.
- [Portis](https://portis.io/) = Portis supports both xDAI and Matic (not BSC yet). To connect to the specific chain, go to the swap page (/exchange/*), then disconnet/connect
- [BitQuery](https://bitquery.io/) = To show transaction history of Binance smart chain
- [Covalent](https://www.covalenthq.com) = To show transaction history of Matic

## TODO

### Short term

- Add tranaction link when the entire swap is complete
- Add ability to recover stuck fund from [UniswapWithdrawHelper](https://github.com/connext/vector-withdraw-helpers/blob/main/contracts/UniswapWithdrawHelper/UniswapWithdrawHelper.sol)
- Add xDAI - DAI token mapping
- Add Token transfer history for xDAI
- Use USDC as base price (to replace out of sync Pancake subgraph)
- Allow user to switch base currency
- Support Multi paths (eg: USDC-> BNB ->UNI)
- Add historical quotes for each pair

### Mid-longer term

- Turn it into bot
- Support more exchanges on different chains
- Send back the swapped token back to original chain.
- Split quote into muliple smaller trades across chains
- Investigate the possibility of forming a pooled fund for profit sharing

## Credits

Special thanks to [Rahul Sethuram](https://twitter.com/rhlsthrm) for the tireless support as well as actively contributing to the project