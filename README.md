# zSwap

A DEX and DeFi system that runs entirely on the blockchain. Deployed as [ERC-8244](https://eip.tools/eip/8244) onchain HTML.

The frontend code and routing is handled by smart contracts that prepare wallet calldata based on intents within a simple UI.

Features:
- Swap aggregation sourced from liquid AMMs (Uniswap, Curve, SushiSwap, etc).
- Hybrid routing (swaps select best output from AMMs and orderbooks, splits).
- ERC20 token launches with creator fees & one-sided liquidity bootstrapping.
- Precision pool AMM with ERC20 LP shares over bound ranges with simple hooks.
- ETH/ERC20/ERC721 (NFT) orderbooks with orders rendered as onchain SVG NFTs.
- Dynamic dutch orders and climbing bids. Partial fills. Private or open.
- Time-delayed ETH & ERC20 token payments ([SLOW protocol](https://0x000000000000888741b254d37e1b27128afeaabc.w4eth.io/)) and swap-to-pay.
- ERC20 token approval abstraction through waterfall (Permit/Permit2/[ERC-5792](https://eips.ethereum.org/EIPS/eip-5792)).
- Native onchain token listing via TCR managed by DAO shares bonded to NFTs.

Gateways:
- [zSwap.wei.domains](https://zswap.wei.domains/)
- [zSwap.wei.limo](https://zswap.wei.limo/)
- [zSwap.wei.is](https://zswap.wei.is/)
  
- 0x[version or resolver deployment].w3eth.io
- 0x[version or resolver deployment].w4eth.io

e.g., [0x000000e7dad6128683d1fb415e80b30c23dab7ac.w4eth.io/](https://0x000000e7dad6128683d1fb415e80b30c23dab7ac.w4eth.io/)

zSwap works with [ERC-4804](https://eips.ethereum.org/EIPS/eip-4804) and [ERC-5219](https://eips.ethereum.org/EIPS/eip-5219) for increased compatibility with other ethereum gateway and resolvers.

Name services:
- [ENS](https://app.ens.domains/)
- [WNS](http://wei.domains/)
- [GNS](http://gwei.domains/)

Swap outputs can be addressed to multiple [Ethereum name services](https://www.npmjs.com/package/@1001-digital/ethereum-names). 

Reverse-resolution also supported in-dapp and renders onchain for orderbook cards.

## Deployments

resolver: [0x000000E7DAD6128683D1fb415e80B30c23dAb7AC](https://etherscan.io/address/0x000000e7dad6128683d1fb415e80b30c23dab7ac#code)

Resolves and serves updated zSwap instance automatically to [zSwap.wei](zSwap.wei.limo) after 3-day cooldown for security and adjustments.

The DAO ([zOrg](https://zfi.wei.is/dao/#/dao/1/0x5E58BA0e06ED0F5558f83bE732a4b899a674053E)) holds the keys and sends updated bytecode payloads through the root `deployNext()`. Token-weighted voting.

# v0.1 (root)
[0x00000095643CFfA7D9fae407a84dfCB6406456c6](https://etherscan.io/address/0x00000095643CFfA7D9fae407a84dfCB6406456c6#code)

# v0.2 
[0xe686952842627A2cf81DF42CCaD54ef98046DB8D](https://etherscan.io/address/0xe686952842627A2cf81DF42CCaD54ef98046DB8D#code)

* [WalletConnect](https://walletconnect.com/) and mobile support
* Launched tokens now appear in dedicated dropdown section (ranked by liquidity)
* Improved deep-linking support for swaps and payments and swap-to-pay
* Various UI stability and design improvements
