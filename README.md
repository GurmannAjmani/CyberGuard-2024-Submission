# Data Analysis Project

## Overview
This project analyzes various categories and subcategories of cyber crimes. The dataset includes multiple columns, some of which are categorical in nature. To facilitate analysis and visualization, categorical labels have been converted to integer representations based on their frequency of occurrence.

## Label Mapping Strategy

The following strategy was used to map categorical labels to integers:
1. **Counting Occurrences**: For each target column, the occurrences of each unique label were counted.
2. **Mapping Labels to Integers**: A mapping was created where the most frequent label is assigned `0`, the second most frequent label is assigned `1`, and so forth.
3. **Replacing Original Labels**: The original labels in the DataFrame were replaced with their corresponding integer values using the mapping.

### Target Columns Mapped

#### Mapping for 'category'
```python
{'Online Financial Fraud': 0, 'Online and Social Media Related Crime': 1, 'Any Other Cyber Crime': 2, 'Cyber Attack/ Dependent Crimes': 3, 'RapeGang Rape RGRSexually Abusive Content': 4, 'Sexually Obscene material': 5, 'Hacking  Damage to computercomputer system etc': 6, 'Sexually Explicit Act': 7, 'Cryptocurrency Crime': 8, 'Online Gambling  Betting': 9, 'Child Pornography CPChild Sexual Abuse Material CSAM': 10, 'Online Cyber Trafficking': 11, 'Cyber Terrorism': 12, 'Ransomware': 13, 'Report Unlawful Content': 14}
```

#### Mapping for 'sub_category'
```python
{'UPI Related Frauds': 0, 'Other': 1, 'DebitCredit Card FraudSim Swap Fraud': 2, 'Internet Banking Related Fraud': 3, 'Fraud CallVishing': 4, 'Cyber Bullying  Stalking  Sexting': 5, 'EWallet Related Fraud': 6, 'FakeImpersonating Profile': 7, 'Profile Hacking Identity Theft': 8, 'Cheating by Impersonation': 9, 'Unauthorised AccessData Breach': 10, 'Online Job Fraud': 11, 'DematDepository Fraud': 12, 'Tampering with computer source documents': 13, 'Hacking/Defacement': 14, 'Ransomware Attack': 15, 'Malware Attack': 16, 'SQL Injection': 17, 'Denial of Service (DoS)/Distributed Denial of Service (DDOS) attacks': 18, 'Data Breach/Theft': 19, 'Cryptocurrency Fraud': 20, 'Online Gambling  Betting': 21, 'Provocative Speech for unlawful acts': 22, 'Email Hacking': 23, 'Business Email CompromiseEmail Takeover': 24, 'Online Trafficking': 25, 'Cyber Terrorism': 26, 'EMail Phishing': 27, 'Online Matrimonial Fraud': 28, 'Damage to computer computer systems etc': 29, 'Website DefacementHacking': 30, 'Ransomware': 31, 'Impersonating Email': 32, 'Intimidating Email': 33, 'Against Interest of sovereignty or integrity of India': 34}
```

### Plots Created
The following strategy was used during inference from the dataset using plots:
1. **Boxplots**: For each target column, the distribution of the the numerical data with respect to the target column is shown as a boxplot.
2. **Class Counts**: For each target column, the distribution of the the class counts of the target variable is shown as a bar graph.
3. **Heatmap**: The correlation between the 2 target columns is depicted as a heatmap.
3. **Numerical Distribution**: The numerical columns are graphed as a histplot to visualize the distribution of occurances.
