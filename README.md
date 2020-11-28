# Text-Mining_Amazon-Reviews
To predict the sentiment of a product review by fitting models like Bernoulli and  Multinomial NB

# Data Source
* Website: Data is obtained from Kaggle. Since its a large file, it is compressed and zipped

# Importance and implications
* Amazon is a world's E-Commerce leader : Reliable & Safe
* Online shopping : Easy, Flexible, & Better Prices
* Product reviews: Becoming more important with the evolution
* Reaction : With the vast amount of consumer reviews, it creates an opportunity to see how the market reacts to a specific product
* Check with Models: Check if we can predict the sentiment of a product review by fitting models like Bernoulli and  Multinomial NB

# Data Description:
* A list of over 34,000 consumer reviews for Amazon products like the Kindle, Fire TV Stick, Bluetooth Speaker, Keyboard etc
* Includes basic product information, review ratings, review title, review text and user details
* The text columns “reviews.text” and “reviews.title” would be of primary focus for the project analysis

# Business Problem and Assumptions
* How are the sentiments on the text columns and the top positive and negative words? 
* Logistic Regression for number of helpful reviews with respect to other attributes
* How accurate is ‘reviews.numHelpful’ w.r.t. ‘reviews.text’?
* How accurate is ‘reviews.numHelpful’ w.r.t. ‘reviews.title*?
Assumptions:
* sample size of 30K examples are sufficient to represent the entire population of sales/reviews
* Information in the text reviews of each product will be rich enough to train a sentiment analysis classifier with accuracy (hopefully) > 70%

# Data Cleaning
* Columns chosen in the final dataframe :
* reviews.doRecommend, reviews.numHelpful, reviews.rating, reviews.text and reviews.title
* Dropped the null rows in the dataframe.
* Check for duplicates values - False
* Columns transformed to binary values :reviews.numHelpful, reviews.doRecommend and reviews.rating

# Sentiment Anlayis with VADER
* Gather sentiments on “reviews.text” and “reviews.title” columns

# Loigstic Regression
* Converting reviews.text and reviews.title features to its length of sentence.
* Converting sentiment scores to 0 and 1:
* Sentiment score >=0.05 return 1
* Sentiment score <=0.05 return 0


# Modelling - Building Count Vector & TFIDF Vector 
* Count Vectorizer converts each sentence into its own vector, it does not consider the importance of a word across the complete list of sentences 
* The goal of using TF-IDF is to scale down the impact of tokens that occur very frequently in a given corpus


# Conclusion

* Positively skewed dataset is consistent with both our data exploration as well as sentiment analysis.
* Overall it is a positive sentiment for the products considered in the dataset.
* Products with high rating are sometimes not recommended.
* From the logistic regression summary we can see that the length of the reviews text and the length of the reviews title have their p-values smaller than 0.05 and therefore       plays a significant role with respect to  number of helpful reviews.
* Multinomial NB model fits the data with higher accuracy than the Bernoulli NB.
* Columns ‘reviews.text ‘ and ‘reviews.title’ are equally helpful in choosing the product for the customers.



