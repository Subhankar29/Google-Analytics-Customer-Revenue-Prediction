# Google-Analytics-Customer-Revenue-Prediction

## Task asigned: 
our task was to predict the Gstore's revenue from those customers which is the predicted values are natural log of sum of all transactions per user.

The steps taken by me to accomplish this are as follows:

## Data Pre-processing

The dataset contains JSON strings which is very difficult to process. For that first I first made separate columns for each subsection and filled the value accordingly. 

* Since the dataset was large, I had to drop all the irrelevant datas that will contribute very less in the training and making the prediction. 
* While flatenning the dataset many empty values were formed. I had to fill all the empty values with NaN values. 
* Each columns are analysed and the columns which contain constant values are removed from the dataset.
* Then the training data was divided into dev set and cross validation set in the ratio roughly 8:2.

## Model

* After preprocessing of the data, I had to choose the best model that should work with the given problem. 
* Here I have chosen Ensemble learning. Ensemble learning helps improve machine learning results by combining several models. This approach allows the production of better predictive performance compared to a single model. 
* For gradient boosting agorithm I have used LightGBM.
* Whenever working with a large dataset there is always chances of overfitting. Hence I used XGBoost because it is a regularised boosting model and hence reduces overfitting. 
* I have used K-Fold Cross Validation which randomly break the dataset into k partitions. For each of k partitions, use k-1 folds for training and the remaining one for testing. The advantage of K-Fold Cross validation is that all the examples in the dataset are eventually used for both training and testing. Finally, the true error is estimated as the average error rate. 
* The Final submission is done in submission.csv file for which I have added it in the jupyter notebook. 

Find the complete code: https://github.com/Subhankar29/Google-Analytics-Customer-Revenue-Prediction/blob/master/Google_GStore_Prediction_Submission.ipynb
