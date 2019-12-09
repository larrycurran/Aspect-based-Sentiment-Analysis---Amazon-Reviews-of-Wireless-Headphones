# Topic/Aspect Extraction---Amazon-Reviews-of-Wireless-Headphones
## Executive Summary
This project sought to usr unsupervised Natural Language Processing (NLP) techniques and modeling to extract features of wireless headphones. The data came from two places. The first is a Kaggle dataset of amazon reviews of wireless headphones. The second source is data I scraped from amazon from various product review pages using a Google Chrome Web Scraper extension. I chose wireless headphones as the product I would like to review because there are definitely specific features coming out in the newer headphones that warrant sentiment analysis.

The data required significant cleaning, including removal of emojis, extra characters, numbers, etc.  There could still be cleaning because of typos and other errors in the reviews that could cause some issues in a model.  What I learned from this is that the data cleaning, particularly with regards to NLP, is extremely important and it impacts your results more so than with numerical data.  

During the Exploratory Data Analysis phase, I conducted an overall sentiment analysis, as well as used Word2Vec to see if there were any insights to be gained from the word similarities. 

I ultimately chose to use a Latent Dirichlet Annotation (LDA) model to conduct a topic/aspect extraction from the over 30,000 reviews that I had on 15 different wireless headphone products.  The LDA model does not provide the number of topics, nor does the output identify the topics.  Rather, the model takes an input from the use on how many topics to output, and the highest coherence score is the one that should be chosen.  Then, it is up to the user to infer what the topics are by examining the model results and which words are most associated with that topic.  This model had the highest score on 5 topics/aspects, and they were not the intuitive ones you would assume for wireless headphones.  

I will continue to iterate on this model, as well as use deep learning techniques to improve the aspect extraction and conduct a sentiment analysis on those aspects.  

### Problem Statement
There are so many different types of headphones, and new features come out seemingly every day. I want to be able to determine among some of the most popular headphones, what specific features draw people to or away from purchasing those headphones. This analysis can be used by companies like Apple and Samsung to determine whether or not their product designs and features are worth the R&D costs, as well as the manufacturing costs.

### Data Science Questions
What insights can be gained through Natural Language Processing techniques/modeling on Amazon product reviews of wireless headphones, particularly related to headphone features that customers are discussing?
Are customers talking about the same features/aspects?
How many aspects are discussed in all of the available reviews?
Ultimately, how do customers feel about those features related to a specific product?

### Risks and Assumptions
The biggest risk/assumption is that the feedback in the reviews on Amazon is genuine and not bot-generated. This would cause the models to possibly inproperly classify the sentiment of the reviews towards certain features.

### Web-scraping to Acquire Data
Outside of the Kaggle dataset of wireless headphone reviews, I used the Google Chrome Web Scraper extension to create a customized scrape of the product review pages.  The extension allows you to parse the html and choose and label the columns, and when the scrape is complete (~30min for 5,000 reviews), the scrape is exported into a .csv file.

### Data Cleaning and Preprocessing
The data required significant cleaning.  This included all of the regular work for natural language processing, such as lowercasing, removing numbers, and using regex to remove punctuation, emojis, etc.  This was done through multiple functions.

### EDA 
There were very little null values, and the biggest concern was to make sure I had the columns names properly and the datatypes correct so that after scraping each page, I could concat the dataframes from each product into a master dataframe. As part of my EDA, I also conducted a general sentiment analysis of the headphones, as well as used Word2Vec to see if there were any significant findings from word similarities.

### The LDA Model 
LDA is specifically designed for NLP topic extraction/analysis.  It uses a probability distribution to show which words the focus of the given document. LDA outputs a fixed set of topics. Each topic represents a set of words, and the goal of LDA is to map all the reviews (documents) to the topics. The LDA does this such that the words in each review are mostly related back to the imagined topics.
I used 3, 5, and 7 topics and found the highest model score was on 5 topics.  What I found was that the topics I could infer from the words related to them were not what I had assumed.  For example, there was no distinct topic for noise cancellation.  


### Way Forward 
I will conduct an aspect-based sentiment analysis on the Amazon reviews of the headphones using a variety of deep learning techniques and neural network models. "The big difference between sentiment analysis and aspect-based sentiment analysis is that the former only detects the sentiment of an overall text, while the latter analyzes each text to identify various aspects and determine the corresponding sentiment for each one."
