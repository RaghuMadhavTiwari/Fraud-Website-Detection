# Fraud-Website-Detection
Repository for Fraud Website Detection Classification ML model and dashboard


Nowadays, the internet has integrated seamlessly into our daily lives, but it has also
given rise to possibilities for harmful actions like phishing. Multiple users purchase
products online and make payments through unsafe websites, through which scammers
try to steal information from people and organizations, such as account IDs, usernames,
passwords, employee details, etc., through these fake or phishing websites. A phishing
website looks similar to the original one as cybercriminals copy the theme, information,
graphics, and other intricate details.
In order to prevent people and organizations from such fake websites, a model using supervised
machine learning techniques that is capable of finding the phishing website was developed and
built a beautiful dashboard to analyze key features (such as special characters in url, character
set, server response, IP addresses, etc) to detect phishing website using Tableau Public.


## Dashboard
### The Process of creating the dashboard was as follows -
1. Create different tables for each analysis in MS Excel [All tables are added in the repo]
2. Import one table at a time and create a sheet containing appropriate visualization
3. Continue building sheets for all the tables
4. Build a dashboard containing all the sheets

### Our dashboard is capable of analyzing the following
1. Analyze the top Character sets, with Website type to see the character encoding
standard amongst the website types
2. Countrywise malicious website percentage highlighting how many out of total websites
are malicious in a particular country in a map
3. Registration and update dates of both the website types
4. Top servers that are used to create a website
5. Number of special characters used in both types of websites
6. A holistic analysis of servers and website type according to 10 features including IP
Packets, DNS Packets, etc.



## Classification model
### A classification model was built on Python and Recall was used as final metric to measure
model performance.
1. Choosing the metric - On wrongly predict the website to be genuine instead of a fraud
one would cause a massive problem. Hence, the cost of False Negatives is much higher
than the cost of False Positives. Cost of False Positive > Cost of False Negative. We
need to focus on getting high recall and at the same time, can evaluate the model
performance by looking at other metrics like accuracy, precision, and F1 score.
2. Basic data exploration indicated the followinga.
Missing values in few features which were imputed
- Classes were imbalance which was tackled using SMOTE
- 1 feature was highly correlated with few other features and was dropped
- Many features had outliers also
3. Data cleaning and feature engineering includes:
- Imputing null values
- Dropping duplicates
- Label encoding
- Converting to appropriate datatypes
4. A machine learning classification model was developeda.
Training and testing data were separated
- SMOTE was applied to create new dataset for handling class imbalance
- Many statistical algorithms were trained and tested and XGBoost had the best
recall and overall metrics and was hence chosen as the final model
5. How the model was improved -
- Using SMOTE to handle class imbalance
- Dropping highly correlated feature
- Finding best parameters fo the statistical algorithms during training
- Use of k-fold validation
