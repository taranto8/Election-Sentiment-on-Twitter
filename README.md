# Election-Sentiment-on-Twitter
An analysis of political affiliations and text sentiments on Tweets from November 10th, 2020 about the 2020 presidential election.

The data was collected using the Twitter API and partially hand-labelled. The first 4001 tweets are labelled for political affiliation, and will be the training set for later models to evaluate the political affiliation of the remaining tweets. This is a multi-class classification problem, with "pro-Biden/Anti-Trump" given the value -1, "Neutral" is 0, and "Pro-Trump/Anti-Biden" is encoded as 1.

The analysis involves word-bagging and TF-IDF vector creation to make the problem numerically tractable. Some basic Natural Language Processing techniques are employed, like investigating text sentiment, length, and readability scores are first explored. The correlation of these values against the political affiliation encoding is checked, and features are selected using this. 

Finally, some classical classification algorithms are applied to the feature-selected data, including random forests, SVM, Linear Discriminant Analysis, neural networks, and a bagging ensemble classifier using SVM. Note that the neural networks are the SK-Learn variation so there are few parameters to tune and likely Tensorflow and Keras could do a better job here with more customization. Optimal parameters for each model are found using a grid search.

As a final note, PCA was used to investigate the possibility of dimension reduction before applying our models, but runtime was not significantly effected so we used the full dimension data.
