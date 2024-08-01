# prophet-challenge
With over 200 million users, Mercado Libre is the most popular e-commerce site in Latin America. This repository will analyze the company's financial and user data in clever ways to make the company grow. Central task - identify if the ability to predict search traffic can translate into the ability to successfully trade the stock.


# Forecasting Net Prophet

The instructions for this Challenge are divided into four steps, as follows:

* Step 1: Find unusual patterns in hourly Google search traffic

* Step 2: Mine the search traffic data for seasonality

* Step 3: Relate the search traffic to stock price patterns

* Step 4: Create a time series model with Prophet

See python notebook for detailed steps.

# Insights:

## Summary: While there is a weak relationship between traffic and stock price during major events, the relationship between these metrics is weak at best and is not useful for making investing decisions. 

## Did the Google search traffic increase during the month that MercadoLibre released its financial results?

The Google search traffic did increase slightly during May 2020, by 8.6%, but we would have to conduct additional research to understand if this is statistically significant.

Traffic increased on May 5th and 6th, it would be interesting to understand if the traffic increase was driven by the release of financial results or if it was related to something else (for example, a sale or promotion?).

## Are there any time based trends that you can see in the data?

The MercadoLibre website traffic is a window into customer behavior, with daily, weekly and annual seasonality.

Web traffic at a daily level peaks in the evenings, from 8pm to midnight. The morning hours of 6am to 10am have the lowest traffic. It picks up gradually midday, holds steady through dinner time and picks up after dinner.

There is a weekly pattern in the data, as well. Weekdays (Mon - Fri) are the most popular days for online shopping/browsing, with Tuesday seeing peak traffic. Traffic dies down Friday and into the weekend, with Sunday as the least popular day.

Seasonal patterns are more volatile but we see peak shopping at the start of the year, followed by the lead up to Christmas. Late summer - early fall are the low period for the year, punctuated by a few weeks (maybe promotions or with the release of popular items like iphones or gaming systems).


## Do both time series indicate a common trend that’s consistent with this narrative?

While there is a relationship between the stock price and web traffic during specific events - 1. the COVID shutdown and 2. the financial earnings results - the data overall does not show a strong enough relationship between both datasets to predict stock price over time. This is true both visually and by finding the correlation coefficient, which is -0.011 or close to zero.

## Does a predictable relationship exist between the lagged search traffic and the stock volatility or between the lagged search traffic and the stock price returns?

Using a correlation matrix, we can determine the strenght and direction of the relationship between Stock Volatility, Lagged Search Trends and Hourly Stock Return so that we can answer the question - is Search Trend a useful indicator for stock performance. The direct answer is no.

Search Trends + Stock Volatility: the corr coef is -0.15, a weak negative relationship. This means when search increases the stock volatility is slightly decreased but is not a strong predicting indicator.

Search + Hourly Stock Return: corr coef is 0.012, a very weak positive correlation, meaning this is no relationship between the metrics.

##  How's the near-term forecast for the popularity of MercadoLibre?

According to the Prophet model output, the near-term forecast for search traffic indicates a stable trend with traffic remaining at high levels, similar to the historical max. The model shows high confidence in this stable forecast, with minor fluctuations.

## According to the Prophet Model, what time of day exhibits the greatest popularity?

8pm to Midnight continues to be most popular.

## Which day of week gets the most search traffic?
   
Tuesday continue to dominate in web traffic, followed by Wed/Thur/Fri.

## What's the lowest point for search traffic in the calendar year?

The early fall period (Sept to Oct) is the weakest of the year.
