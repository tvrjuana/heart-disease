# Heart Disease

This repository was created for tutorial purposes on exploratory data analysis, creating models, tuning models, and evaluating those models from the Heart Disease dataset. A local health clinic in Atlanta, GA wants a unique insights for classifying whether their patients have heart disease or not based on certain features.

Tutorial Blog: Tavera Analytics - Heart Disease

Juana Tavera

## Business Understanding & Problem
The business problem at hand is that Heart Healthy Clinic (stakeholder - local health clinic) is looking for a model that will classify whether a patient has heart disease minimizing error. This model will lend a hand to their overbooked and busy doctors - reducing their workload. Therefore Tavera Analytics' goal was to analyze, create models, and fine tune them to minimize false negatives.

False negative: Not diagnosing a patient with heart disease when in actuality the patient does have heart disease.

## Data Analysis - Inital Setup 
The dataset heart.csv was used for data analysis and modeling. 

heart.csv has 14 columns and 303 entries. This a fairly small dataframe (since it is usually used for academic purposes), realized that keeping all the columns was necessary to keep as much data as possible.

# Results 

## heart_disease_modeling

The first and largest section of this notebook is the Exploratory Data Analysis (EDA) since there are no null values and there are no columns that could be dropped. 

![graph1](./images/correaltion_heatmap.png)
A correlation heatmap to see which features have a higher correaltion (postive or negative) with the target variable output: 0 less chance of heart disease and 1 more chance of heart disease. 

From the heatmap can see that variables cp, thalachh, slp have the highest positive correlation and exng, oldpeak, caa, thall have the highest negative correlation.

### Highest Positive Correlation 

![graph2](./images/chest_pain.png)
With the patient that has typical angina there are less likely to have heart disease, however when they have atypical angina or non-anginal pain there are more likely to have heart disease.

![graph3](./images/thalachh.png)
Thalachh: maximum heart rate achieved, typical resting heart rate in adults is 60 - 100 beats per minute.

People who do not have heart disease have a larger range between the maximum heart rate achieved from 71 to 195 and most of the values were within 156 bpm. Their mean thalacch was at 139.1. However the people who do have heart disease the range was smaller but typically the thalachh was also higher from 96 to 202 and most of the values were within 172 bpm. The mean for people who did have heart disease was also higher at 158.47 bpm.

![graph4](./images/slope_thalachh.png)
Slope: the slope of the peak exercise ST segment (it corresponds to the area from the end of the QRS complex to the beginning of the T wave)

0 = unsloping
1 = flat
2 = downsloping

On average people who do not have a heart disease their thalachh is lower compared to those who do have heart disease across the slopes. The people whose slope was downsloping tend to have a higher thalachh in general no matter if they have a heart disease or not. The person who had the highest thalachh at 220 and has heart disease also had a downsloping ST segment.

### Highest Negative Correlation

![graph5](./images/exng.png)

It was negatively correlated; therefore, the people who did not have exng were more likely to be diagnosed with heart disease.

![graph5](./images/oldpeak_exng.png)
Oldpeak: ST depression induced by exercise relative to rest This relationship between oldpeak and exng:

- when exng is no there is a larger range in oldpeak
- people who do have heart diesease tend to have a lower range in oldpeak

![graph6](./images/caa.png)
Fluoroscopy: an imaging technique that uses X-rays to obtain real-time moving images of the interior of an object

From the correlation heatmap - saw that caa was negatively correlated therefore it makes sense that when caa is equal to 0 than the output has higher heart disease value.

![graph7](./images/thall.png)
Thalessemia: a genetic blood disorder that is characterized by a lower rate of hemoglobin than normal

- 0 = null
- 1 = fixed defect
- 2 = normal
- 3 = reversable defect

As the plot shows when thall was equal to 2 i.e normal, people were diagnosed with heart disease with three (reversable defect) coming in second. This makes sense since thalessemia is relatively rare in the world with it effecting only 1.8% of the global population. Here is a [link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2893117/) explaining the disorder in detail.

## Dummy Model 
The Dummy Model was just using the majority class of the target variable to predict the 