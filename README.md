# Customer_Sentiment_Analysis
CSAT Prediction and Recommendation Engine

Download or Review: <a href="Customer_Sentiment_Analysis.ipynb">Customer_Sentiment_Analysis.ipynb</a>

# **Summary**
- Cleaned raw text and categorized in 3 reviews such as cleaned_review, Processed_review and Lemma_review. Finally considered lemma_review for further process as it filters entire text in to crisp and noun format by removing stop words (the, is, etc.), exclamatory symbols, pull stops, etc.
- Extracted weighted scores from different models such as Vader, Textblob and BERT. Compared all three and found BERT score gives accurate prediction as it is associated with external documents and provide scores.
- Normalized all scores to 0 to 1 to avoid inconsistacies during training the models.
- Extracted CSAT scores based on combined of all three models by adding weight to preffered models on its scores. And categorized into High, Low and Neutral for CSAT score. Then encoding the label as 0 for high, 1 for low and 2 for neutral, which is essential to before training the ML model as it supports numericals.
- Splitted Training set and Test set based on 80:20 ratio for Training and Evaluating the model, where Normalized scores of 3 models as input features and CSAT scores as Target feature.
- Applied these variable to intiate training and performed on different classification models such as Random forest, SVM, KNN and Logistic Regression.
- Achieved accuracy of 90% in Random forest and 95% in SVM, KNN models.
- Achieved 100% precission on High and Low category for all 3 models, 86% in Random Forest and 92% in SVM, KNN models for neutral category.
- Recalls values depicts 100% aligned with neutral category, 86% for High class and 50% for Low class, which indicates there is inconsistency in Low scored reviews, nothing but people are deceptive at giving negative reviews.
- Got High F1 score for High and Neutral classes, then otherhand average F1 score in RF model and 100% score in SVM, KNN models. It clearly indicates Model struggling to find low rank reviews.
- Majority of support value (12) to Neutral category, while getting low support to other categories. Clearly showed that Majority of people neither fully satisfied nor fully rejected. It may indicates majority are not interested to give feedback.

## **Issues Distribution:**
<img width="1082" height="601" alt="image" src="https://github.com/user-attachments/assets/b6f3ae7a-194d-4271-b0f1-be9108d2b185" />

#  Testing with Random feedback text, which is not trained
## Example 1
**User Input Text:** My baggage arrived late and no one responded properly
<div>
<p><b>Demo:</b></p>
<img width="815" height="412" alt="image" src="https://github.com/user-attachments/assets/eee87710-d110-472d-80be-e02f2ed3c723" />
</div>

## Example 2
**User Input Text:** Payment system failing frequently
<div>
<p><b>Demo:</b></p>
<img width="810" height="412" alt="image" src="https://github.com/user-attachments/assets/c06c2b82-ca92-4ac0-885a-9339691c6f2a" />
</div>

## Example 3
**User Input Text:** Payment system failing frequently
<div>
<p><b>Demo:</b></p>
<img width="807" height="407" alt="image" src="https://github.com/user-attachments/assets/0583aa43-2545-4382-b66d-d69592dee421" />
</div>
