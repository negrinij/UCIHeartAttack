# UCI Heart Attack Dataset

The Heart Attack UCI database originally contained 76 attributes and was created to detect the presence of heart disease in patients using ML algorithms. In the original database, the target features are integers valued from 0 (no presence) to 4. However, most experiments refer to using this dataset instead, containing only fourteen of the original attributes. Previous works with the UCI database have also concentrated on simply attempting to distinguish presence (values 1,2,3,4 as 1) from absence (value 0) of heart disease. 

In this notebook we follow the same approach, analysing the data as a binary classification problem. From a Machine Learning perspective, this is one of the classics datasets.

Key Remarks:
- Small dataset with approximately three hundred samples and fourteen features
- Overall, the dataset is balanced between both classes of the Target feature. However, there is an expressive unbalance regarding gender, where Males compose ~70% of the data
- The Female samples are mostly from positive Heart Attacks
- The median age for Males with No Heart Attacks is higher than for Males that had Heart Attacks
- A higher concentration of positive Heart Attack samples appears in the region where lower values for Age and Cholesterol and higher values of Heart rate meet
- Data Scaling, OneHotEncoding and the use of KMean for the creation of new features did not improve model generalisation
- In the training set results, the model shows a tendency for False Positives
- Best Model is Logistic Regression with 89,7% Accuracy. The models were finely tuned with Optuna Library
