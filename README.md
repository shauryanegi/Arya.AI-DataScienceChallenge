# Arya.AI-DataScienceChallenge

This dataset has no null values, duplicate features, very few outliers (which I ignored as it did not have a huge impact on the data) so the data preprocessing was fairly simple. The y feature labels were divided into a ratio of 60:40 and therefore oversampling/undersampling of the y feature samples could be ignored.

This github repo has the following files:

1. all_models_score.csv: This excel file was created using the LazyClassifier library to have a "feel" of the performance of all ML models with the data. Since the dataset is small, it would be better to use more "simple" models so we could focus on interpreting the results.

2. accuracy_all_hyperparameters.csv: Hyperparamater tuned 6 classification algorithms to get the best parameters and the "best" model based on accuracy.

3. predictions.xlsx: Predictions Excel file which was obtained after running our best model on the test set.

4. Decision_Tree.png: Our hyperparameter tuned visualized Decision Tree for better understanding of the Decision Tree Model.

5. Arya_Binary_Classification: Python notebook containing all the scripts and codes.

This dataset has ambigious features and therefore using domain knowledge or intuition for feature selection, feature extraction and feature engineering was hard and unclear.
For all the feature selection, I relied on statistical measures. Since the dataset had 57 features and very less samples of data, high dimensionality would unnecessarily create problems like overfitting and less understanding of the features.

## Feature Selection - There are two ways to do this.

## Feature Selection (Statistical) - One way is to use a feature selection algorithm like filtering, wrapper and embedded methods.

## Feature Selection (Domain) - Another way is to use domain knowledge and intuition. For example, we can use the domain knowledge of the target variable to find features that are relevant to the problem. In this case, where we do not know the feature names, I will only use feature selection based on statistics and no domain knowledge or intuiton would be used.

I prefered to use an embedded feature selection tool like LightGBM for feature selection. I although used a Correlation filter method too to find the important features.

This was a fairly simple dataset which was a little odd because it was a little too easy to have a good accuracy on the test set. I decided to go for accuracy over other metrics to see how well I would get the average in a real context. I started by creating my preprocessing pipeline. I split the dataset into a train and test set using an 80:20 split.

## We would be using simple ML models like Logistic Regression, Decision Trees and maybe a Random Forest to better visualize and understand the data after modelling. 


## Based on all the models we saw, we can say that the best model is the Random Forest model based on the test set.

### But here is a question:

## Are we sure that the Random Forest model is the best model based on business requirements?

## Are we more concerned with the accuracy of the model or the interpretability of the model?

## We are concerned with the accuracy-interpretability tradeoff in this case.

## Let me use my intuition: Since we have very limited data, and the accuracies of the simpler models and the more complex models are very similar in the test set, we can say to use a simpler model like Decision Tree for our final dataset to understand the data better as well as to get a better understanding of the model.


## As we can see, the features which are most important for the Random Forest model are conciding with the decision tree which we plot. So, from calculation we can say that features like X52, X53, X55 and X25 etc.


