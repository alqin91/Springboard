# Distingushing messages: SPAM OR HAM

*Users who recieve messages via email, text, or other communicaton experience spam or fake messages. This may cause users to fall for scams or be exposed to illegitimate practices. If we can eliminate this issue and focus on differentiating spam and ham (real messages), users will be better off.  

## Data

*The data we will be using is from kaggle. The SMS Spam collection is a set of text messages collected for the SMS Spam research. There are 5572 messages of which some are tagged as spam and others as ham. 

> * [Kaggle Dataset](https://www.kaggle.com/uciml/sms-spam-collection-dataset)

## Data Wrangling

*I will be cleaning the data and seperating the spam and ham. I will also create features such as message length and value where 0 is ham and 1 is spam.

## EDA

*I will be exploring and analyzing correlations between message length and spam vs ham and frequency of occurance betwween ham and spam. I will then clean the messages by eliminating puncutation and stopwords using the nltk.corpus module and stopwords. Then I will determine the most common words in spam and ham and assign a numerical value to them.


## Modeling/Predictions

*I will use countvectorizer to convert the text to matrix of token counts. Then use the multinomial Naive Bayes classifier to classify features. Will also be using tf-idf to transform a count matrix to a normalized tf-idf. I will use tf-idf to scale down impact of tokens that occur more frequently. So the more common a word is, the less of a score they recieve. The more unique of a word, the higher the score. Then compare the model to a logistic regression model and compare the accuracy scores and the confusion matrix to see which model works better in differentiating spam vs ham.





