# Car Salary Prediction (Uzbek cars) Project Overview
* Created a small system that estimates uzbek cars prices in order to help people buy or sell their own cars with best price on the market.
* Scraped over 20000 cars descriptions from [avtoelon](https://avtoelon.uz/uz/) using python and Scrapy.
* Engineered features: made new columns, parsed value from the text and removed garbage. 
* Optimized Linear, Lasso, and Random Forest Regressors using GridsearchCV to reach the best model.
* Built a client facing API using FastApi.

## Code and Resources Used 
**Python Version:** 3.8  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, selenium, fastapi, json, pickle    
**For Web Framework Requirements:** FastApi   
**Scraper Github:** https://github.com/bakhtiyorovdilshod/car_price_scrapy   
**Scraper Article:** https://scrapfly.io/blog/web-scraping-with-scrapy/    
**FastApi Deployment:** https://testdriven.io/blog/fastapi-machine-learning/  

## Web Scraping
Tweaked the web scraper github repo (above) to scrape 20000 car postings from avtoelon.uz. With each car, we got the following:
*	Car name
*	Car price
*	Car year
*	Car description
*	Region


## Data Cleaning
After scraping the data, I needed to clean it up so that it was usable for our model. I made the following changes and created the following variables:

*	Parsed numeric data out of car price.
*   Removed newline character from all columns.
*   Made a new column called pozitsiya that parsed from the car name column.
*   Made transmission, fuel_type columns for each car.

## Model Building
We use various machine learning algorithms for building our car price prediction model. Here you can see the final results: 
* Linear Regression: 0.79
* Ridge: 0.79
* Lasso: 0.79
* ElasticNet: 0.79
* KNeighbors: 0.82
* RandomForest: 0.83
* GradientBoost: 0.8
* ExtraTree: 0.82
* XGB: 0.83

## Addition
* Colab: [colab](https://colab.research.google.com/drive/1oVXQu5QxNl0bxrnOcMpzatZR7HrXd4pp#scrollTo=yk73RkMFXtue)
