# StarbucksCapstoneChallenge

[Udacity Data Scientist Nanodegree](https://www.udacity.com/course/data-scientist-nanodegree--nd025)

## Project Overview
Customer satisfaction drives business success and data analytics provides insight into what customers think. For example, the phrase "[360-degree customer view](https://searchsalesforce.techtarget.com/definition/360-degree-customer-view)" refers to aggregating data describing a customer's purchases and customer service interactions.
  
The Starbucks [Udacity Data Scientist Nanodegree](https://www.udacity.com/course/data-scientist-nanodegree--nd025) Capstone challenge data set is a simulation of customer behavior on the Starbucks rewards mobile application. Periodically, Starbucks sends offers to users that may be an advertisement, discount, or buy one get on free (BOGO). An important characteristic regarding this dataset is that not all users receive the same offer.
  
## Problem Statement / Metrics 
The problem that I chose to solve is to build a model that predicts whether a customer will respond to an offer. My strategy for solving this problem has four steps. First, I will combine the offer portfolio, customer profile, and transaction data. Each row of this combined dataset will describe an offer's attributes, customer demographic data, and whether the offer was successful. Second, I will assess the [accuracy](https://developers.google.com/machine-learning/crash-course/classification/accuracy) and [F1-score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html) of a naive model that assumes all offers were successful. This provides me a baseline for evaluating the performance of models that I construct. Accuracy measures how well a model correctly predicts whether an offer is successful. However, if the percentage of successful or unsuccessful offers is very low, [accuracy is not a good measure of model performance](https://www.manning.com/books/practical-data-science-with-r). For this situation, evaluating a model's [precision and recall](https://towardsdatascience.com/beyond-accuracy-precision-and-recall-3da06bea9f6c) provides better insight to its performance. I chose the F1-score metric because it is "[a weighted average of the precision and recall metrics"](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html). Third, I will compare the performance of [logistic regression](https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc), [random forest](https://towardsdatascience.com/the-random-forest-algorithm-d457d499ffcd), and [gradient boosting](https://machinelearningmastery.com/gentle-introduction-gradient-boosting-algorithm-machine-learning/) models. Fourth, I will refine the parameters of the model that has the highest accuracy and F1-score.  

## Results Summary
- Model ranking based on training data [accuracy](https://www.datarobot.com/wiki/accuracy/)  
    1. RandomForestClassifier model accuracy: 0.742
    2. GradientBoostingClassifier model accuracy: 0.736
    3. LogisticRegression model accuracy: 0.722
    4. Naive predictor accuracy: 0.471
- Model ranking based on training data [F1-score](https://en.wikipedia.org/wiki/Precision_and_recall)  
    1. RandomForestClassifier model f1-score: 0.735
    2. GradientBoostingClassifier model f1-score: 0.725
    3. LogisticRegression model f1-score: 0.716
    4. Naive predictor f1-score: 0.640
- Results suggest that the random forest model has the best training data accuracy and F1-score  


## Files  
- Starbucks_Capstone_notebook.ipynb  
  - [Jupyter notebook](https://jupyter.org/) that performs three tasks:  
    - Combines offer portfolio, customer demographic, and customer transaction data  
    - Generates training customer demographic data visualizations and computes summary statistics  
    - Generates logistic regression, random forest, & gradient boosting models  
- clean_data.py  
  - Python software that combines offer portfolio, customer demographic, and customer transaction data  
- exploratory_data_analysis.py  
  - Generates training customer demographic data visualizations and computes summary statistics  
	
## Python Libraries Used
-[Python Data Analysis Library](https://pandas.pydata.org/)  
-[Numpy](http://www.numpy.org/)  
-[Matplotlib](https://matplotlib.org/)  
-[seaborn: Statistical Data Visualization](https://seaborn.pydata.org/)  
-[re: Regular expression operations](https://docs.python.org/3/library/re.html)  
-[os — Miscellaneous operating system interfaces](https://docs.python.org/3/library/os.html)  
-[scikit-learn: Machine Learning in Python](https://scikit-learn.org/stable/)  
-[Joblib: running Python functions as pipeline jobs](https://joblib.readthedocs.io/en/latest/)  
  
