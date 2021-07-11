# Mining Energy Usage

This repository contains all of the data and resources necessary to run the dashboard. The dashboard is a visual representation of Bitcoin and Ethereum mining energy costs compared with Ethereum 2.0 (Proof of Stake), the traditional banking system, gold mining and annual energy usage by country.

The aim of this project was to explore the cost of Bitcoin and Ethereum mining on the environment, whether the value outweighs the cost and if there is a better solution.

The findings show that a potential strategy to reduce the impact on the environment, is to use crypto currencies that use the Proof of Stake method as opposed to the Proof of Work method.

----
## Bitcoin and Ethereum energy usage in TWh and $USD
----
![Chart](Png/energy_usage_twh.png)
![Chart](Png/energy_usage_usd.png)
* That little flat green line running parrallel with the bottom of the chart is ETH 2.0 energy usage.
* It uses so little energy compared to Proof of Work mining that it appears this like a flat line, we are comparing less than 1 TWh with over 100 TWh.
* In the energy consumption in USD chart we are comparing $1.3 million dollars with billions of dollars in electricity.
* Ethereum once switched to PoS will use 99.95% less energy than Ethereum in its current state

* Bitcoin currently uses around 6.7 billion USD in energy per year and its current marketcap sits at 865 billion USD - mkt cap to cost of operation ratio = 0.007, in other words the current market cap of Bitcoin could power the protocol for 129 years

* Ethereum currently uses around 2.7 billion USD in energy per year and its currentl marketcap sits at 369 billion USD - mkt cap to cost of operation ratio = 0.007 (coincidence), in other words the current marketcap of Ethereum could power the protocol for 136 years

* Ethereum 2.0 currently uses around 1.3 million USD in energy per year - mkt cap to cost of operation ratio = 0.000003, in other words the current market cap of Ethereum could power the Ethereum PoS protocol for 276,923 years

It's very hard to say what kind of financial impact the total sum of the Bitcoin or Ethereum network has on the world but it's still worth making the comparison to get some idea of how much value it adds and at what cost.

----
## Bitcoin hashrate 
----
![Chart](Png/btc_hashrate.png)
----
## Bitcoin revenue per hash in $USD
----
![Chart](Png/btc_rev_hash.png)
* From it's inception up until late 2011 BTC revenue per hash in USD was as high as 5 dollars per hash 
in todays BTC prices. This meant that everything after late 2011 looks like a flat line on the full chart, so we plotted only from 2016 onwards.
* Fun fact, this means that if you mined even for 1 minute 
with a rig running at 10 mh's (similar to mining with a laptop CPU) and held that BTC up until today, you would have roughly the equivalent of three billion USD.

* 10,000,000 hashes per second for 1 minute = 600m hashes * 5 dollars per hash = 3 billion USD

----
## Bitcoin hashrate and price correlation
----
![Chart](Png/btc_hashprice_correlation.png)
* I am no expert in correlation but I was surprised to see that it does look like there is a correlation between the price and overall hashrate. Sometimes a drop in the hashrate seems to make the price drop and sometimes a drop in the price seems to make the hashrate drop. 
* My uneducated guess would be that when the price drops first, some people deem it no longer worth it to run there mining rigs for a period of time, and when the hashrate drops first it is crypto crackdown FUD affecting buyer sentiment.

----
## Comparing TradFi and Gold mining to Bitcoin, Ethereum and Ethereum 2.0
----
![Chart](Png/tradfi_compared.png)
* Currently the banking system is estimated to use almost 2x the amount of energy that Bitcoin uses and 5x that of Ethereum. 
* Currently the banking system uses 8766x the amount of energy that Ethereum 2.0 uses. It is hard to put a precise monetary value on the banking system but let's compare Ethereum 2.0 with Gold mining
* Gold mining currently uses 8020x the amount of energy that Ethereum 2.0 uses. 
* Gold currently has a market cap of $10t USD. 
* Ethereum currently has a market cap of $247b USD
* Gold's marketcap is 40x larger, but Ethereum is 8000 times more energy efficient. 

