# CYBERGUARD 2024 SUBMISSION
**Team Members:**
1. Gurmann Singh Ajmani (3rd year student at MIT,Manipal)
2. Ashvin Ganesh (3rd year student at MIT,Manipal)
## Data Preprocessing

1. **Lemmatization**: Reduction of words to their base words for capturing their meaning better
2. **Removal of Stop words**: Remove stopwords (commonly occuring words) which do not contribute to the meaning of the word.
3. **Tokenization**: Tokenize the text to enhance featuer extraction
4. **Label Encoding**: Convert categorical to numeric data type so that the model works as expected
#### Mapping for 'category'
```python
{'Online Financial Fraud': 0, 'Online and Social Media Related Crime': 1, 'Any Other Cyber Crime': 2, 'Cyber Attack/ Dependent Crimes': 3, 'RapeGang Rape RGRSexually Abusive Content': 4, 'Sexually Obscene material': 5, 'Hacking  Damage to computercomputer system etc': 6, 'Sexually Explicit Act': 7, 'Cryptocurrency Crime': 8, 'Online Gambling  Betting': 9, 'Child Pornography CPChild Sexual Abuse Material CSAM': 10, 'Online Cyber Trafficking': 11, 'Cyber Terrorism': 12, 'Ransomware': 13, 'Report Unlawful Content': 14}
```
#### Mapping for 'sub_category'
```python
{'UPI Related Frauds': 0, 'Other': 1, 'DebitCredit Card FraudSim Swap Fraud': 2, 'Internet Banking Related Fraud': 3, 'Fraud CallVishing': 4, 'Cyber Bullying  Stalking  Sexting': 5, 'EWallet Related Fraud': 6, 'FakeImpersonating Profile': 7, 'Profile Hacking Identity Theft': 8, 'Cheating by Impersonation': 9, 'Unauthorised AccessData Breach': 10, 'Online Job Fraud': 11, 'DematDepository Fraud': 12, 'Tampering with computer source documents': 13, 'Hacking/Defacement': 14, 'Ransomware Attack': 15, 'Malware Attack': 16, 'SQL Injection': 17, 'Denial of Service (DoS)/Distributed Denial of Service (DDOS) attacks': 18, 'Data Breach/Theft': 19, 'Cryptocurrency Fraud': 20, 'Online Gambling  Betting': 21, 'Provocative Speech for unlawful acts': 22, 'Email Hacking': 23, 'Business Email CompromiseEmail Takeover': 24, 'Online Trafficking': 25, 'Cyber Terrorism': 26, 'EMail Phishing': 27, 'Online Matrimonial Fraud': 28, 'Damage to computer computer systems etc': 29, 'Website DefacementHacking': 30, 'Ransomware': 31, 'Impersonating Email': 32, 'Intimidating Email': 33, 'Against Interest of sovereignty or integrity of India': 34}
```

6. **Removal of Null values**: Remove all the null values
7. **Extract Input Embeddings**: Convert the text to their respective numeric embeddings

## EDA PERFORMED
1. We used **Boxplots** to identify the outliers/anomalies amongst the categories and subcategories
2. We used **count plots and distribution plots** to identify most common categories and subcategories.
3. We use **WordClouds** to identify the most common words used in messages of each category and subcategory. This helps in identifying the key words and indicators of each distribution
4. We used **heatmaps** to visualize **correlation** between categories and subcategories.


##  VARIOUS NLP MODELS USED:
1. **BERT-BASE**: Created by Google, it has **110 million parameters** and is designed for bidirectional understanding of language through a masked language model.
2. **DISTILBERT**:**Developed by Hugging Face, it is a distilled version of BERT with **66 million parameters**, offering faster performance with minimal accuracy loss.
3. **ROBERTA**:Created by Facebook AI, it has **125 million parameters** and improves BERT with optimizations like larger training data and longer sequences.
4. **FAST TEXT**:Developed by Facebook AI, it has **100 million parameters** and is known for its efficiency in text classification and word embeddings.
5. **XLNET**:Created by Google and Carnegie Mellon University, it has **117 million parameters**  and improves BERT by leveraging permutation-based training.
6. **ELECTRA**:Developed by Google Research, it has **110 million parameters**  and replaces the masked language model with a more efficient token detection task.

## MODEL PERFORMANCE COMPARISION:

### FOR CATEGORY CLASSIFICATION
| Model Name  | Training Accuracy  | Validation Accuracy |
|-------------|--------------------|---------------------|
| **BERT-BASE**   | **84.8%**              | **79.8%**               |
| DISTILBERT  | 83.1%              | 76.7%               |
| ROBERTA     | 82.4%              | 79.4%               |
| FAST TEXT   | 73.0%              | 73.8%               |
| ELECTRA     | 84.8%            | 78.1%              |
| XLNET       | 83.6%              | 78.8%               |

As seen, **BERT-BASE is the best performing model for category classification**.

### FOR SUBCATEGORY CLASSIFICATION
| Model Name  | Training Accuracy  | Validation Accuracy |
|-------------|--------------------|---------------------|
| **BERT-BASE**   | **62.8%**              | **57.7%**               |
| DISTILBERT  | 60.5%              | 54.9%               |
| ROBERTA     | 58.8%              | 65.5%               |
| FAST TEXT   | 37.9%              | 41.8%               |
| ELECTRA     | 63.6%              | 56.6%               |
| XLNET       | 58%                | 55%                 |
Again, **BERT-BASE is the best performing model for subcategory classification**.
