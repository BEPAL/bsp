# BSP-0021 : 收款码

```
编号:  BSP-0021
标题:  收款码标准
层级:  应用层
类型:  标准协议
状态:  草稿
作者:  陈鲁勇 <louie@bepal.pro>
创建时间: 2018-09-28
```

## 简介

该BSP提出了用于进行币种支付的URI方案。

根据URI RFC3986标准，规定的URI的一般格式。使用UTF-8字符集来表示

## 动机

此URI方案的目的是使用户只需单击网页上的链接或扫描QR码即可轻松进行付款。

BIP开源社区不希望存储与比特币无关的键值，所以我们希望BSP能成为承载这一切的主体。

## 详情


1. 根据币种，生成文本格式的收款参数字符串
2. 将文本字符串进行URLEncoder，编码格式选择UTF-8
3. URLEncoder后的文本生成收款二维码

采用类URL 格式，各主流币种格式如下：


**币种名:地址?键=值&键=值&...&键=值**

## 示例

地址：
```
bitcoin:175tWpb8K1S7NmH4Zx6rewF9WQrcZv245W
```

请求转入20.30比特币:

```
bitcoin:175tWpb8K1S7NmH4Zx6rewF9WQrcZv245W?amount=20.3
```

请求转入20.30比特币到标签为louie地址上：

```
bitcoin:175tWpb8K1S7NmH4Zx6rewF9WQrcZv245W?label=louie&amount=20.3
```

必须遵循正确的URI编码


## 注册URI键名

|  编号 | 键名  | 说明  |
| :---: | :---: | :---: |
| 1 | amount | 收款金额 |
| 2 | value | 收款数值（该数值不应包含小数点） |
| 3 | decimal | 小数点位数 |
| 4 | contractAddress | 合约标记地址 |

## 注册币种名

为公链注册币种名称

|  币种编号 | 币种符号  | 币种全称  |
| :---: | :---: | :---: |
|  0 |  BTC | [bitcoin](https://bitcoin.org/) |
|  2 |  LTC | [litecoin](https://litecoin.org/) |
|  5 |  DSH | [dash](https://www.dash.org/) |
|  60 |  ETH | [ethereum](https://ethereum.org/) |
|  61 |  ETC | [ethereumclassic](https://ethereumclassic.github.io/) |
|  145 |  BCH | [bitcoincash](https://www.bitcoincash.org/) |
|  153 |  BTM | [bytom](https://bytom.io/) |
|  194 |  EOS | [eos](https://eos.io/) |
|  2301 |  QTUM | [qtum](https://qtum.org/) |
|  2303 |  GXC | [gxchain](https://www.gxb.io/) |
|  2304 |  SSC | [selfsell](https://www.selfsell.com/) |


## 引用

[bip-0021.mediawiki - URI方案](https://github.com/bitcoin/bips/blob/master/bip-0021.mediawiki)

[slip-0044.md - 币种类型注册](https://github.com/Bepal/slips/blob/master/slip-0044.md)

[bip-0072.mediawiki - 支付协议的uri扩展](https://github.com/bitcoin/bips/blob/master/bip-0072.mediawiki)



