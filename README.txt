# Alexa-Amazon-Reviews
The data was scrapped from amazon website. The dataset consisted of a nearly 3000 Amazon customer reviews (input text), star ratings, date of review, variant and feedback of various amazon Alexa products like Alexa  Echo,  Echo dots,  Alexa  Firesticks etc.
The business objective was to predict whether the feedback given by the customers were positive or negative.
In the first step EDA was performed to draw insights. The major insights that were drawn from the dataset was-
 •	Majority of the reviews are reviews ranging between 0 and ~200 characters
 •	The dataset has almost 10 times positive reviews compared to negative reviews.
 •	A review having a rating of 3 or more than 3, is given a feedback of 1, else 0.
The dataset was also checked if it was balanced or not and it was found to be imbalanced so in order to fix this over sampling by smote was implemented to fix it
The data was cleaned by removing special character and numbers using regular expression, Converting the entire sms into lower case, Tokenizing the sms by words, Removing the stop words, Lemmatizing the words, Joining the lemmatized words, Building a corpus of messages.
After performing data cleaning and  obtaining  corpus of messages a bag of model was created with the help of count vectorizer..A classification model was built by splitting the dataset into test and train dataset.
After trying out with different classification models the random forest classifier was selected as the finalized model as it had accuracy of 98% .
The model was deployed with flask framework and Flask API was created using heroku

For EDA and Model Building refer - alexa_reviews_sentiment_analysis_using_nlp.ipynb
For Deployment refer - app.py
Flask API - https://alexa-amazon-reviews-api.herokuapp.com/
