# Classifying-Smartphone-Prices

In today’s competitive technology sector, it is very difficult for smaller brands to compete for market share in the smartphone industry. In 2019 the top 5 vendors of smartphones (Sasmsung, Apple, Huawei, Xiaomi and OPPO) had a combined market share reaching over 70%. Thus, this project aimed to classify the price range of a given smartphone based on its features using a variety of machine learning algorithms. The application of such a model could then be used to help provide smaller brands with a better idea on how to provide consumers with an affordable smartphone with features in-line with the most up-to-date technology which in turn would increase sales. The dataset was sourced from Kaggle [1]

## Exploratory Data Analysis (EDA)
* The box-and-whisker plot showed potential outlier values in many features however, the values were found to be correct and not due to reporting error.
<img src="https://github.com/aidenaslam/Classifying-Smartphone-Prices/blob/master/Figure%201.png" width="650" height="400" />

* The histogram distribution of each feature shows that the majority of the features are uniformly distributed
<img src="https://github.com/aidenaslam/Classifying-Smartphone-Prices/blob/master/Figure%202.png" width="650" height="400" />

* There is a positive correlation of 0.64 between fc (front camera megapixels) and pc (primary camera megapixels), a positive correlation of 0.58 between whether the smartphone has 3G or 4G. However, the largest positive correlation is 0.92 which is between price_range and ram. These high correlation values indicate that not all the attributes will be required for modelling and thus as part of the data preparation stage, some attributes will not be selected.
<img src="https://github.com/aidenaslam/Classifying-Smartphone-Prices/blob/master/Figure%203.png" width="650" height="400" />

## Data Preparation
* There were no missing values or outliers in the dataset

* Feature selection was carried out using Chi Squared method and the top-10 features were selected for modelling.
<img src="https://github.com/aidenaslam/Classifying-Smartphone-Prices/blob/master/Figure%204.png" width="150" height="300" />

## Modelling Results
* Three machine learning algorithms were considered: logistic regression, decision tree (with and without pruning) and neural network.

* K-fold cross validation accuracy and AUC were selected as the evaluation criteria

* The best model was the neural network with a testing accuracy of 97.5% and macro-average AUC of 0.98.
<img src="https://github.com/aidenaslam/Classifying-Smartphone-Prices/blob/master/Figure%205.png" width="300" height="100" />

## Limitations and Future Work
* Although many algorithms were used for this dataset and their parameters fine-tuned, further work would include applying sampling techniques to overcome the issue for class imbalances.

* Furthermore, no validation set was used due to the small dataset size. In the future, more data can be supplied, and a validation set can be used to evaluate the models. 





## References
[1]  https://www.kaggle.com/iabhishekofficial/mobile-price-classification#train.csv
