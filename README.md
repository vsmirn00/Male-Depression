# Male Depression
Testing of different Machine Learning Algorithms to determine which one fits the best for predicting the True Positives.

## Table of Contents
- About the Project
- Data Wrangling
- Exploratory Data Analysis
- Using The Algorithms
- Evaluation Metrics
- Conclusion

## About the Project
Depression is one of the most common psychological disorders in modern societies and it especially affects more men than women. In our team, we decided to tackle down this problem by testing different algorithms and finding the key features that can explain why males suffer from depression.

## Data Wrangling
To begin with, we check and clean the data from all the features that might cause an overfitting problem. Focusing our attention on those that are more likely to have a correlation with Depression. First off, we might see that there is an imbalance in the data since we have 17% and 83% of people depressed and not depressed respectively.

## Exploratory Data Analysis
So, we separate the dataset by sex and use different metrics to find out the most relevant features. Once we've chosen those features (Age, education_level and Married), we then tackle the problem of imbalanced data undersampling the not-depressed. Then we standardize the resulting dataset since we don't want our KNN to misclassify the results.

## Using the Algorithms
We define the Confusion Matrix function and proceed with KNN where we must tune the hyperparameter "k" once we check the error rate function to get as many true positives as we can. Actually, KNN gives a great precision. Next, the Logistic Regression performed not so well with the oversampled data. The same happened with Gaussian Naive Bayes, which works pretty well when the complexity is low, but not in this case. On the other hand, the reason why we oversampled our data was mainly that SVM and Decision Trees are highly sensitive to unbalanced datasets. Thus, DT performed really well on this test. In the end, we used SVM which performs a really low score of True Positives if we use linear kernels. However, if we use "RBF" we get the expected result.

## Evaluation Metrics
The main evaluation metrics we used for this project were Confusion Matrix and Classification Reports to check the precision and f1 scores.

## Conclusion
As a matter of fact, studying male depression is a complex problem that must be evaluated in detail. But it seems that using education, age, and marriage as the predictive variables might play a role in estimating whether or not a man can develop depression. Further research would be needed since there should be clearly a better way to test depression. Regarding the algorithms, DT and SVM performed well with balanced data, GNB and LR are more precise in unbalanced datasets without resampling and KNN is a more robust model independently of the dataset.
