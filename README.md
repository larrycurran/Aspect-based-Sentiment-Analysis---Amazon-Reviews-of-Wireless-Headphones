# Aspect-based-Sentiment-Analysis---Amazon-Reviews-of-Wireless-Headphones
GA Capstone Project - NLP of scraped Amazon reviews to analyze features of wireless headphones
I have chosen to conduct an aspect-based sentiment analysis of product reviews.  I chose wireless headphones as the product I would like to review because there are definitely specific features coming out in the newer headphones that warrant sentiment analysis.

Problem Statement:  There are so many different types of headphones, and new features come out seemingly every day.  I want to be able to determine among some of the most popular headphones, what specific features draw people to or away from purchasing those headphones.  This analysis can be used by companies like Apple and Samsung to determine whether or not their product designs and features are worth the R&D costs, as well as the manufacturing costs.  

Proposed Methods:
I will conduct an aspect-based sentiment analysis on the Amazon reviews of the headphones.  "The big difference between sentiment analysis and aspect-based sentiment analysis is that the former only detects the sentiment of an overall text, while the latter analyzes each text to identify various aspects and determine the corresponding sentiment for each one."  

Once the EDA is done, the next steps are to make the data ready to be placed into an undersupervised Machine Learning model or a neural network.  The models used will be cluster models, as well as various classification tools to determine whether the overall sentiment of a speciic feature on a certain model of headphone is positive or negative.  

Risks and Assumptions:  The biggest risk and assumption is that the feedback in the reviews on Amazon is genuine and not bot-generated.  This would cause the models to possibly inproperly classify the sentiment of the reviews towards certain features.

Criteria for Success:  The goal is to determine a number of specific features on specific headphone models to show the popularity/unpopularity of the feature compared to other aspects of the headphones or other headphones with that same feature. 

Data Source:  I have two main sources of data.  The first is a Kaggle dataset of amazon reviews of wireless headphones.  The second source is data I scraped from amazon from various product review pages.  I used a Google Chrome Web Scraper extenstion to conduct these scrapes.  

Preliminary EDA - There were very little null values, and the biggest concern was to make sure I had the columns names properly and the datatypes correct so that after scraping each page, I could concat the dataframes from each product into a master dataframe.  
