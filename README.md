# Exploratory Data Analysis of Energy Prices in Spain

## Overview

This project presents an in-depth exploratory data analysis (EDA) of energy prices in Spain. Utilizing comprehensive datasets, the study focuses on uncovering trends, patterns, and insights related to the fluctuation of energy costs over time. The data is taken from ENTSOE, a public portal for Transmission Service Operator (TSO) data.

## Methods

Three algorithms are used to aid in the inference process: L1-Penalized Lasso regression, a simple decision tree and a bagged decision tree algorithm. 

## Results (Taken from Notebook)

1. Production variables such as Gas, Coal, Nuclear, etc are quite a bit more important to determine electricity prices than weather variables. Chief amongst those variables, is Gas, which makes a lot of sense given the actual energy crisis which is mostly caused by a shortage of natural Gas supply in Europe due to armed conflicts. The bagged deicion tree model, the more accurate one so far, yielded a test MSE of 29.9 when using all the variables, and slightly higher at 36 when using just the production variables. However, it yielded a much higher test MSE of 111.9 when just using the weather variables.

2. However, the weather variables can be helpful when analyzing electricity prices, as we saw that the models that included all variables had lower test MSE’s than the corresponding ones with just production or weather variables. On their own, we can see that in general, the temperature variables seem to dominate over all other weather variables.

3. In general, the problem of determining Gas prices is a highly non-linear one, which is why we saw the dramatic decrease in test MSE in every scenario once we moved to a more flexible model.
