# heart_disease_prediction
Heart Disease UCI dataset

This is experiment to simply predict presence of heart disease from its absence. 

### 1. About dataset:
The dataset is provided on Kaggle (https://www.kaggle.com/ronitf/heart-disease-uci). and can be otained from UCI machine learning repository (https://archive.ics.uci.edu/ml/datasets/Heart+Disease).

The data containes total 14 attributes which are listed below.

#### Description of attributes
1. age: age in years
2. sex: sex (1 = male; 0 = female)
3. cp: chest pain type
    > Value 1: typical angina
    Value 2: atypical angina
    Value 3: non-anginal pain
    Value 4: asymptomatic

4. trestbps: resting blood pressure (in mm Hg on admission to the hospital)
5. chol: serum cholestoral in mg/dl
6. fbs: (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false)
7. restecg: resting electrocardiographic results
    > Value 0: normal
    Value 1: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV)
    Value 2: showing probable or definite left ventricular hypertrophy by Estes' criteria
8. thalach: maximum heart rate achieved
9. exang: exercise induced angina (1 = yes; 0 = no)
10. oldpeak = ST depression induced by exercise relative to rest
11. slope: the slope of the peak exercise ST segment
    > Value 1: upsloping
    Value 2: flat
    Value 3: downsloping
12. ca: number of major vessels (0-3) colored by flourosopy
13. thal: 3 = normal; 6 = fixed defect; 7 = reversable defect
14. target: diagnosis of heart disease (angiographic disease status)
    > Value 0: < 50% diameter narrowing
    Value 1: > 50% diameter narrowing
    


### 2. Data preprocessing and visualization:

The data is visualized with various graphs for its distribution of attributes. 
#### One Hot Encoding: 
The attribute 'slope' and 'thal' are the categorical variables for which numerical values are provided in the data.
As these attributes correspond to the slope of the peak exercise ST segment and the type of defect, respectively, the categories do not represent any order and are not graded values. To make model more efficient, thus, I have considered one-hot-encoding for these attributes.

### 3. Applying Naive Beyes algorithm
The basic probablistic model of naive beyes is applied and the model performance is analysed for various 'smoothig' and 'fit_prior' combinations. Smoothing is required to avoid zero probability outcome in case of inadequate data value variance.
The best model was selected with 'smoothing' value of 1 and fitted with priors.

### 4. Results:
The **accuracy of the model is 85.2%** with precision of prediction 83% for absence of heart disease and 87% for presence of heart disease.
This model successfully classifies the patients based on 14 given attributes into presence and absenece of heart disease. 

### Acknowledgement:
Creators:  
Hungarian Institute of Cardiology. Budapest: Andras Janosi, M.D.  
University Hospital, Zurich, Switzerland: William Steinbrunn, M.D.  
University Hospital, Basel, Switzerland: Matthias Pfisterer, M.D.  
V.A. Medical Center, Long Beach and Cleveland Clinic Foundation: Robert Detrano, M.D., Ph.D.  
Donor:  
David W. Aha (aha '@' ics.uci.edu) (714) 856-8779  
