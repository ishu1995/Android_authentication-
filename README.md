# Android Authenticity Predictor
#### Co Created by [Ayush Jain](https://www.linkedin.com/in/ayush-jain-290b5a141/), Dhongari Pavan Raj Varma, Nadeeha A, Sreenivasan K V, Romaly Das and Yash Patil


<b> Links: </b> [Collab](https://github.com/ishu1995/Android_authentication-/blob/main/TEAM_REALITY_ANDRIOD_AUTHENTICITY_PREDICTION.ipynb), [Dataset](https://drive.google.com/file/d/1g9jc_Uqe894P1tYIARC9uZzVF0t0M6gX/view?usp=sharing), [Presentation](https://drive.google.com/file/d/1RC7g4z8JihggzZwtSkoYODigEBcq7liK/view?usp=sharing), [Techincal Documentation](https://docs.google.com/document/d/1ftD_ItXG7caQg-k7BEWGed_kln0jXhDJ/edit?usp=sharing&ouid=115811449159523075548&rtpof=true&sd=true)

<h3> Business Problem </h3>
The open source nature of Android OS has attracted wider adoption of the system by multiple kinds of developers. This occurrence has further promoted an exponential in the number of devices running the Android OS into different sectors of the economy. Even if this progress brings some amazing technological improvements and simplicity of doing businesses and social relationships, they have however become powerful channel for the unconstrained cyberattacks and surveillance against business and the individual users of these mobile devices. Many cyberattacks techniques exist but attacks through the malicious applications have taken a jump in the recent years. Android malware has done progress in sophistications and intelligence that they have become highly immune to current detection systems. 

<h3> Problem Statement </h3> 
In our problem statement of predicting Android application authenticity, we have a observation about a particular application and using those details we have to predict the application is either Malware (1) or benign (0) as a target class.

<b> Tags: Exploratory Data Analysis, Feature Engineering, Machine Learning, Descision Trees, Esemble Techniques, NLP </b>

<h3> Available Dataset: </h3>
We collect applications from three different sources namely google play, third-party apps and malware dataset. This file contains more than 30,000 Android application features extracted at the time of installation and execution. The dataset contains the name of the features and .apk file corresponding to it extracted permissions with respective package. Applications are collected from Google's play store, hiapk, app china, Android, mumayi , gfan slideme, and pandaapp. 

The features which we have in our dataset are: 

1. Name of the Application 
2. Category of the Application 
3. Number of related application 
4. Description of the application 
5. Ratings
6. Number of Ratings 
7. Price of application 
8. Dangerous Permission Count 
9. Safe Permission Count 
10. Types of permission needed while installing the application 

## Approach towards project 
We start our project by doing the research on how permissions plays a important role in predicting the application status and types of attacks which generally happen through such malicious application. 

Once we got the idea, we started working to prepare our dataset by doing cleaning and preprocessing in which we handle the duplicate the observations, handled the null values using imputer package, and removing the non contributing columns to target class. 

After the preparation, we did EDA on the dataset and come with some really good insights on the Price, Category, Ratings and Permission Columns. Once EDA is done, we have worked on the description feature using NLP model. This model was built to check if text columns can also help in predicting the target class. We run the XG Boost model and got around 70% accuracy after tuning the hyperparameter tuning. 


Now the time has come to fi the model and evaluate the model using the evaluation metrices. We used below models to train and test our dataset: 
1. KNN
2. Random Forest 
3. Logistic 
4. GBM 
5. XG Boost

Also, the model with Probability derived column which we generated from textual data give us an increment of 8% as compared to the normal model without text derived column. 

<h4> Conclusion </h4>
The model which best worked for us is XGBoost which give us better accuracy, precision, recall. We got in total 89% accuracy from the model.   

<b> References: [Andriod Application Security](https://www.researchgate.net/publication/318326749_Predicting_Android_Application_Security_and_Privacy_Risk_with_Static_Code_Metrics), [Mobile Malware Detection](https://www.mdpi.com/2079-9292/10/13/1606/pdf)</b>
