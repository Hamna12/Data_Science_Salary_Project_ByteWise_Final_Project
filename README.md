# PROJECT OVERVIEW

## Data_Science_Salary_Project

# Data Science Job Position Organizer: 
What we have done
* Created a tool that estimates data science salaries (MAE ~ $12k) to help data scientists negotiate their income when they get a job

* Scraped over 1000 job descriptions using python and selenium

* Engineered features from the text of each job description to quantify the value companies put on python, excel, aws, and spark.

* Optimized Linear, Lasso, and Random Forest Regressors using RidsearchCV to reach the best model.

* Built a client facing API using flask.

# RESOURCE:

## Programming Language I used and Version
* Python: 3.9
* Packages: pandas, numpy, sklearn, matplotlib, seaborn, selenium, flask, json, pickle
* For Web Framework Requirements: pip install -r requirements.txt

## Video I followed
* Guided DS Salaries Project: https://www.youtube.com/playlist?list=PL2zq7klxX5ASFejJj80ob9ZAnBHdz5O1t

## GitHub 
* Scraper Git Hub: https://github.comarapfaik/scraping-glassdoor-selenium

## Medium
Scraper Article: https://towardsdatascience.com/selenium-tutorial-scraping-glassdoor-com-in-10-minutes-3d0915c6d905

# Following are the Steps that I followed:

## 1. WEB SCRAPPING:
Tweaked the web scraper and scrapped Data of different Data Science jobs from glassdoor.com. With each job, I got the following:

* Job title
* Salary Estimate
* Job Description
* Rating
* Company
* Location
* Company Founded Date
* Type of Ownership
* Industry
* Sector
* Revenue

# NEXT STEP IS:
## 2. DATA CLEANING

After collection of data then next important step is Data Cleaning. After scraping the data, I needed to clean it up so that it was usable for my model. I made the following changes and created the following variables:

Parsed numeric data out of salary
Made columns for employer provided salary and hourly wages
Removed rows without salary
Parsed rating out of company text
Made a new column for company state
Transformed founded date into age of company
Made columns for if different skills were listed in the job description: ..* Python ..* R ..* Excel ..* AWS ..* Spark
Column for simplified job title and Seniority
Column for description length
Column for minimum degree reqirement

# NEXT STEP IS:
## 3. EXPLORATORY DATA ANALYSIS

Exploratory Data Analysis refers to the critical process of performing initial investigations on data so as to discover patterns.In data mining, Exploratory Data Analysis (EDA) is an approach to analyzing datasets to summarize their main characteristics. So after cleaning Data I display my data into different graphs like Bar charts, Box Plots and Bar charts.

# Model Building:

So in next step I built model using train and Test split functions. and then deploy my model.

# Putting Model into Production:
After model building I used Flask API to put my model into server. The API endpoint takes in a request with a list of values from a job listing and returns an estimated salary.
