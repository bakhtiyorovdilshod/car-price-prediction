# Car Salary Prediction (Uzbek cars) Project Overview
* Created a small system that estimates uzbek cars prices in order to help people buy or sell their own cars with best price on the market.
* Scraped over 20000 cars descriptions from [avtoelon](https://avtoelon.uz/uz/) using python and Scrapy
* Engineered features from the text of each job description to quantify the value companies put on python, excel, aws, and jupyter notebook
* Optimized Linear, Lasso, and Random Forest Regressors using GridsearchCV to reach the best model.
* Built a client facing API using fastapi

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
