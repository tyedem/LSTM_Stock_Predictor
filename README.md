# LSTM Stock Predictor

![deep-learning.jpg](Images/deep-learning.jpg)

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG)](https://alternative.me/crypto/fear-and-greed-index/) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. Here I am building and evaluating deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

I use long short-term memory recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the closing price while the second model will use a window of closing prices to predict the nth closing price.

### Libraries

This project uses the pandas, hvplot, tensorflow, keras and sklearn libraries.

# Summary

After tuning and comparing LSTM models using the Crypto FNG Index and BTC closing prices, it is evident that using BTC closing prices tracks actual values better over time. It also demonstrates a lower loss when compared to the FNG model. When tuning the model, the window size that works best is 1 day. The greater the window size, the less the model tracks the actual values over time and the greater the loss. Ultimately, it is not advised to try and predict closing prices. At best, the model can be used to understand the predicted trend rather than the actual price.

## LSTM Model Comparison

![LSTM_BTC](Images/LSTM_BTC.png)

![LSTM_FNG](Images/LSTM_FNG.png)