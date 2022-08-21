# Insurance Claim Fraud Detection

### Problem Statement

To build a classification methodology to determine whether a customer is placing a fraudulent insurance claim.

### Architecture

![My Image](./appFlow.png)

The Csv file(s) from the data batches path is read, the validation,transformation steps are performed and the cleaned data is exported from a sqlite database to a csv file, and this csv file serves as the training data for the ML models.

Clustering: KMeans algorithm is used to create clusters in the preprocessed data and the optimum number of clusters is selected by plotting the elbow plot. The idea behind clustering is to implement different algorithms for each cluster.

![ELbow](./preprocessing_data/K-Means_Elbow.PNG)

After the clusters have been created, we find the best model for each cluster by using two algorithms, “SVM” and "XGBoost". For each cluster, both the algorithms are passed with the best parameters derived from GridSearch and the models for each cluster are saved for prediction.

The prediction csv file is created at the path _fraudDetection/Prediction_Output_File/Predictions.csv_

### Deployment 🚀

A frontend application is developed using the flask framework and deployed to Heroku cloud platform.

## App URL:

https://app-frauddetection.herokuapp.com/

---

### Links 🔗

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/imsaw)

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/im_SsAaWw)
