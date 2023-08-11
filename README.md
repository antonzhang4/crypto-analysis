# crypto-analysis
All Juypter notebook projects above start by authentication for usage of the Binance API. After authentication, historical data is retrieved to test various methods of predicting buying and selling times


## Technical Analysis
This approach involves taking the 'Volume', 'Number of trades' and 'Close price' and looking back in time from any given moment. Upon comparing, if all the features above pass a certain threshold, we determine that there is a buy signal. Issues with this current approach is that applying a similar idea to finding selling moments doesn't work. Also, it is hard to test approach to timing the market because it works very well only on long time intervals over several months

## training-model-with-binance-api
This approach takes all the historical data and adds an additional feature. This is feature is the future price. Each row will display all the current prices along other relevant information and the final column will contain the close price of the next row of data (what is should predict as the future price). Afterwards, machine learning is used. So far, any Machine Learning algorithm applied to data structured in this way always performs very similarly. The predictions always lag behind by 1 step making it a poor method of predicting prices

## Reddit-API
Look through reddit subreddits and retrieve relevant posts on particular cryptocurrencies. Retrieve the sentiment from these posts and comments and see if their is a relationship between these posts and fluctuations in the crypto prices