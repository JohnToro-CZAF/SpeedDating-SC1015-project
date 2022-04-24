# Welcome to Speed-Dating-analysis repository

## About
This is a Mini-Project for SC1015(Introduction to Data Science and Artificial Intelligence) which focuses on speed-dating from [Speed Dating Experiment](https://www.kaggle.com/datasets/annavictoria/speed-dating-experiment). For detailed information, please view the source code in order from:


1. [Preliminary Exploratory Analysis](https://github.com/JohnToro-CZAF/SpeedDating-SC1015-project/blob/main/1-PreliminaryExploratoryAnalysis.ipynb)
2. [Attributes And satIncome](https://github.com/JohnToro-CZAF/SpeedDating-SC1015-project/blob/main/2-Attributes%26incomeSAT.ipynb)
3. [Similarities](https://github.com/JohnToro-CZAF/SpeedDating-SC1015-project/blob/main/3-Similarities.ipynb)
4. [Logistic Regression](https://github.com/JohnToro-CZAF/SpeedDating-SC1015-project/blob/main/4-LogisticRegression.ipynb)
5. [OtherModels(RandomForest, XGBoost, OLS)](https://github.com/JohnToro-CZAF/SpeedDating-SC1015-project/blob/main/5-OtherModels(RandomForest%2C%20XGBoost%2C%20OLS).ipynb)

## Contributors

1. Ng Zheng Kai - U2122921J - @nzkai 
2. Kelvin Pang - U2122086A - @JohnToro
3. Phan Nhat Hoang - U2120111G - @kelpjr

| Contribution List     	|                                 	        |
|-----------------------	|------------------------------------	    |             
| Ng Zheng Kai 	            | Presentation Slides, EDA, random forest   |
| Kelvin Pang            	| Presentation Slides, OLS                  |
| Phan Nhat Hoang           | Data spliting, Logistic Regression	    |

## Background
The choice of a marriage partner is one of the most serious 
decisions people face. In contemporary Western societies, this 
decision usually follows a long learning period during which 
people engage in more informal and often polygamous relation 
ships, i.e., dating. In particular, we analyze gender differences in dating preferences by analysing the speed-dating dataset. 

As in all matching markets, determining dating preferences from equilibrium 
outcomes is difficult because a given correlation of attributes across 
partners is often consistent with various preference structures such as:

Women put greater weight on the intelligence and the race of partner, while 
men respond more to physical attractiveness. Moreover, men do not value women's 
intelligence or ambition when it exceeds their own. 

To overcome this problem, we use speed dating dataset, the dataset came from a survey which was conducted in carefully controlled dating environment by researchers. What we found in this dataset might consistent with known social structure theory or something we have not known yet. 
     
## Dataset
This dataset recored speed-dating dates which each one is a date between subject and his/her partner. Everything about the date was recorded including partner's and subject's dating preference(score on attributes they want in their partner), personal information: age, income, sat score. And the most important variable is `match`: indicating this date was successful or not. We will focus on this variable as a response.
## Problem Definition
- With so many different factors that can affect the result of a match which ones have the most impact?
- How can we identify which variable as the most important to a match
- Identify which variables appeared in dataset affect a male's or female's match separately. From there identify the difference in dating preference between male and female

## Solving problem
- By doing preliminary exploratory analysis, we observed that there are many variables that are irrelevant to the response. Also the dataset is prevalent with missing values. So we decided just take a look to into specific categories of variables: attributes, satIncome and similarity. 
- Cleaning data and do EDA on each of category of variables, by limiting our scope of exploring this dataset, we were able to control the sophisticated missing values in each category. Creating a better analysis for each category.
- Aggregate existing variables to create variables that portrayed dating preference while the original can not.
- Based on generalized linear probability model, the coefficient of appropriate predictive or regression model can be used as the magnitude of variable's importance. By using different models and normalizing technique, we were able to extract stastically significant dating preference of both male and female.

## Problem Categories that we splitted into
- 1st Category ( 6 Key Attributes )
   - Attractive, Sincerity, Intelligence, Fun, Ambition and Shared Interest
- 2nd Category ( Intelligence & Income )
   - Sat Score & Income
- 3rd Category ( Similarities )
   - Shared Interest, Race, Field Of Study, Region

## Models Used

1. Logistic Regression
2. Random Forest
3. XGBoost
4. Ordinary Least Squares(OLS)

## Conclusion
- The ideal traits that Males look for in Females are:
   - Fun
   - Attractive
   - Intelligence
   - Similar interest
- The ideal traits that Females look for in Males are:
   - Humurous
   - Inteligence
   - Similar field of study
- Finally, we look at the importance of similarity. 
   - Women strongly discriminate on the basis of race. They are more than 8% more 
    likely to accept a partner of their own race. Given the underlying 
    match rate is only around 38%, this is a large effect. 
   - Men, on the other hand, do not exhibit a significant racial preference. Whether this 
    difference stems from gender-specific dating goals or reflects a 
    more fundamental gender difference is difficult to ascertain from 
    our data. 
   - Being in the same field of study has no predictive 
    power, but both men and women prefer partners from the same 
    region of the world. 


## What did we learn from this project?
- Handling imbalance dataset using regEx, categorizing the similar data
- Logistic Regression from sklearn
- XGBoost & OLS
- API Usage
- Other packages such as pandasql
- Collaborating using GitHub
- Normalizing data

## Future work
- Exploring racial dating preference
- Based on significant features, creating a high accuracy predicting a match. Benchmarking on different methods of sampling data

## References
- https://pandas.pydata.org/pandas-docs/version/0.23/generated/pandas.DataFrame.plot.html
- https://seaborn.pydata.org/tutorial/color_palettes.html
- https://www.statsmodels.org/dev/generated/statsmodels.regression.linear_model.OLS.html
- https://nominatim.org/release-docs/latest/api/Overview/
- https://geopy.readthedocs.io/en/stable/
- https://scikit-learn.org/stable/auto_examples/ensemble/plot_forest_importances.html
- https://towardsdatascience.com/understanding-feature-importance-and-how-to-implement-it-in-python-ff0287b20285
- https://christophm.github.io/interpretable-ml-book/feature-importance.html
- https://academic.oup.com/qje/article-abstract/121/2/673/1884033?redirectedFrom=PDF
- https://machinelearningmastery.com/calculate-feature-importance-with-python/
