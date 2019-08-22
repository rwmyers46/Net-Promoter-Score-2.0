# Net-Promoter-Score-2.0

The Net Promoter Score was created by Bain & Co's Fred Reichheld as a metric to gauge customer satisifaction and debuted in Harvard Business Review's 2003 article, "One Number You Need to Grow.” According to the [Wall Street Journal](https://www.wsj.com/articles/the-dubious-management-fad-sweeping-corporate-america-11557932084), The Net Promoter Score's correlation with net income has earned management's ear, witnessing a 500% increase in mentions over the past 5 years on S&P 500 companies earnings calls.

![alt text](images/nps-graphic.png)

###### *Image: Wall Street Journal*

Although rising in popularity, Net Promoter Scores still rely on traditional surveys, subjecting them to selection biases. Conversely, online reviews inherently increase accuracy by providing both purchase verification and vastly larger sample sizes. This project strived to improve Net Promoter Scores by employing Natural Language Processing and Machine Learning to gauge customer satisfaction from the [Amazon Customer Reviews Dataset](https://s3.amazonaws.com/amazon-reviews-pds/readme.html).

### Value Proposition:

With the proliferation of e-Commerce, 95% of shoppers are reading online reviews before making a purchase [(1)]. This makes it imperative for managers to actively utilize these data not only to measure performance, but also understand the underlying drivers:

* Are customers rating your product 1-star because it was poorly designed or because of a shipping delay?
* Have reviews improved after you switched to the new supplier?
* Is your customer service team saving the day or eroding your brand? 

While the average star rating for a product or service is useful, these examples demonstrate how invaluable information can be lost if review content is not examined. This issue remains largely unresolved because analyzing reviews at scale is a laborious undertaking. 

## Tools

#### Pre-processing:

* Spacy
* NLTK
* Count Vectorizer
* TF-IDF

#### Topic Modeling:

* LDA
* NMF
* LSA
* Word2Vec
* CorEx

#### Sentiment Analysis:

* VADER

#### Classification Tools/Metrics:

* Logistic Regression
* Naive Bayes
* Precision / Recall
* Confusion Matrix

#### Framework and Visualization Tools:

* T-SNE / Bokeh
* Matplotlib
* Seaborn

[(1)]:https://spiegel.medill.northwestern.edu/_pdf/Spiegel_Online%20Review_eBook_Jun2017_FINAL.pdf
