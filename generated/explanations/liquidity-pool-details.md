## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## Liquidity Pool Details
 
 **Liquidity Graph**        
### Uniswap V2 - Liquidity Graph
In Uniswap v2, liquidity providers (LPs) deposit an equal value of two tokens (e.g., ETH and DAI) to create a liquidity pool. In our example, the pool consists of 100 ETH and 150,000 DAI. The liquidity in Uniswap v2 is spread uniformly across the entire price range, from 0 to infinity. This means that liquidity is available for trading at all price levels.

When a user trades in the pool, the price is determined by the current ratio of the two assets in the pool, following the constant product formula (x * y = k). In our example, the initial ratio is 100 ETH * 150,000 DAI = 15,000,000.

<div align="center">
<img src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/liquidity-pool-details-uniswap/1681912476448_07_v2_liquidity_chart.png" />
</div>

### Explainer Video
<div class="play-js-player py-6" data-plyr-provider="youtube" data-plyr-embed-id="rWPVTz4cao8"></div>


### Uniswap V3 - Liquidity Graph
Uniswap v3 introduces the concept of concentrated liquidity, which allows liquidity providers to specify a price range for their liquidity. Instead of providing liquidity across the entire price spectrum, LPs can choose custom price ranges where they believe most of the trading will happen. This allows them to earn more fees for a given amount of deposited capital.

In our example, if an LP believes that the ETH/DAI price will stay between 1,400 DAI and 1,600 DAI, they can deposit their liquidity within this range. This effectively concentrates their liquidity around the expected price, which can lead to more efficient capital usage and potentially higher returns.

<div align="center">
<img src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/liquidity-pool-details-uniswap/1681912741645_07_v3_liquidity_chart.png" />
</div>

To sum up, in Uniswap v2, liquidity is spread uniformly across the entire price range, while in Uniswap v3, liquidity providers can concentrate their liquidity within custom price ranges, which can lead to more efficient capital usage and potentially higher returns.



 
 **Real Reserves Graph**        
## Real and Virtual Reserves
In Uniswap V3, the concepts of real and virtual reserves are used to manage liquidity within a pool. Let's break down these terms in simple words and provide an example to illustrate their roles.

**Real reserves**: Real reserves are the actual amounts of the two tokens held in a liquidity pool. When liquidity providers (LPs) add or remove liquidity, they directly affect the real reserves. The real reserves are used to calculate the exchange rate between the two tokens in a pool, following the constant product formula (x * y = k).

**Virtual reserves**: Virtual reserves are a mathematical concept used to determine how much liquidity is available for trading within the current price range. They are not actual tokens held in the pool but rather a representation of the liquidity that is active within a specific price range. Virtual reserves help calculate the effective exchange rate and slippage for trades within the given range.

<div align="center">
<img src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/liquidity-pool-details-uniswap/1681926781696_09_real_reserves.png" />
</div>

### Example
Let's consider another example using the Uniswap V3 ETH/USDC pool. In this case, we'll use specific real reserve amounts and simulate adding liquidity within a certain price range.

Assume the ETH/USDC pool has the following real reserves:

```
Real reserves: 50 ETH and 100,000 USDC (Initial Value)
```
Now, a liquidity provider (LP) wants to add liquidity within the price range of 1,800 USDC/ETH to 2,200 USDC/ETH. They decide to add 10 ETH and 20,000 USDC within this range.

After adding the liquidity, the pool's real reserves will be updated:

```
Real reserves: 60 ETH (50 + 10) and 120,000 USDC (100,000 + 20,000)
```

However, only the added liquidity by the LP falls within the specified price range (1,800 to 2,200 USDC/ETH). Therefore:
```
Virtual reserves: 10 ETH and 20,000 USDC (the liquidity active within the price range)
```
When a user wants to swap tokens within the 1,800 to 2,200 USDC/ETH price range, the virtual reserves (10 ETH and 20,000 USDC) will be used to determine the exchange rate and potential slippage for their trade. Trades outside of this price range will not have access to the virtual reserves and may experience higher slippage or fail due to lack of liquidity.