----
## Bitcoin and Ethereum energy consumption relative to countries energy consumption
----
![Chart](Png/btc_energy_usage_by_country.png)
![Chart](Png/eth_energy_usage_by_country.png)
* Bitcoin and Ethereum in their current state use the same amount of annual electricity as a small country, Bitcoin falling just inbetween Argentina and Sweden and Ethereum falling just inbetween Romania and Uzbekistan.
* We wanted to plot Ethereum 2.0 next to some things with some similar energy use, but we ran out of time/couldn't find the right data to compare to

----
## Ethereum 2.0 adoption
----
![Chart](Png/eth_2_nodes.png)
![Chart](Png/eth_2_staked.png)
* Ethereum 2.0 encompasses two major upgrades to the Ethereum network, EIP 1559 and the Merge to Proof of Stake. These changes aim to massively increase scalability and hopefully make Ether a deflationary asset as more Ether will be burned during transactions than will be issued to validator nodes.
* In order to test these, the beaconchain was deployed at the start of December 2020. The beaconchain simulates Ethereum PoS by letting users lock their Ether in the staking contract and receive an APY of around 6%. This Ether cannot be withdrawn until the merge to PoS has been completed (The aim is early 2022).
* We included these two charts to show the rate of adoption in just eight short months. 
* There is currently over 6m Ether staked in the ETH 2.0 contract, roughly the equivalent of $12b USD which cannot be withdrawn until an at this time, unspecified date. This is a huge vote of confidence for Ethereum PoS.

----
## Bitcoin and Ethereum candlestick charts
----
![Chart](Png/btc_candles.png)
![Chart](Png/eth_candles.png)
* We included these candlestick charts just for fun, the data used is from the binance API so they will always have the latest asset prices, enjoy!
----
## Dashboard
----
The whole aim of this project was to create a dashboard to convey all of this information in a neat and easy to understand manner. 

We hit a couple of hiccups along the way. We were originally using a python plotting package called [cufflinks](https://github.com/santosjorge/cufflinks), it is an amazing package and we had a lot of fun using it. But once all of the charts were ready to go and it was time to build the dashboard we realised that cufflinks charts wouldn't render within Panel. 

So we refactored all the code to plot the charts with Plotly, and they still turned out great minus a few things that Plotly can't do. It was time to build the dashboard again and once we had a few charts in there we realised that the charts were buggy once rendered using Panel. They have lost most of their interactivity, the datapoints don't always show on hover, you can't use the zoom area function and you can't pan around the chart.

To be honest we were super dissapointed after all of that. We tried multiple solutions but nothing has worked so far. We will continue to try and fix it, but for now if you wan't the full interactivity of the charts make sure to use the starter_code_plotly.ipynb file.

----
## References
----
[digiconomist.net](https://digiconomist.net/)

[cbeci.org](https://cbeci.org/)

[hbr.org](https://hbr.org/2021/05/how-much-energy-does-bitcoin-actually-consume)

[ethereum.org](https://blog.ethereum.org/2021/05/18/country-power-no-more/#:~:text=Digiconomist%20estimates%20that%20Ethereum%20miners,99.95%25%20in%20total%20energy%20use.)

[blockchain.com](https://www.blockchain.com/charts/hash-rate)

[BCEI Whitepaper](https://assets.ctfassets.net/2d5q1td6cyxq/5mRjc9X5LTXFFihIlTt7QK/e7bcba47217b60423a01a357e036105e/BCEI_White_Paper.pdf)

[visualcapitalist.com](https://www.visualcapitalist.com/visualizing-the-power-consumption-of-bitcoin-mining/)

[A study by Galaxy mining](https://docsend.com/view/adwmdeeyfvqwecj2)

[beaconcha.in](https://beaconcha.in/charts)

----
## Requirements
----
To run this dashboard and accompanying starter code files you will need the following software and packages:
* Python
* Jupyter lab
* Panel
* Plotly
* Requests library
* Numpy
* Pandas
* python-binance
