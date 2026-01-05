## Week 3 – Transformer-Based Sentiment Analysis and Model Comparison

In this week, transformer-based models were explored for financial sentiment classification, with the objective of demonstrating the advantages of deep contextual representations over traditional lexicon-based and bag-of-words approaches.

### Transformer Fundamentals and Fine-Tuning
The FinBERT model, pre-trained on large-scale financial corpora, was fine-tuned on the Financial PhraseBank dataset. Fine-tuning was performed using a stratified train–validation–test split to ensure fair evaluation. The model was trained for three epochs with standard hyperparameters, and the best checkpoint was selected based on weighted F1 score.

### Performance Evaluation
The fine-tuned FinBERT model achieved strong performance on the held-out test set, with an accuracy of approximately 0.90 and a weighted F1 score of approximately 0.90. Per-class evaluation shows balanced precision and recall across positive, negative, and neutral classes, indicating that the model effectively captures both explicit and implicit sentiment cues present in financial text.

### Comprehensive Model Comparison
A unified comparison was conducted across all models developed in the course using the same test set:
- Lexicon-based sentiment analysis (VADER)
- Traditional supervised models using TF-IDF features (Logistic Regression, Naive Bayes, KNN)
- Fine-tuned FinBERT transformer model

The results show a clear performance hierarchy, with lexicon-based methods performing the weakest due to their inability to capture contextual sentiment, traditional machine learning models offering moderate improvements, and the transformer-based FinBERT model significantly outperforming all others. This highlights the effectiveness of contextual embeddings and pre-training on domain-specific corpora for financial sentiment analysis.

### Conclusion
Transformer-based models provide substantial gains in both accuracy and robustness for financial sentiment classification. By leveraging contextual information and domain-specific pre-training, FinBERT overcomes many limitations of lexicon-based and bag-of-words approaches, particularly in handling implicit sentiment and complex financial language. This week’s experiments demonstrate the practical advantages of modern NLP techniques and conclude the progression from rule-based methods to state-of-the-art deep learning models.
