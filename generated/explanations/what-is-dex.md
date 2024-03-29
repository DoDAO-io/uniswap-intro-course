## Header
This is the course header. This will be added on top of every page. Go to [DoDAO.io](https://www.dodao.io) to know more.

 ---
 
 ## What Is a DEX?
 
 **What is Automated Market Maker?**        

### Exchanging Assets

Cryptocurrencies are exchanged for reasons similar to those in traditional financial markets, including investment, trading, hedging, risk management, payment purposes, access to new tokens and projects, and regulatory compliance. Cryptocurrencies are seen as a new asset class with high potential returns and are highly volatile, creating trading opportunities for investors. Cryptocurrencies can be used to hedge against other investments or to manage risk in a portfolio. They can also be used as a means of payment for online transactions or remittances. Investors may exchange cryptocurrencies to gain access to new tokens or projects not available on traditional markets or to comply with regulations.

### Traditional Way - Order Book
Assets are traded on an exchange through a centralized platform, an order book, where buyers and sellers place orders to buy or sell a specific asset. Trading involves placing an order, matching orders based on price and other parameters, settling the trade, and clearing it through a central counterparty. 
<div align="center">
<img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/what-is-a-dex-uniswap/1682107243577_order_book.png"/>
</div>

An order book is a list of buy and sell orders for a financial instrument. It shows the supply and demand for the asset and allows traders to make informed decisions. Each order includes the type, price, quantity, and time. Orders are matched and filled based on price and time stamp. Order books are used in exchange-traded markets for transparency and price discovery.

### New Way - Automated Market Maker
An automated market maker (AMM) is a type of decentralized exchange (DEX) protocol that uses a mathematical algorithm to create a market for trading assets without market makers. It creates a liquidity pool for each asset pair, and the pool's algorithm determines the asset's price based on the ratio of tokens in the pool. The AMM algorithm ensures that the pool has sufficient funds for trading and adjusts the price according to the trading volume and liquidity. 
<div align="center">
<img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/what-is-a-dex-uniswap/1682097075973_10_amm_basic.png"/>
</div>


AMMs are used in DeFi platforms and are popular for their simplicity, transparency, and accessibility.


### Explainer Video
<div class="play-js-player py-6" data-plyr-provider="youtube" data-plyr-embed-id="2tTVJL4bpTU"></div>

 
 **How AMM Works?**        
### AMM Intro
An Automated Market Maker (AMM) is a type of decentralized exchange (DEX) protocol that allows traders to trade cryptocurrencies and other digital assets without an order book or an intermediary. In traditional markets, a market maker plays a critical role in ensuring that there is sufficient liquidity by acting as an intermediary between buyers and sellers. An AMM replaces the role of a traditional market maker with a mathematical algorithm that determines the price of assets being traded.

<div align="center">
<img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/what-is-a-dex-uniswap/1682107290305_amm_logical_diagram.png"/>
</div>

In an AMM, traders can trade cryptocurrencies and other digital assets by swapping them with each other, without having to go through a centralized exchange or intermediaries. Instead, AMMs rely on a liquidity pool, which is a pool of funds that are contributed by liquidity providers. These liquidity providers deposit funds into a smart contract that is designed to facilitate trading.

<div class="play-js-player py-6" data-plyr-provider="youtube" data-plyr-embed-id="1PbZMudPP5E"></div>

### Price Calculation
When a trader wants to buy or sell an asset, they submit a transaction to the smart contract with the amount of asset they want to buy or sell, and the smart contract automatically calculates the price based on a mathematical formula that determines the ratio of each asset in the liquidity pool.

The most common mathematical formula used in AMMs is the constant product formula, also known as the x*y=k formula. This formula ensures that the product of the quantity of each asset in the pool remains constant, which is why it's called the constant product formula. This formula is used in Uniswap, one of the most popular AMMs.

For example, suppose a liquidity provider deposits 100 units of token A and 50 units of token B into the liquidity pool. The total value of the liquidity pool is 100 x 50 = 5000. Suppose a trader wants to buy 10 units of token A with token B. The AMM smart contract will calculate the price of token A in token B based on the ratio of token A to token B in the liquidity pool, and the trader will receive 10 units of token A, while the liquidity provider will receive the equivalent amount of token B.

### Benefits
Here are some benefits of AMMs over order books:
- AMMs provide liquidity to traders with always available prices, while order books require both buyer and seller to agree on a price leading to low liquidity for some assets. 
- AMMs do not need order matching, using a mathematical formula for price discovery based on the asset ratio in the pool. 
- Because AMMs utilize smart contracts and mathematical formulas, traders can exchange assets around the clock, while traditional trading is restricted to operating hours.
- AMMs have reduced risks of price manipulation compared to order books that are susceptible to it.
- Additionally, AMMs have lower barriers to entry, allowing traders to add liquidity to the pool and earn fees instead of requiring significant capital to participate in the market.




One advantage of AMMs is that they enable decentralized trading and remove the need for an order book or an intermediary, which can result in lower fees and faster transaction times.

### Downsides
One major disadvantage is the risk of impermanent loss, which occurs when the value of the two assets in the liquidity pool changes. This risk is higher for volatile assets, and liquidity providers can incur losses if the value of the two assets changes significantly during the time that their funds are locked in the liquidity pool. 
 **What are Liquidity Pool?**        
### What are Liquidity Pools?
A liquidity pool is a pool of tokens held by a smart contract on a decentralized exchange, allowing traders to swap one token for another by trading against the pool. The pool's price is determined by the ratio of tokens in the pool, and liquidity providers earn a share of the trading fees in proportion to the amount of liquidity they provide. Liquidity pools enable decentralized trading by providing a source of liquidity, and are a critical component of AMMs.

<div class="play-js-player py-6" data-plyr-provider="youtube" data-plyr-embed-id="dVJzcFDo498"></div>

### User Position - Liquidity Pool Tokens
In a liquidity pool, users can add funds to the pool in exchange for a share of the liquidity pool tokens. These tokens are used to represent the user's share of the liquidity pool, and they can be traded or sold just like any other cryptocurrency.

Liquidity pool tokens share in a liquidity pool. Liquidity Provides earn a portion of the trading fees generated by the exchange proportional to their share in the pool.

### User Position - NFTs
In Uniswap V3, Liquidity Providers (LPs) receive a non-fungible token (NFT) called a "liquidity position token" instead of traditional LP tokens. This is because Uniswap V3 introduces the concept of "concentrated liquidity," where LPs can choose to provide liquidity within a specific price range or "tick" rather than providing liquidity for the entire price range of an asset. The NFT represents the LP's specific position within a particular tick range, allowing for more granular control and flexibility over their liquidity provision.

### Token Ratios
In a liquidity pool that supports trading between USDC and ETH, the rations determine the relative amount of each token that is contributed to the pool. For example, if the rations are set at 50:50, it means that half of the liquidity pool's value is in USDC and the other half is in ETH. If a user wants to swap 1 ETH for USDC, the pool's smart contract calculates the current exchange rate based on the ratio of USDC to ETH in the pool and determines the amount of USDC that the user will receive in exchange for their 1 ETH. The rations play a crucial role in determining the price of each token in the pool and ensuring that the pool has sufficient liquidity for trading.

The smart contract automatically adjusts the ratio of the two tokens in the pool to ensure that the price remains balanced. If there is more demand for ETH, then the smart contract will automatically adjust the price of ETH higher and the price of USDC lower to encourage more users to sell ETH and buy USDC. This helps to ensure that the pool remains liquid and that users are always able to buy and sell the tokens they need.

 
 **Types of AMMs**        
There are several types of AMMs, each with their own unique features and characteristics. In this answer, we'll explore the three most common types of AMMs: Constant Product, Constant Sum, and Hybrid AMMs.

### Constant Product AMM:
Constant Product AMMs, also known as Uniswap-style AMMs, are the most popular type of AMM. In a constant product AMM, the product of the quantity of two assets in a liquidity pool remains constant. For example, if a pool contains 100 units of token A and 200 units of token B, the product of the two is 20,000. When a user wants to trade one token for another, they deposit one token into the pool and receive the other token in return, causing the product of the pool to remain constant. The price of each token is determined by the ratio of the number of tokens in the pool. If more people buy token A, the price of token A will increase and the price of token B will decrease, and vice versa. 
<div align="center">
<img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/what-is-a-dex-uniswap/1682107381351_constant_product_amm.png"/>
</div>

### Constant Sum AMM
In a constant sum AMM, the sum of the quantity of two assets in a liquidity pool remains constant. When a user wants to trade one token for another, they deposit one token into the pool and receive the other token in return. The price of each token is determined by the ratio of the number of tokens in the pool, as well as the sum of the tokens in the pool. Constant sum AMMs are less popular than constant product AMMs, but they have been implemented in several DEXs, such as Balancer and Shell Protocol.

<div align="center">
<img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/what-is-a-dex-uniswap/1682107409699_constant_sum_amm.png"/>
</div>

### Hybrid AMM
Hybrid AMMs combine features of both constant product and constant sum AMMs. They allow liquidity providers to set the parameters of the pool, such as the ratio of the two assets in the pool and the sum of the two assets in the pool. The price of each token is determined by the ratio of the number of tokens in the pool, as well as the sum of the tokens in the pool. Hybrid AMMs are less common than constant product AMMs, but they have been implemented in several DEXs, such as Curve and Bancor.

<div align="center">
<img style="max-height:400px;margin-bottom:30px" src="https://d31h13bdjwgzxs.cloudfront.net/academy/uniswap-eth-1/Guide/what-is-a-dex-uniswap/1682107429503_hybrid_amm.png"/>
</div>

### Comparing

| Type of AMM      | Pros                                           | Cons                                           |
| ---------------- | ---------------------------------------------- | ---------------------------------------------- |
| Constant Product | - Simple and easy to use<br>- High liquidity   | - Limited control over price<br>- High slippage |
|                  | - Less chances of impermanent loss                           | - Limited flexibility                           |
|                  | - Popular and widely used                       |                                                |
| Constant Sum     | - More flexibility and control over price       | - More complex and less intuitive               |
|                  | - Lower slippage                               | - Potential for impermanent loss                |
|                  | - Can support multiple assets in one pool       | - Less liquidity than constant product AMMs    |
| Hybrid           | - Combines the advantages of constant product and constant sum AMMs    | - More complex and less intuitive               |
|                  |                          | - Potential for impermanent loss                |
|                  | - More flexibility and control over price       | - May have lower liquidity than constant product AMMs      |
 
 **Conclusion**        
Cryptocurrencies are exchanged for various reasons, and traditionally, assets are traded on centralized platforms through an order book. However, an automated market maker (AMM) is a type of decentralized exchange that allows traders to swap cryptocurrencies and other digital assets without the need for an order book or intermediary. Instead, AMMs use a liquidity pool, where traders can trade assets by swapping them with each other. The pool's price is determined by a mathematical formula based on the ratio of tokens in the pool, ensuring sufficient funds for trading. AMMs offer several advantages, including always available prices, faster transactions, lower fees, and reduced risks of price manipulation. However, the risk of impermanent loss exists, where liquidity providers can incur losses if the value of assets in the pool changes. There are several types of AMMs, including constant product, constant sum, and hybrid AMMs, with unique features and characteristics.

 
 
