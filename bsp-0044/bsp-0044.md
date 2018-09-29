# BSP-0044 : Registered coin types for BIP-0044

```
Number:  BSP-0044
Title:   Registered coin types for BIP-0044
Type:    Standard
Status:  Draft
Authors: LuYong Chen (louie@bepal.pro)
Created: 2018-09-29
```

## Abstract

BIP-0044 defines a logical hierarchy for deterministic wallets.
Level 2 of the hierarchy describes a coin type in use.

## Motivation

Record the path BEPAL acknowledges

## Registered coin types

These are the registered coin types for usage in level 2 of BIP44 described in chapter "Coin type".

All these constants are used as hardened derivation.

index | hexa       | symbol | coin
------|------------|--------|-----------------------------------
0     | 0x80000000 | BTC    | [Bitcoin](https://bitcoin.org/)
1     | 0x80000001 |        | Testnet (all coins)
2     | 0x80000002 | LTC    | [Litecoin](https://litecoin.org/)
3     | 0x80000003 | DOGE   | [Dogecoin](https://github.com/dogecoin/dogecoin)
5     | 0x80000005 | DSH    | [Dash](https://github.com/dashpay/dash) (ex Darkcoin)
43    | 0x8000002b | XEM    | [NEM](https://github.com/NemProject)
52    | 0x80000034 | BTCD   | [Bitcoindark](https://github.com/jl777/btcd)
60    | 0x8000003c | ETH    | [Ether](https://ethereum.org/ether)
61    | 0x8000003d | ETC    | [Ether Classic](https://ethereumclassic.github.io)
135   | 0x80000087 | STEEM  | [Steem](http://steem.io)
144   | 0x80000090 | XRP    | [Ripple](https://ripple.com)
145   | 0x80000091 | BCH    | [Bitcoin Cash](https://www.bitcoincash.org)
153   | 0x80000099 | BTM    | [Bytom](https://bytom.io)
156   | 0x8000009c | BTG    | [Bitcoin Gold](http://www.btcgpu.org)
171   | 0x800000ab | HSR    | [Hcash](https://h.cash)
666   | 0x8000029a | ACT    | [Achain](https://www.achain.com/)
668   | 0x8000029c | SSC    | [SelfSell](https://www.selfsell.com/)
818   | 0x80000332 | VET    | [VeChain Token](https://vechain.com/)
888   | 0x80000378 | NEO    | [NEO](https://neo.org/)
999   | 0x800003e7 | BCD    | [Bitcoin Diamond](http://btcd.io/)
1000  | 0x800003e8 | BTN    | [Bitcoin New](http://bitcoinnew.org/)
2301  | 0x800008fd | QTUM   | [QTUM](https://qtum.org/en/)
2302  | 0x800008fe | ETP    | [Metaverse](https://mvs.org/)
2303  | 0x800008ff | GXC    | [GXChain](https://www.gxb.io)
2304  | 0x80000900 | SSC    | [SelfSell](https://www.selfsell.com)
2305  | 0x80000901 | ELA    | [Elastos](https://www.elastos.org/)
8888  | 0x800022b8 | SBTC   | [Super Bitcoin](https://www.superbtc.org)
8999  | 0x80002327 | BTP    | [Bitcoin Pay](http://www.btceasypay.com)
9888  | 0x800026a0 | BTF    | [Bitcoin Faith](http://bitcoinfaith.org)
9999  | 0x8000270f | GOD    | [Bitcoin God](https://www.bitcoingod.org)

Coin types will be added only if BEPAL wallet implementing BIP-0044 for desired coin.

## Libraries

* [BIP44-constants](https://www.npmjs.com/package/bip44-constants) ([source](http://github.com/bitcoinjs/bip44-constants)) JavaScript package with described coin types

## References

* [BIP-0044: Multi-Account Hierarchy for Deterministic Wallets](https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki)

* [slips-0044: Registered coin types for BIP-0044](https://github.com/satoshilabs/slips/blob/master/slip-0044.md)
