## Week 2 – Supervised Learning

In this week, supervised learning models were trained and evaluated for financial sentiment classification using the Financial PhraseBank dataset. Unigrams and bigrams were chosen for TF-IDF feature extraction because this representation effectively balances term importance with local context information, while remaining suitable for use with linear models.

The performance of three classifiers was compared: Logistic Regression, Multinomial Naive Bayes, and K-Nearest Neighbors. Logistic Regression consistently achieved the best weighted F1 score on the validation set, outperforming both Naive Bayes and KNN. This behavior is expected, as Logistic Regression handles high-dimensional sparse TF-IDF feature vectors well and is less sensitive to noise compared to distance-based methods such as KNN.

The dataset is highly class-imbalanced, with the neutral class dominating. Consequently, while the model performs well on neutral samples, recall for the positive and negative classes is relatively lower. This behavior is reflected in the confusion matrix and failure case analysis, where many factually phrased financial statements with implicit sentiment are predicted as neutral. Such ambiguity is inherent to financial news text and represents a limitation of bag-of-words-based approaches.
