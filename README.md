# Fishing Out Phishing Websites: A URL Classification Model


# **Elevator Pitch**

This project uses machine learning to recommend a set of models for predicting phishing websites. The motivation for this project is to reduce the loss of personal and financial information by vulnerable online shoppers who often cannot distinguish a legitimate website form its phishing counterpart. The best performing model predicts legitimate websites 91% of the time. 


![image](https://user-images.githubusercontent.com/115121410/230516092-c7a112ec-1722-4bf7-b896-9142f608bb7c.png)


# **Business Understanding**
Online shoppers lose money, time, and personal identifiable information to malicious websites because they are often unable to differentiate between a legitimate website and a phishing site. Cybercrimes have become rampart due to the increase in data value, a recent study "revealed that the share of phishing sites detected using HTTPS increased from 32% in 2021 to over 49% last year – a rise of nearly 56%" (InfoSecurity Group). The model built within this project can be adopted across different industries; however, this project is geared to the retail/e-commerce industry and would be useful for vulnerable consumers to protect themselves from cybercrimes.

 ![image](https://user-images.githubusercontent.com/115121410/230516995-1beb54ed-dc32-42e5-b015-5f7c56ef1261.png)

# **Data Understanding**
This project uses data sourced from Phish Tank, Open Phish, Alexa and Yandex to build a model that classifies websites as legitimate or as phishing websites. Data was downloaded from Kaggle, an online platform for data scientists. Kaggle sourced the dataset originally from Engineering Application of Artificial Intelligence, an academic journal. Dataset was constructed in May 2020, the dataset used for this project is from the latest dataset publication in July 2021

The dataset contains information of 11430 URLs from both phishing and legitimate websites. The data came with 89 columns extracted from the websites page content, structure and URL syntax The dataset is balanced, i.e., it contains 50% phishing and 50% legitimate URLs. Some of the features in the dataset include domain age, WHOIS registered domain, page rank, ratio internal /external redirection, page rank (from open PageRank) among others.

# **Modelling and Evaluation**
The folowing models where usd for the website classifiation problem:
- Logistic Regression (Baseline model)
- Decision Trees and Random Forest
- XGBoost (Best model)

The baseline model presdicted legitimate websites 83% of the time while the best performing model did the same 91% of the time. 
Among all the URLs predicted by the baseline model, only 82% of them were true positives (i.e, indeed legitimate websites).
Among all the URLs predicted by the best performing model, 91% of them were indeed legitimate websites.


# **Conclusion**
The best performing model is the XGBoost. The evaluation metrics from the training data shows all the models might be overfitting, although the overfitting is not significant for some models, it will be interesting to see how the model adjusts with an increase in the availability of datasets.

The final model can be used by vulnerable shoppers to validate a suspicious URL before commiting to shop on the website.

This project can be expanded upon in the following ways:
- Increasing the amount of dataset for a more robust model
- Classsification of phishng emails
- Classsification of phishng emails
- Classification of shortened URLs, e.g URLs that have been shortened using Bitly, TinyURL
- Embeding the URL detection model to a web browser
- Creating a model that contains actionable detection that reports or close domains of phishing URLs

# **Repository Navigation**
The repository contains two folders and three files, see description below:
- Archive: This is a folder, it conains draft notebooks used in preliminary coding
- Data: This is a folder that contains the data used for modelling
- Capstone_SunmiOgundairo.ipnynb: This is a jupyter notebook that contains all the code and explanation  of the reason behind methodologies used
- Capstone_SunmiOgundairo.pptx: This is a powerpoint deck with presentaion slides that explains the model and results to nontechnical audiences
- ReadMe: This is a summary file with that provides a general overview of the project 
