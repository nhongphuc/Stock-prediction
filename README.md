# Stock-prediction

![alt text](https://github.com/nhongphuc/Stock-prediction/blob/main/StockPicture.png)

The goal of this project is to develop models to forecast stock prices. 

## Data

The data comes from the Nasdaq API. Specifically, we'll use equities data from the Frankfurt Stock Exhange (FSE).

## Data Wrangling

- We first cast the entire data for FSE in JSON format. Then, we used a subset of that data from 2010 to 2017 as the training data, and stored that time series in a pandas dataframe. We did not want to use data before 2010 to avoid the financial crisis of 2008.
- Initially, we intended to use data after 2017 as the test data. However, we found that the data for FSE after 2017 contained a large swatch of missing values. We could have imputed those missing values, but that didn't seem like a good idea because so many of them were missing. So, we chose to evaluate our model by an in-sample forecast instead of out-of-sample forecast with the test data.

## EDA


## Preprocessing



## Modelling

## Conclusion and future improvement
