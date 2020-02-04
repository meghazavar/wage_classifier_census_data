
# Goal

The project was completed as part of 1 day ( 8hours) Hackathon ,with a goal to create the best performing predictive model 
on a hold-out sample of data to Predict whether income exceeds $50K/yr based on census data. Also known as "Census Income" dataset.
Our team was  presented with following contrainst .More details on project statement can be found ![here](https://git.generalassemb.ly/mzavar/Hackathon-Good-Fast-Cheap)

### Team Algorithm Constraint
Must use a Random Forest
Your choice of features
Your choice of samples

# About data
The dataset has Rows 32561 columns 14 features, 7 categorical, 6 are numerical features. The target column being predicted is
called 'wage' with 2 values <=50k and  >50k.
Data can be found ![here](https://archive.ics.uci.edu/ml/datasets/adult) 

# Exploratory Data Analysis
### missing data
The seems clean with no missing values with exeption  leading spaces and few '?' on few of the cartofrical data.
we removed '?' with 'unkown' with lack of any better mputing strategy and removed spaces.



### handling categorical data
we converted the ** targe ** column, wage to a numerical eqivalent where  0 meant  wage<=50k and 1 meant wage>50k.

We analysed the categorical columns, identified them as nominal or ordinal columns and converted them to numerical or dropped them if they were repetative , contained non-relevant information to predict the target , as part of EDA

|  column |Categories|Type   | description  | Missing data|  
|---|---|---|---|--- |
| wage  |2   |binary |  Converted to 0 as < 50k and 1  > |   |   |
| workclass|9 |nominal| dummified  |{Private,Local-gov,?,State-gov,Self-emp-inc,Federal-gov,Without-pay, Never-worked}
| education | 60  | ordinal | Dropped as education-num has same information in numeric form  |   |   |
| marital_status  | 5  | nominal  |   | {Married-civ-spouse,Never-married,Divorced,Separated,Widowed,Married-spouse-absent,Married-AF-spouse} |
|occupation |15 |noimnal |
|relationship| 6|nominal | skip for now as it might be same as marital_status|Husband,Not-in-family,Own-child,Unmarried,Wife,Other-relative
|sex |2 |nominal | 0 - Male , 1 - Female | none
|native-country|42 |nominal | United-States= 1 , Other -0 |




# Modelling approach

# Results

| Model  | train accuracy  | test accuracy|  description  |  |
|---|---|---|---|---|
| Baseline  |75.9%   |75.9%  | Model would be right 75 percent of time If it were to predict every incoming record less than 50k, |   |   |
| Random forest 1  | 96.40%  | 82.20%  |   |   |
|  gs1 | 82.28%  |  84.12 |max_depth=10,n_Estimators =200  |
|gs2-7 | no change | no-chage | criterion , min_samples_split ,min_sample_leaf |
|gs1 +fnlwgt| 84.28% | 84.42% | included fnlwgt
|gs1 + feature selection| 84.19 | 84.76 | We simplified model by choosing feature with coeff > 0.1 and < -0.1


# Conclusion
