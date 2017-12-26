<p align=center>
<img src="https://raw.githubusercontent.com/bichenkk/coinmon/master/logo.png">
</p>
<p align=center>
<a target="_blank" href="http://nodejs.org/download/" title="Node version"><img src="https://img.shields.io/badge/node.js-%3E=_6.0-green.svg"></a>
<a target="_blank" href="https://opensource.org/licenses/MIT" title="License: MIT"><img src="https://img.shields.io/badge/License-MIT-blue.svg"></a>
<a target="_blank" href="http://makeapullrequest.com" title="PRs Welcome"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"></a>
</p>  

> 💰 Cryptocurrency price ticker CLI.

Check cryptocurrencies' prices, changes on your console.
Best CLI tool for those who are both **Crypto investors** and **Engineers**.

All data comes from [coinmarketcap.com](https://coinmarketcap.com/) APIs.

## Changes in this fork
- use .env variables to calculate current value of your coins in each currency

## Install

In order to use coinmon, make sure that you have [Node](https://nodejs.org/) version 6.0.0 or higher.
```
$ git clone https://github.com/bichenkk/coinmon.git
$ cd coinmon
$ yarn
$ npm install -g
$ npm link
$ coinmon
```
## Usage

To check the top 10 cryptocurrencies ranked by their market cap
```
$ coinmon
```

To store and calculate the value of your investment in each applicable currency, create an .env file in the root of the coinmon folder and enter a coin/amount mapping, like so

.env
```
BTC=1.5
```

## Options

You can use the `-c` (or `--convert`) with the fiat currency symbol to find in terms of another currency.
The default currency is USD and it supports AUD, BRL, CAD, CHF, CLP, CNY, CZK, DKK, EUR, GBP, HKD, HUF, IDR, ILS, INR, JPY, KRW, MXN, MYR, NOK, NZD, PHP, PKR, PLN, RUB, SEK, SGD, THB, TRY, TWD, ZAR.

```
$ coinmon -c eur // convert prices to Euro
$ coinmon -c jpy // convert prices to Yen
```

You can use the `-f` (or `--find`) with coin symbol to search cryptocurrencies. You can add symbols seperated by comma. Credit to @maticrivo

```
$ coinmon -f btc // search coins included keyword btc
$ coinmon -f btc,eth // search coins included keyword btc or eth
```

You can use the `-t` (or `--top`) with the index to find the top n cryptocurrencies ranked by their market cap.

```
$ coinmon -t 50 // find top 50
$ coinmon -t 1000 // find top 1000
```

You can use the `-H` (or `--humanize`) with true / false to display market cap in different format. By default, the option is true and the market cap will be shown in humanized format. Credit to @pgilad

```
$ coinmon -H false // show market cap in full number like 136343835627
```

You can use the `-h` (or `--help`) to find all valid options of coinmon

```
$ coinmon -h
```

## Screenshot

<img src="https://raw.githubusercontent.com/bichenkk/coinmon/master/screenshot.png">



## License

MIT
