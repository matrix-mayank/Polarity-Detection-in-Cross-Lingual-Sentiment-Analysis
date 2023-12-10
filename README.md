# Polarity-Detection-in-Cross-Lingual-Sentiment-Analysis

This repository examines how polarity classification is influenced when it is performed on a corpus of French tweets and its machine-translated English version. The code was written in Python and sentiment analyses were performed on _SpaCy_. 

## Steps Undertaken

1. A corpus of 1.2 million tweets in French (https://github.com/gamebusterz/French-Sentiment-Analysis-Dataset) was downloaded for the purpose of this study.
2. Data cleaning was performed (removing user handles, hashtags, web addresses, punctuations and special characters, numbers and conversion of text to lowercase).
3. Data lemmatization was performed and _n_-grams were obtained from the tweets (_n_ = 1, 2 and 3)
4. TF-IDF vectorizer was used to encode the _n_-grams into numerical vectors
5. Using a 5-fold cross validation, Logistic Regression, Naïve Bayes' Algorithm and Stochastic Gradient Descent were performed.
6. Classification accuracies were compared using confusion matrices.

## Results

**Across features**: Best accuracies of prediction are seen when unigrams are used as features, and decrease with bigrams and trigrams
**Across algorithms**: The highest overall accuracy of 74.19% was obtained by Logistic Regression on unigrams obtained from the machine-translated English corpus. Logistic Regression presents the best results with unigrams and bigrams but Naïve Bayes’ Algorithm serves as a slightly better classifier from Logistic Regression in case of trigrams for both the languages.
**Across languages**: While the accuracies obtained for models trained on English corpus are higher with unigrams, the accuracies obtained for models trained on French corpus are higher with bigrams and trigrams. 

Results from this analysis were published in the proceedings of the 2020 8th International Conference on Reliability, Infocom Technologies and Optimization (Trends and Future Directions) (ICRITO): **M. Sharma, "Polarity Detection in a Cross-Lingual Sentiment Analysis using spaCy," 2020 8th International Conference on Reliability, Infocom Technologies and Optimization (Trends and Future Directions) (ICRITO), Noida, India, 2020, pp. 490-496, doi: 10.1109/ICRITO48877.2020.9197829.**
