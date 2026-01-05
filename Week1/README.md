## Week 1 – NLP Fundamentals and Lexicon-Based Sentiment Analysis

In this week, foundational natural language processing techniques were explored through lexicon-based sentiment analysis on financial news text. The goal was to understand the limitations of rule-based sentiment methods and motivate the need for supervised learning approaches introduced in later weeks.

### Text Preprocessing
A custom text preprocessing pipeline was implemented to handle financial text effectively. The preprocessing steps include text normalization, contraction expansion, tokenization, and stopword removal. Financially meaningful words such as *profit*, *loss*, *growth*, *gain*, and *decline* were intentionally retained during stopword filtering, as these terms carry sentiment in financial contexts. Numeric tokens and decimal values were also preserved to maintain important quantitative information present in financial news. Aggressive stemming or lemmatization was avoided to prevent distortion of domain-specific terms.

### Lexicon-Based Sentiment Analysis
Three lexicon-based sentiment approaches were applied:
- **VADER**, which provides rule-based sentiment scores suited for short text.
- **TextBlob**, which computes polarity using a statistical sentiment model.
- A **custom financial sentiment lexicon**, designed to capture domain-specific sentiment words common in financial reporting.

An ensemble sentiment score was computed by averaging the outputs of these three methods, providing a more balanced sentiment estimate than any single approach.

### Evaluation and Analysis
The lexicon-based ensemble was evaluated on the Financial PhraseBank dataset. Overall accuracy was reasonable for strongly polar statements; however, performance was dominated by neutral predictions due to the highly imbalanced nature of the dataset. The confusion matrix and error analysis reveal that many factually phrased financial statements with implicit sentiment (e.g., profit growth or reduced losses) are predicted as neutral. This highlights a fundamental limitation of lexicon-based methods, which rely on explicit sentiment cues and cannot effectively capture contextual or implicit sentiment.

### Conclusion
Lexicon-based sentiment analysis offers interpretability and requires no training data, making it useful as a baseline. However, its inability to handle implicit sentiment and complex financial language significantly limits its effectiveness. These observations motivate the use of supervised machine learning models explored in Week 2, which are better suited for capturing nuanced sentiment patterns in financial text.
