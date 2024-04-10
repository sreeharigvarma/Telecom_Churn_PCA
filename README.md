# Telecom Churn CaseStudy Using PCA and RF
PCA and Random Forest were performed on the Telecom_Churn dataset as part of an assignment coursework for PG in Machine Learning and AI from IIIT Bangalore.


## Table of Contents
* [Problem Statement](#problem-statement)
* [General Information](#general-information)
* [Business Understanding](#business-understanding)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Contact](#contact)

<!-- You can include any other section that is pertinent to your problem -->

## Problem Statement
In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.

For many incumbent operators, retaining high profitable customers is the number one business goal. To reduce customer churn, telecom companies need to predict which customers are at high risk of churn. In this project, you will analyze customer-level data of a leading telecom firm, build predictive models to identify customers at high risk of churn, and identify the main indicators of churn.

Your goal is to build a machine-learning model that is able to predict churning customers based on the features provided for their usage.



## General Information
- Customers usually do not decide to switch to another competitor instantly, but rather over a period of time (this is especially applicable to high-value customers). In churn prediction, we assume that there are three phases of customer lifecycle :
  
1. The ‘good’ phase: In this phase, the customer is happy with the service and behaves as usual.

2. The ‘action’ phase: The customer experience starts to sore in this phase, for e.g. he/she gets a compelling offer from a competitor, faces unjust charges, becomes unhappy with service quality etc. In this phase, the customer usually shows different behaviour than the ‘good’ months. It is crucial to identify high-churn-risk customers in this phase, since some corrective actions can be taken at this point (such as matching the competitor’s offer/improving the service quality etc.)

3. The ‘churn’ phase: In this phase, the customer is said to have churned. In this case, since you are working over a four-month window, the first two months are the ‘good’ phase, the third month is the ‘action’ phase, while the fourth month (September) is the ‘churn’ phase.


- PCA, PCA with Logistic Regression, Random Forest etc. are a few models attempted to protect churn_probability
- The project is done as part of coursework in the Machine Learning chapter. 
- Data imbalance is handled using SMOTE


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## Business Understanding
In the case of telecom churn prediction, where you want to identify customers at risk of leaving, the most important metric between specificity, sensitivity, and accuracy depends on the business cost associated with each outcome. Here's a breakdown:

* Accuracy: This reflects the overall correctness of the model's predictions (both identifying churners and non-churners correctly). It's a good general measure but might not tell the whole story in this case.

* Sensitivity: This refers to the model's ability to correctly identify true churners (i.e., how many customers predicted to churn actually do churn).  High sensitivity is ideal for churn prediction.

Why?  Because the cost of missing a churner (who then leaves and takes their business elsewhere) can be significant.  The telecom company loses revenue, and the churner might become a customer of a competitor.

Specificity: This refers to the model's ability to correctly identify non-churners (i.e., how many customers predicted to stay actually do stay). High specificity is desirable, but it's less crucial than high sensitivity in this context. Misclassifying a non-churner as a churner might lead to unnecessary customer retention efforts, but it doesn't cause a direct loss of revenue or a new customer for the competitor.
In conclusion, while accuracy is a good overall measure, for churn prediction,  focus on achieving high sensitivity.  This ensures you catch as many true churners as possible and allows the telecom company to take proactive steps to retain them.

## Conclusions
* We have cleaned and visualized the data, treated for data_imbalance and imputed values as and when required and prepared the model for training. 
* After trying several models we have observed that for achieving the best sensitivity, which is our ultimate goal, the classic Logistic regression with PCA models performs well. The model delivered a sensitivity index of approx 84% on test data. Also, we have good accuracy of approx 88%. If only Accuracy is important Random Forest model was able to get approx 93% on test data.



## Technologies Used
- pandas
- seaborn
- matplotlib
- sci-kit learn
- numpy

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact
sreeharipkgvarma@gmail.com


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->
