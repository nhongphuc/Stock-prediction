# Stock-prediction

![alt text](https://github.com/nhongphuc/Stock-prediction/blob/main/StockPicture.jpg)

The goal of this project is to develop models to forecast stock prices. 

## Data

The data comes from the Nasdaq API. Specifically, we'll use equities data from the Frankfurt Stock Exhange (FSE).

## Data Wrangling

- We first cast the entire data for FSE in JSON format. Then, we used a subset of that data from 2010 to 2017 as the training data, and stored that time series in a pandas dataframe. We did not want to use data before 2010 to avoid the financial crisis of 2008.
- Initially, we intended to use data after 2017 as the test data. However, we found that the data for FSE after 2017 contained a large swatch of missing values. We could have imputed those missing values, but that didn't seem like a good idea because so many of them were missing. So, we chose to evaluate our model by an in-sample forecast instead of out-of-sample forecast with the test data.

## EDA
- We studied the statistical properties of the stock returns, which we derived from the stock prices by: (1) resampling the stock prices to weekly frequency, and (2) computing the percentage change of the resampled data.
- We found that the autocorrelation of the weekly return is negative (specifically -0.14), so the series is mean reversing. 
- We plotted the ACF of the return to test the statistical significance of the value -0.14. We found that it is indeed significant (with 95 % confidence interval).
- Furthermore, the ACF plot reveals that - among the first 10 lags - only the lag-1 autocorrelation is statistically significant.
- The PACF plot of the returns is quite similar to the ACF plot (only the lag-1 partial autocorrelation is statistically significant), and it is negative.
- We used the augmented Dickey-Fuller test to see if the stock prices is a random walk, and we rejected the null hypothesis that it is a random walk (the p-value was 0.023, which is smaller than 0.05).
- We also used the KPSS test to see if the returns are a stationary time series, and found that we can accept the null hypothesis that it is (the p-value was 0.1, which is larger than 0.05).

## Preprocessing



## Modelling

## Conclusion and future improvement