This example demonstrates the difference between real and virtual reserves in Uniswap V3. Real reserves are the actual token amounts held in the pool, while virtual reserves represent the liquidity available within a specific price range for trading. 
 **What is a Tick?**        
### Ticks in Uniswap V3
In Uniswap V3, a tick is a discrete value that represents a specific price point within the price range of a liquidity pool. Ticks are used to divide the price range into equally sized intervals, and they help determine how liquidity is distributed across the pool.

Each tick is associated with a unique tick index, which is an integer value. The tick index can be positive, negative, or zero, and the relationship between tick indexes and price is logarithmic. In Uniswap V3, the price at a given tick is determined by the formula: price = 1.0001^(tick index).

An important concept related to ticks is the "tick spacing," which is the difference between two adjacent tick indexes. The tick spacing depends on the liquidity pool's fee tier, and it can be 10, 60, or 200. This means that liquidity providers (LPs) can only add or remove liquidity at price levels that correspond to the tick spacing.

### Example
Let's consider a Uniswap V3 liquidity pool for the token pair ETH/DAI with a tick spacing of 10. Suppose a liquidity provider wants to add liquidity within the price range of 1000 DAI/ETH and 2000 DAI/ETH. To determine the ticks for this range:

1. Calculate the tick index for the lower price bound (1000 DAI/ETH):
tick_lower = log(1000) / log(1.0001) ≈ 6909.57, rounded down to 6900 (nearest multiple of 10)
2. Calculate the tick index for the upper price bound (2000 DAI/ETH):
tick_upper = log(2000) / log(1.0001) ≈ 13819.14, rounded down to 13810 (nearest multiple of 10)

The liquidity provider would then add liquidity between tick 6900 and tick 13810. As the price moves between these ticks, the liquidity provider would earn fees proportional to the amount of liquidity provided and the volume of trades occurring within this range.
 
 **Price Graph with Ticks**        
### Price Graph with Ticks
In Uniswap V3, the price graph represents the relationship between two tokens in a liquidity pool, token-0 and token-1. The amount of token-0 in the pool is denoted as X, and the amount of token-1 in the pool is denoted as Y. The price of token-0 in terms of token-1 is calculated using the constant product formula, where X * Y = k.

<div align="center">
<img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/liquidity-pool-details-uniswap/1682099529192_08_graphs_with_tciks_0.png"/>
</div>



### When traders buy "token-0"
In this scenario, as token-0 is slowly exchanged for token-1, the amount of token-0 (X) in the pool decreases while the amount of token-1 (Y) increases. As a result, the price of token-0 in terms of token-1 will increase, following the constant product formula (since X is decreasing and Y is increasing, k remains constant). The price graph will show an upward curve, indicating a rising price for token-0 as the available supply decreases.


<div align="center">
<img style="max-height:400px;margin-bottom:30px" 
 src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/liquidity-pool-details-uniswap/1682099557308_08_graphs_with_tciks_1.png" />
</div>


### When traders buy "token-1"

In this scenario, as token-1 is slowly exchanged for token-0, the amount of token-1 (Y) in the pool decreases while the amount of token-0 (X) increases. As a result, the price of token-0 in terms of token-1 will decrease, following the constant product formula (since X is increasing and Y is decreasing, k remains constant). The price graph will show a downward curve, indicating a falling price for token-0 as the available supply increases.

<div align="center">
<img style="max-height:400px;margin-bottom:30px"  src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/liquidity-pool-details-uniswap/1682099579132_08_graphs_with_tciks_2.png" />
</div>

It is important to note that in Uniswap V3, liquidity is concentrated within specific price ranges determined by ticks, and liquidity providers can earn fees only when the price is within their specified range. This means that the price graph will not be a smooth curve but rather a series of connected line segments corresponding to the different liquidity positions within the specified price ranges. However, the overall trend in the price graph will still follow the behavior described in each scenario.
 
 
