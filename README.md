# Machine Learning Project
## Detection of Parkinson's Disease
### Table of Contents
- [Description](#Description)
- [Data Pre Processing](#Data-Pre-Processing)
- [Algorithms](#Algorithms)
- [Accuracy of best algorithm](#Accuracy-of-best-algorithm)
----------------------------------------------------------------------
## Description
In this paper, i present a machine learning model that seeks to achieve the best possible accuracy in detecting Parkinson's disease.
This dataset is from UCI Machine Learning Repository.This dataset is composed of a range of biomedical voice measurements from 31 
people, 23 with Parkinson’s disease (PD). Each column in the table is a particular voice measure, and each row corresponds one of 
195 voice recording from these individuals (“name” column). The main aim of the data is to discriminate healthy people from those 
with PD, according to “status” column which is set to 0 for healthy and 1 for PD.
We should have some idea about the features. Let’s have a look.

     name - ASCII subject name and recording number
     MDVP:Fo(Hz) - Average vocal fundamental frequency
     MDVP:Fhi(Hz) - Maximum vocal fundamental frequency
     MDVP:Flo(Hz) - Minimum vocal fundamental frequency
     
     MDVP:Jitter(%),
     MDVP:Jitter(Abs),
     MDVP:RAP,           Several measures of variation in fundamental frequency
     MDVP:PPQ,
     Jitter:DDP 
     
     MDVP:Shimmer,
     MDVP:Shimmer(dB),
     Shimmer:APQ3,       Several measures of variation in amplitude
     Shimmer:APQ5,
     MDVP:APQ,
     Shimmer:DDA  
     
     NHR,
     HNR      Two measures of ratio of noise to tonal components in the voice
     
     status - Health status of the subject , (one) - Parkinson’s, (zero) - healthy
     
     RPDE,
     D2       Two nonlinear dynamical complexity measures
     
     DFA      Signal fractal scaling exponent
     
     spread1,
     spread2,   Three nonlinear measures of fundamental frequency variation
     PPE      

In order to achieve the best possible detection accuracy of the disease, 5 different classification algorithms are compared in the
first stage. Then, because the goal is to achieve the best possible accuracy, I use some Ensemble techniques such as boosting and 
bagging.Ensemble learning helps improve machine learning results by combining several models.Ensemble methods are meta-algorithms
that combine several machine learning techniques into one predictive model in order to decrease variance (bagging), bias (boosting),
or improve predictions (stacking).

-----------

## Data Pre Processing
- Describing and Visualising Descriptive Statistics

   Histogram plot visualisation for each attribute will be diffcult because we have high dimensional column 23. I use heat map to find
   the correlations coefficient values and then remove the less correlation coefficient columns. After that i remove the irrelavant 
   features because this will minimize the accuracy of the algorithms.
 
   
- Data cleaning

- Feature split

   Splitting the dataset into input and output attributes.
   Drop irrelavant column values from dataset so that I can get better accuracy.

- Splitting the dataset into training and test set.

-----------

## Algorithms
- Compare 5 different algorithms and visualize boxplot, with and without applaying feature scale.
  
- Regularisation tuning for top 2 classification algorithms.
  
- Boosting and bagging classification algorithms with and without feature scale.
  
- Regularisation tuning for top 2 boosting and bagging classification algorithms.
  
- Compare all tunned algorithms and select the best algorithm.
  
- Fit and predict the best algorithm.
  

## Accuracy of best algorithm
The best algorithm got training accuracy of 100% and the test set accuracy 84%.The model is not underfit or overfit.
