# Project Overview

### Introduction
The international news company World Daily News is going through key executive changes, and are keen on conducting a company-wide overview of its articles. They have thousands of articles from all over the world in various categories that refer to the COVID-19 pandemic, and are particulary interested in the information they can get out of the data. More precisely, World Daily News wants a model that predicts the category of a given text mentioning COVID-19, as well as a model that analyses the articles’ sentiment towards the pandemic and compares the results of the different categories in which the articles lie.

The following project performed by Lumos should aid World Daily News in extracting constructive insights and help them make better qualified decisions.

# Data
The data sent to us by World Daily News can be classified as Big Data. Initially, it amounted to ~470,000 rows, after which we randomly extracted a ~10,000 sample of observations. The reason we did it is because when previously randomly extracting ~50,000 observations, only 200 articles of a specific category were sampled, leading to no observations being included when performing the train/test split in the Machine-Learning (ML) segment. Therefore, we took the minimum number of the smallest category from the complete dataset (i.e. "ESG": 2045), and randomly sampled by this value from the other categories. This way, we ensured a balanced dataset and trust-worthy results of the models.

However, we may still argue that the models we perform could be scaled and potentially improved, and we are more than happy to work together in achieving that in the future.

The dataset consists of three variables:

* Title: The title of the respective article. This column is, on average, clean and does not require extensive pre-processing.
* Content: The content of the respective article. This column required extensive pre-processing, especially since there are numerous articles in languages other than English.
* Category: The category of the respective article. There are only 5 categories, those being: General, Business, ESG, Tech and Science.
Approach
EDA
Firstly, we began with the Exploratory Data Analysis (EDA) phase in order to better observe the data and extract any key information before heading to the next parts of the case. After we gathered as much information as we could, we began with cleaning / pre-processing the data with the help of the nltk package.

# Machine-Learning
As soon as the data was ready to be utilized, we initiated the Machine Learning (ML) phase, which is concerned with the classification task. We have built baseline models, after which we hyperparameter tuned them in order to gain the best performance. We have built with a Multinomial Naive Bayes Classifier, Random Forests, K-Nearest Neighbors Classifier and finally a Gradient Boosting Classifier.

# Sentiment Analysis
The final task was concerned with the sentiment analysis model, and we were able to observe the main factors (e.g., lexicon) that affect specific categories of articles.

# Results
We have observed that the best performing model was the Gradient Boosting Classifier. After the cross-validation process, the model performed with a Precision rate of 74%. Precision was the measurement used to test the models' performances, particularly because the costs of False Positive is high. If the articles aren't classified accordingly to their categories, some World Daily News subscribed readers may miss on specific articles that are labeled otherwise than they anticipate.

The sentiment analysis model has also identified the overall sentiment across the articles. We have identified that "ESG" tends to have the most positive-perceived sentiment, with 70% of the total articles from the respective category sharing that. The least positive category was "Science", with a positive rate of 42%.

# Limitations
No substantial limitations were observed throughout the execution of the project, other than the limited computational power. It may also be observed that the following Notebook may take longer than anticipated to run, however should perform correctly.

We invite you to analyse our code below and observe our thought-process during this case study.
