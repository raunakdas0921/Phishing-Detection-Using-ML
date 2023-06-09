# Phishing-Detection-Using-ML


## Objective

A phishing website is a common social engineering method that mimics trustful uniform resource locators (URLs) and webpages. The objective of this project is to train machine learning models and deep neural nets on the dataset created to predict phishing websites. Both phishing and benign URLs of websites are gathered to form a dataset and from them required URL and website content-based features are extracted. The performance level of each model is measures and compared.

## Data Collection

The set of phishing URLs are collected from opensource service called PhishTank. This service provide a set of phishing URLs in multiple formats like csv, json etc. that gets updated hourly. To download the data: https://www.phishtank.com/developer_info.php. From this dataset, 5000 random phishing URLs are collected to train the ML models.

The legitimate URLs are obatined from the open datasets of the University of New Brunswick, https://www.unb.ca/cic/datasets/url-2016.html. This dataset has a collection of benign, spam, phishing, malware & defacement URLs. Out of all these types, the benign url dataset is considered for this project. From this dataset, 5000 random legitimate URLs are collected to train the ML models.

The above mentioned datasets are uploaded to the 'DataFiles' folder of this repository.

## Feature Extraction

he below mentioned category of features are extracted from the URL data:

Address Bar based Features
          In this category 9 features are extracted.
Domain based Features
          In this category 4 features are extracted.
HTML & Javascript based Features
          In this category 4 features are extracted.
The details pertaining to these features are mentioned in the URL Feature Extraction.ipynb.

So, all together 17 features are extracted from the 10,000 URL dataset and are stored in '5.urldata.csv' file in the DataFiles folder.
The features are referenced from the https://archive.ics.uci.edu/ml/datasets/Phishing+Websites.


## End Result

From the obtained results of the above models, XGBoost Classifier has highest model performance of 86.4%. So the model is saved to the file 'XGBoostClassifier.pickle.dat'

## Next Steps

This project can be further extended to creation of browser extention or developed a GUI which takes the URL and predicts it's nature i.e., legitimate of phishing. As of now, I am working towards the creation of browser extention for this project. And may even try the GUI option also. The further developments will be updated at the earliest.
