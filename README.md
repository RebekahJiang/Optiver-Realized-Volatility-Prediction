# Optiver-Realized-Volatility-Prediction
## 1. Project Background: 
In financial market, volatiltiy captures the amount of fluctuation in prices. For trading firms like Optiver, predicting volatilty precisely is essential for the trading of options since the price of options is directly related to the volatility of the underlying product. The target of this competition is to use past 10 minutes high-frequency order book and trade data to predict "realized volatility" over the next 10 minutes.

## 2. Metrics 
The competition is evaluated using the Root Mean Square Percentage Error(RMSPE). Since volatility values are typically small, RMSPE is highly sensitive to relative errors, I apply ***weighting to samples of different mangnitudes***.

## 3. Tools
(1) **Polars**: Given the massive volume of high-frequency financial data, traditional Pandas may encounter bottlenecks in terms of memory and speed. I use Polars for feature engineering, leveraging its ***lazy execution*** mechanism to achieve ultra-fast data processing.

(2) **Training Model**: LightGBM
