# Recommender systems based on Amazon review data using Machine learning 

Problem statement:
---
  The problem our model works on is that when an internet user wants to use an e-commerce platform like amazon to buy a product, the one thing they trust are the reviews. So, our model tries to get data related to products and their ratings/reviews and work on it. We use sentiment analysis on the reviews and create a sentiment summary for a list of keywords.Our model at the end suggests the desired products to users based on their individual interests and overall ratings of the products. 

Project plan:
---
* Amazon review data
* Preprocessing the data and using a sample of the data for the project
* EDA
* Sentiment analysis
* Recommender system

 
About the data:
---
Around 1 million rows of data. EDA resulted in understanding 60813 unique reviewers and 4181 unique products.
Null values and unique categories have been checked and action has been taken. Few plots to better understand the data,
![Markdown Logo](https://github.com/abhi19071993/gitpracticum1/blob/master/eda_1.png)

It is evident from the above plot that number of ratings for the products have greater concentration when ratings count is less than
100 and very few products have more than 500 ratings.
 
 Another plot between productID and mean rating the product got is,
 
 ![Markdown Logo](https://github.com/abhi19071993/gitpracticum1/blob/master/eda_2.png)

Plot between the overall rating vs the number of products rated is,

![Markdown Logo](https://github.com/abhi19071993/gitpracticum1/blob/master/eda_3.png)

 5 rating had been given the most number of times and 2 rating had been given the least number of times.
 
 Sentiment analysis:
 ---
 
 We create an SFrame from the dataframe with columns reviewerID,productID,reviewText and overall rating. This SFrame is given as an input to graphlab's funtion to create the product sentiment summary which tokenizes the keywords in the review, does TF-IDF transform and creates inverted index.
 
 ![Markdown Logo](https://github.com/abhi19071993/gitpracticum1/blob/master/sentiment_1.png)
