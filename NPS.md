The Net Promoter Score was created by Bain & Co's Fred Reichheld as a metric to gauge customer satisifaction and debuted in Harvard Business Review's 2003 article "One Number You Need to Grow”. Its alleged correlation with net inncome has earned management's ear, witnessing a 500% increase in mentions over the past 5 years on S&P 500 companies earnings calls (WSJ). 

Although rising in popularity, Net Promoter Scores still rely on traditional surveys, subjecting them to unnecessary associated biases. When was the last time you completed a survey? Exactly. Online reviews, on the other hand, are more accessible and improve accuracy through sample size and purchase verification. This project strived to improve Net Promoter Scores by employing Natural Language Processing and Machine Learning to gauge customer satisfaction from the Amazon Reviews data set.

Q: "On a scale of 0 to 10, how likely are you to recommend this product or service?"

NPS scoring awards a +1 to anyone responding with a 9 or 10, a zero in the 7 - 8 region, and negative 1 otherwise. This number is then divided by the total respondents to yield the average NPS on a scale from -100 to 100. 

Step 1 is to verify the base assumption that a robust correlation between review language and satisfaction exists. Using a review's "Star Rating" as a proxy for customer satisfaction, this 5 point rating system was mapped to the NPS systems as follows: (since this step is only to verify correlation, some signal loss from this mapping is acceptable)

* 5 Stars - Promoter
* 4 Stars - Neutral
* < 4 Stars - Detractor 

Given the importance of this assumption, it's important to test it with a few combinations of vectorizers and algorithms. In this case, Count Vectorizer and Term Frequency-Inverse Document Frequency (TF-IDF) vectorizers were used with Logistic Regression and Naive Bayes (Bernoulli and Multinomial) algorithms. Hyperparameters with n-grams of 1 and 1-2 were set for both vectorizers. The results yielded F-1 Scores between 78.1 and 83.3, demonstrating sufficient review language / star rating correlation to continue with NLP.

Step 2 - Sentiment Analysis with Valence Aware Dictionary and sEntiment Reasoner (VADER):

With a scale of -1 to 1, Vader's sentiment scoring conveniently mirrors the Net Promoter Score. Additionally, Vader scores also provide 100x the accuracy of traditional NPS: 2 decimal places vice zero. This is a critical improvement that solves the fidelity loss problem from mapping 11 points scales to 5. Ideally, some combination of rating and sentiment could get closer to the truth. 

