
# Goal

The project was completed as part of 1 day ( 8hours) Hackathon ,with a goal to create the best performing model on a hold-out 
sample of data to Predict whether income exceeds $50K/yr based on census data. Also known as "Census Income" dataset.

Data can be found ![here](https://archive.ics.uci.edu/ml/datasets/adult) 

Our team was  presented with following contrainst .More details on project statement can be found ![here](https://git.generalassemb.ly/mzavar/Hackathon-Good-Fast-Cheap)
### Team Algorithm Constraint
Must use a Random Forest
Your choice of features
Your choice of samples

#



# Results

| Model  | train accuracy  | test accuracy|  description  |  |
|---|---|---|---|---|
| Baseline  |75.9%   |75.9%  |If your mdoel said people earn less than 50k, model would be right 75 percent of time  |   |   |
| Random forest 1  | 96.40%  | 82.20%  |   |   |
|  gs1 | 82.28%  |  84.12 |max_depth=10,n_Estimators =200  |
|gs2-7 | no change | no-chage | criterion , min_samples_split ,min_sample_leaf |
|gs1 +fnlwgt| 84.28% | 84.42% | included fnlwgt
|gs1 + feature selection| 84.19 | 84.76 | We simplified model by choosing feature with coeff > 0.1 and < -0.1
