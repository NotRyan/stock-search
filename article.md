# Building a Stock Market predictor with Milvus and LSTM networks.

Predicting trends on the stock market has been a goal for as long as stock markets have existed. The motivation is simple; anyone able to predict market trends can make money off of it. However, this is not an easy task. The [efficient-market hypothesis](https://en.wikipedia.org/wiki/Efficient-market_hypothesis) suggests that the market prices at any given instant take into account all publicly availiable knowledge, thereby making prediction of future prices using the same set of information effectively impossible. 

Despite how often this hypothesis is mentioned, the fact remains that a multi-billion dollar industry exists around trying to predict the stock market. This would seem to indicate that the entire financial industry is hopelessly misguided, or the efficient-market hypothesis is not quite as airtight as it purports itself to be. 

### Forecasting the market

There are several ways to predict the market. The traditional method is known as [fundamental analysis](https://www.investopedia.com/terms/f/fundamentalanalysis.asp). Fundamental analysis involves analyzing and understanding a business's accounts, operations, business strategy, and more. In other words, it is looking at the business itself to try to identify stock performance.

The second way to predict the market is [technical analysis](https://www.investopedia.com/terms/t/technicalanalysis.asp). Technical analysis attempts to predict market trends by using past patterns of a stock's price movements. It is worth noting that technical analysis is not as at-odds with the efficient-market hypothesis, unlike fundamental analysis. A wide variety of technical analysis techniques exist with various types of math and associated strategy, but here we'll be attempting to perform technical analysis with the use of machine learning. 

### Long-Short Term Models: LSTMs

Long-Short Term Models (LSTM) are a type of recurrent neural network which excel as processing time-series data. Due to this, it is a commonly chosen model for stock market analysis, as stock market trends are a form of time-series data. LSTMs are often trained on a singular time-series set in order to predict future outcomes of that same time-series set; an operation known as time-series forecasting.

In this project, we combine LSTM models and Milvus as a form of Ensemble Learning to reduce over-fitting. After selecting a target stock and time period, we leverage Milvus to find similar stock time periods from our historical data. We then use classifiers trained on each stock to create predictions for our target stock, combined using a weighted average into a single prediction.

## Implementation details - pending feedback on the notebook itself. If you are reading this, [please review the project here](stock\ search\ v3.ipynb) and send your feedback to Ryan on the U.S. team.