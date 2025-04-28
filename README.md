# Sentiment Analysis on Amazon Healthcare Product Reviews

## 📖 Overview
This project focuses on sentiment analysis of Amazon healthcare product reviews using both traditional lexicon-based and modern transformer-based NLP models.

## 📦 Dataset
- **Source**: Amazon 2023 Health & Personal Care Product Reviews
- **Preprocessing**: 
  - Cleaning text (remove emojis, special patterns)
  - Handling short reviews
  - Balancing classes

## 🤖 Models Used
- **VADER** (Lexicon-Based)
- **RoBERTa** (Transformer-Based)
- **DistilBERT**
- **Twitter RoBERTa**
- **XLNet**

## ⚙️ Hybrid Approach
A weighted combination of VADER and RoBERTa scores:
\[
S_{\text{hybrid}} = \alpha \times S_{\text{VADER}} + (1-\alpha) \times S_{\text{RoBERTa}}
]\

## 📈 Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-Score
- Matthews Correlation Coefficient (MCC)
- Cohen’s Kappa

## 🏆 Key Results
| Metric     | VADER | RoBERTa | Hybrid | DistilBERT | Twitter RoBERTa | XLNet |
|------------|-------|---------|--------|------------|-----------------|-------|
| Accuracy   | 78%   | 89%     | 87%    | 83%        | 89%             | 31%   |
| Precision  | 84%   | 92%     | 93%    | 94%        | 88%             | 76%   |
| Recall     | 86%   | 93%     | 88%    | 81%        | 97%             | 3%    |
| F1-Score   | 85%   | 93%     | 90%    | 87%        | 92%             | 6%    |
| MCC Score  | 0.4644| 0.7405  | 0.6900 | 0.6400     | 0.7160          | 0.0211|
| Cohen's Kappa | 0.4636| 0.7405| 0.6874 | 0.6233     | 0.7056          | 0.0047|

## 📊 Statistical Comparison
- Chi-square test showed significant differences between RoBERTa and Twitter RoBERTa ($p < 0.001$).

## 📚 Conclusion
- Transformer-based models significantly outperform lexicon-based models.
- Hybrid approach improves robustness and interpretability.
