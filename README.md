  ## Stock Prediction Quick Guide For Beginners Using Data Sceince (EDA,LTSM,KNN)
## _Introduction_

![N|Solid](https://www.investopedia.com/thmb/hATOUQ_Iq5v5CgGKLhrj22v1aXM=/2120x1414/filters:no_upscale():max_bytes(150000):strip_icc()/GettyImages-1300495462-e66753342f304f45a9215505352b596a.jpg)


Everybody has think atleast for a once to invest in stocks, thinking about whether it is a good idea to invest in something you barely know in that case study i will show you how to invest in stock market with a knowledge related to big stocks comapnies APPLE,GOOGLE, etc... (FAANG).

We need to know first the stock types and what is the type that i am going to work on ?
- Large Cap Stocks: These are often stocks of Blue-chip companies which are established enterprises with large reserves of cash at their disposal. It is interesting to note that the larger size of the large cap companies does not mean that they grow more rapidly. In fact it is the small stock companies that tend to outperform them over the longer time frame. But large cap stocks do come with the benefit of allowing the investors to reap higher dividends in comparison to the smaller and mid cap companies stocks, ensuring that the capital is preserved over the long term period.(The model that we will work on like APPLE,AMAZON, etc.....)

- Mid Cap Stocks: These are the stocks of medium sized companies that have a market capitalization of INR 250 Crore to about INR 4000 crore. These companies have a well recognize name in the market which brings along the benefit of potential for growth, as well as the stability that is usually accompanied with being a seasoned player in the market.
Mid cap companies have a good track record of steady growth and are very similar to blue chip stocks barring their  size. In the long term these stocks do and grow well(LIKE Hotels & Resorts Inc).

- Small Cap Stocks: As is suggestive of the name, small cap stocks have the smallest value in the market as compared to its counterparts. These are small sized companies that have a market capitalization of upto INR 250 and have the potential to grow at a good pace in the future. Investors who are willing to commit to a long term and are not very particular about the current dividends, and are willing to stand their ground during price volatility, can make significant gains in the future(LIKE insurance company Genworth Financial Inc. (GNW), printing and imaging company Eastman Kodak Co.)

# Before diving deep into the data analysis we need to first to know some of the most important terminologies.
- Buy: To take a position by buying shares of a company.
As a trader, you generally buy shares when you think a stock’s price will rise.
- Sell: To sell the shares you currently own.Traders generally sell shares when they see an opportunity to take profits or they think the stock’s rise is ending.
- Bid: When a trader in the market makes an offer to buy shares.Traders will bid for a stock at a certain price.
- Ask: When a trader offers their shares for sale at a certain price.
- Bid-Ask Spread: The difference between the highest price at which someone is willing to buy shares and the lowest price someone is willing to sell shares.
- Volatility: The statistical measure of how much a stock moves up or down.
- Liquidity: The measure of how easy it is to buy and sell a stock.
- Trading Volume: The number of shares being traded at any time.
- Going Short: When a trader tries to profit from a stock’s dropping price.
- Going Long: When going long, you purchase stock shares hoping to profit from an increase in the stock price.
- Open: The open is the starting period of trading on a securities exchange or organized over-the-counter market. An order to buy or sell securities is considered to be open, or in effect, until it is either canceled by the customer, until it is executed, or until it expires.
- Close:  The close is a reference to the end of a trading session in the financial markets when the markets close for the day. 
- Today's high: Refers to a security's intraday highest trading price.
- Today's low: The lowest price that a stock trades in that day.
- Adjusted close: Is the closing price after adjustments for all applicable splits and dividend distribution

# Main project questions for 4 companies (apple,microsoft,amazon and google)
I have asked 6 major questios 

>  What was the change in price of the stock over time?
> What was the moving average of the various stocks?
> What was the daily return of the stock on average?
> What was the correlation between different stocks?
> How much value do we put at risk by investing in a particular stock?
> How can we attempt to predict future stock behavior? (Predicting the closing price stock price using LSTM)


From data analysis we have answered the first 5 questions and the last question is for prediction.
#### What was the change in price of the stock over time?
![1](https://user-images.githubusercontent.com/91282437/194433050-ef9056b6-6e8d-40f1-9290-999715cf9f73.png)
After we did the explatory data analysis we have found the below:
- All four companies has got a lower value for their stocks in Sep 2022. 
- From Nov 2021 till Jan 2022 APPLE stock got a higher value over all.
- MICROSOFT stocks got lower value startinf from Nov 2021 until the late Sep 2022.
- GOOGLE stocks got lower value startinf from Nov 2021 until the late Sep 2022.
- We Can see that AMAZON stock market starts to recover from July 2022

#### What was the moving average of the various stocks?
The moving average (MA) is a simple technical analysis tool that smooths out price data by creating a constantly updated average price. The average is taken over a specific period of time, like 10 days, 20 minutes, 30 weeks, or any time period the trader chooses.

![2](https://user-images.githubusercontent.com/91282437/194433807-c5164e98-0b53-49f6-854b-4b8f0697ff9b.png)

After we did the explatory data analysis we have found the below:
- MA for 50 Days shows a progressive over all in four companies 
- Apple share price is 146.40 while AAPL 20-day simple moving average is 146.00, which is a Buy signal.
- Amazon share price is 120.95 while AMZN 20-day simple moving average is 116.66, which is a Buy signal.
- Google share price is 102.22 while GOOG 20-day simple moving average is 99.48, which is a Buy signal.
- Microsoft share price is 249.20 while MSFT 20-day simple moving average is 240.52, which is a Buy signal.

#### What was the daily return of the stock on average?
Daily return is calculated by subtracting the opening price from the closing price. If you are calculating for a per-share gain, you simply multiply the result by your share amount. If you are calculating for percentages, you divide by the opening price, then multiply by 100.

![3](https://user-images.githubusercontent.com/91282437/194434161-7e9caf16-c43d-4467-a331-7f8e5ca008c0.png)
![3](https://user-images.githubusercontent.com/91282437/194434228-2fa00bd7-77c5-413d-a64d-34b87f482d70.png)

After we did the explatory data analysis we have found the below:
- All four companies shows a high daily return.
- AMAZON shows a high daily return value over the last three months.
- GOOGLE is the least daily return value.

####  What was the correlation between different stocks?
![4](https://user-images.githubusercontent.com/91282437/194434392-d4112e94-03e7-485f-ad33-8d51dc5e17cc.png)

After we did the explatory data analysis we have found the below:
- So now we can see that if two stocks are perfectly (and positivley) correlated with each other a linear relationship bewteen its daily return values should occur.

![4](https://user-images.githubusercontent.com/91282437/194434655-a802346e-f49e-40cc-b66d-c8000f675c0a.png)

Above we can see all the relationships on daily returns between all the stocks. A quick glance shows an interesting correlation between Google and Amazon daily returns.

![4](https://user-images.githubusercontent.com/91282437/194434719-3e5f736c-54b8-4c87-b6b5-001b183bc2a0.png)
![4](https://user-images.githubusercontent.com/91282437/194434762-46ba68ab-d49c-4231-8e3d-216e5ebad081.png)

Fantastic! Just like we suspected in our PairPlot we see here numerically and visually that Microsoft and Amazon had the strongest correlation of daily stock return. It's also interesting to see that all the technology comapnies are positively correlated.

#### How much value do we put at risk by investing in a particular stock?

![5](https://user-images.githubusercontent.com/91282437/194434833-8a79266f-f9dc-494b-9b9f-0c6098e9cdb7.png)

After we did the explatory data analysis we have found the below:
- Apple is the most safest place for stock investment (low risk,expected return)
- Microsft is the least risk in the four stocks
- Google has a higher risk and and a low expected return
- Amazon in the highest risk

#### How can we attempt to predict future stock behavior?
![6](https://user-images.githubusercontent.com/91282437/194434916-918d0a79-3b14-43cf-8d4d-e854d03079bf.png)

According to the predection that we have for four companies it shows a good indicator regarding investing with a low price you can buy then sell at a higher price range it shows also a lower range in the late of 2022 but over all from 2012 till 2022 it shows an increasing in value and that's a good indicator.



Thanks for completing that journey with me ;)

