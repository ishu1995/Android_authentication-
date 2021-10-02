# Android_authentication-
In our problem statement of predicting Android application authenticity, we have a observation about a particular application and using those details we have to predict the application is either Malware (1) or benign (0) as a target class.

The features which we have in our dataset are: 

Name of the Application 
Category of the Application 
Number of related application 
Description of the application 
Ratings
Number of Ratings 
Price of application 
Dangerous Permission Count 
Safe Permission Count 
Types of permission needed while installing the application 

We start our project by doing the research on how permissions plays a important role in predicting the application status and types of attacks which generally happen through such malicious application. 

Once we got the idea, we started working to prepare our dataset by doing cleaning and preprocessing in which we handle the duplicate the observations, handled the null values using imputer package, and removing the non contributing columns to target class. 

After the preparation, we did EDA on the dataset and come with some really good insights on the Price, Category, Ratings and Permission Columns. Once EDA is done, we have worked on the description feature using NLP model. This model was built to check if text columns can also help in predicting the target class. We run the XG Boost model and got around 70% accuracy after tuning the hyperparameter tuning. 

Now the time has come to fi the model and evaluate the model using the evaluation metrices. We used below models to train and test our dataset: 
KNN
Random Forest 
Logistic 
GBM 
XG Boost
Also, the model with Probability derived column which we generated from textual data give us an increment of 8% as compared to the normal model without text derived column. 

The model which best worked for us is XGBoost which give us better accuracy, precision, recall. We got in total 89% accuracy from the model.   
