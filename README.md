# Fetal_Health_Classification_Logistic_Regression

## Note:
This repository is for personal back-up purpose. Download, copy or use of any code will be considered a violation of Georgia Tech's Honor Code.


## Problem Statement

Cardiotocograph exams (CTG) measure changes in the fetal heart rate and draw conditional relationships with uterine contractions. The objective of these exams is to assess the fetus health by monitoring fetal heart rate (FHR), fetal movements, uterine contractions, and numerous other related factors. Results from these exams enable health care professionals to perform additional assessments to ensure fetus’s wellbeing and determine if the baby needs to be delivered by caesarean section or instrumental vaginal birth.
The objective of our project is to analyse the features collected from multiple cardiotocograph exams and their corresponding results to gain an understanding of the critical factors that determine a fetus’s health. The goal of this study is to use this descriptive model to enable healthcare professionals to better predict a fetus’s health in a timely fashion and perform necessary actions to prevent child and maternal mortality.
We will be primarily working with Fetal Health data set acquired from Kaggle [1]. The data set includes 2126 training examples and 21 predictors. This data set was collected by examining features of 2126 cardiotocograph exams. The results of these exams were then classified by three expert obstetricians into three categories, briefly explained below:
• Normal: Features UNLIKELY to be associated with fetal compromise. No further action required.
• Suspect: Features MAY be associated with fetal compromise. Requires further action.
• Pathological: Features are LIKELY to be associated with fetal compromise. Immediate action required.


## Methodology

We started our analysis with a multinomial logistic regression which is followed by a binomial logistic regression for each class. During exploratory analysis, we removed certain predictors with high correlations to avoid multicollinearity in our fitted model. After fitting an initial full model we checked for outliers and multicollinearity in the model. We performed variable selection by using stepwise regression, elastic net regression and lasso regression. Then we evaluated the effect of changing the probability threshold based on the model performance as per different metrics. After choosing models based on the criteria suitable for the class of each response variable, we used all three models to make predictions on a new set of observations. Our models can be used by medical professionals to assess a fetus’s health and perform corrective measures to ensure the fetus’s wellbeing. This can in turn help health care professionals to prevent child or maternal mortality.
One of the major challenges in this data set is that the class of response variables were not evenly distributed. Most observations belonged to the “Normal Fetus”. Having a data set with equal number of classes can help to better recognise the pathological cases, which were heavily outnumbered in this data set. Secondly, in actual conditions, the interpretation of fetus’s CTC varies with respect to the baby’s trimester and labor’s stage. If multiple data sets can be collected for different set of these features, then different models can be fitted to assess a fetus’s health based on its trimester and labor.

## Selected Results
Selected results from employed methodology are shown below. For full results, please refer to the uploaded report. Thank you. 

### Exploratory Data Analysis
![image](https://user-images.githubusercontent.com/70823162/151109275-dfbf94a2-4df3-4eac-a9ba-0a355c4509ec.png)
![image](https://user-images.githubusercontent.com/70823162/151109302-676c82b4-b248-4d80-afa1-5f803ff90911.png)

### Model Fitting
![image](https://user-images.githubusercontent.com/70823162/151109390-8fe1dada-5199-454f-b5a4-389aa847e31e.png)

### Model Evaluation
![image](https://user-images.githubusercontent.com/70823162/151109404-e82a0830-535e-43b0-bbe6-5292da819d69.png)

### Model Selection
![image](https://user-images.githubusercontent.com/70823162/151109423-de5677b0-e633-4812-9067-cfeb5171b523.png)
![image](https://user-images.githubusercontent.com/70823162/151109435-a5093220-1f3b-414d-aa29-0b71f79750b2.png)
![image](https://user-images.githubusercontent.com/70823162/151109469-5234972e-4369-4658-a11e-4e46a5f9de9f.png)
![image](https://user-images.githubusercontent.com/70823162/151109483-f1166404-bba6-4462-9152-b13eee5ecf32.png)

### Model Deployment
![image](https://user-images.githubusercontent.com/70823162/151109514-96ef177c-8118-4cb8-a833-d953c6b19405.png)
![image](https://user-images.githubusercontent.com/70823162/151109522-957d382c-8647-44f5-ad7e-2e485c5f19e0.png)

## Code Execution

**Main Instructions**


* Main data file is “fetal_health.csv”
* There are five folders in total, one for each class of response variable , one for getting predictions from each model and one for multinomial regression.


**01 – Normal Folder:**

* In this folder, following files are present:
1. 6414_Project_Python_AR.pynb
2. 6414_Project_R_Studio_AR.rmd
3. fetal_health.csv
4. Normal.csv
* User should follow these instructions in exact order:
1. Run the 6414_Project_Python_AR.pynb file. This file will output all the relevant figures, tables and output files that will be required in the next section.
2. User should then run 6414_Project_R_Studio_AR.rmd file. This file will require the Normal.csv file. Normal.csv is already present in this folder. This file will also come as an output after running the 6414_Project_Python_AR.pynb file. Running the 6414_Project_R_Studio_AR.rmd will output the relevant figures, tables and output files which will be later used in the report. 



**02 – Suspect Folder:**

* In this folder, following files are present:
1. 6414_Project_Python_AR.pynb
2. 6414_Project_R_Studio_AR.rmd
3. fetal_health.csv
4. Suspect.csv
* User should follow these instructions in exact order:
1. **Skip this step, if Suspect.csv file is already present in the folder**
Run the 6414_Project_Python_AR.pynb file. This file will output all the relevant figures, tables and output files that will be required in the next section.
2. User should then run 6414_Project_R_Studio_AR.rmd file. This file will require the Suspect.csv file. Suspect.csv is already present in this folder. This file will also come as an output after running the 6414_Project_Python_AR.pynb file. Running the 6414_Project_R_Studio_AR.rmd will output the relevant figures, tables and output files which will be later used in the report. 




**03 – Pathological Folder:**


* In this folder, following files are present:
1. 6414_Project_Python_AR.pynb
2. 6414_Project_R_Studio_AR.rmd
3. fetal_health.csv
4. Pathological.csv
* User should follow these instructions in exact order:
1. **Skip this step, if Pathological.csv file is already present in the folder**
Run the 6414_Project_Python_AR.pynb file. This file will output all the relevant figures, tables and output files that will be required in the next section.
2. User should then run 6414_Project_R_Studio_AR.rmd file. This file will require the Pathological.csv file. Pathological.csv is already present in this folder. This file will also come as an output after running the 6414_Project_Python_AR.pynb file. Running the 6414_Project_R_Studio_AR.rmd will output the relevant figures, tables and output files which will be later used in the report. 




**04 – Predictions Folder:**
1. All the csv files in this folder are outputs from the python notebooks executed for each class in above steps.
2. User should run the Model_Selection.ipynb file directly. This file will output the Model_Selection.csv file. 



**05 – Multinomial Logistic Regression:**
1. All the required csv files are in the folder. 
2. User should run the MultinomialLogisticRegression_fetal_health.rmd file directly. 



