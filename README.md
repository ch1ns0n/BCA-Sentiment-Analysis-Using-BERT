Project Workflow
Here's a simple breakdown of the steps we take:

1. Preparing the Data
First, we take a bunch of news articles that already have sentiment labels. We clean up the text by removing junk like website links and strange symbols. To make sure our model learns fairly, we also balance how many positive, negative, and neutral examples it sees.

2. Training the AI (DistilBERT)
We use a special AI model called DistilBERT, which is great at understanding language. We teach this model by showing it our labeled news articles. It learns to recognize patterns that indicate positive, negative, or neutral sentiment.

3. Predicting on New Articles
Once our DistilBERT model is smart enough, we give it a bunch of unlabeled news articles. The model then predicts the sentiment for each of these articles.

4. Getting Insights
After predicting, we look at the results to understand:
- How many articles are positive, negative, or neutral?
- What are the most common words in positive, negative, and neutral articles? This helps us see what kind of language is used for each sentiment.

5. Making the AI Even Smarter (Semi-Supervised Learning)
We then combine our original labeled articles with the new articles that DistilBERT just predicted sentiments for. We train DistilBERT again, but this time with this larger mix of data. This helps the model become even more accurate.

6. Another Layer of Prediction (Random Forest)
To make our predictions super reliable, we also use another machine learning technique called Random Forest.
- We convert the text into numbers using something called TF-IDF.
- We train the Random Forest model on this numerical data.
- We make sure the model isn't biased by using a technique called SMOTE if we have uneven numbers of positive, negative, and neutral examples.
- Finally, we fine-tune this Random Forest model to get the best possible results.
