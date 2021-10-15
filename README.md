# Project 2: Ames Housing Predictions

## Executive Summary
As part of the property valuation team at Ames Investment Company, we have been tasked by the Director of Real Estate Investment to come up with a machine learning model that can predict housing prices in Ames and identify properties with high investment potential. The machine learning model can reduce human bias in evaluating a property and predicting its selling price. Real estate investment involves large capital investment and a great deal of financial risk. It is essential that investment opportunities are assessed in an unbiased and scientific manner to increase the consistency of making successful investment decisions. Linear regression is a machine learning algorithm based on supervised learning. It can be optimized using Ridge regression and Lasso regression. The Ridge Regression model is a good model to use to predict the sale price of properties in Ames. It would perform better than the baseline model since it has a lower RMSE score. However, the model performance can be improved by refining the features in the dataset.

## 1. Problem Statement
As part of the property valuation team at Ames Investment Company, we have been tasked by the Director of Real Estate Investment to come up with a machine learning model that can predict housing prices in Ames and identify properties with high investment potential. The machine learning model can reduce human bias in evaluating a property and predicting its selling price. By comparing the listed sale price with our predicted sale price, we can identify properties that have higher predicted price to listed price ratio. These would be identified as properties with high investment potential and can be added to our company's real estate investment portfolio. With this model, we can advise our shareholders on which properties to invest in to maximize investment returns.

## 2. Introduction
Real estate investment involves large capital investment and a great deal of financial risk. Valuation is an inherent human activity and a judgemental process. [1] It is essential that investment opportunities are assessed in an unbiased and scientific manner to increase the consistency of making successful investment decisions. The development of machine learning models that use sophisticated algorithms to analyze data and predict patterns can be optimized to correct and refine their conclusions based on new and changing data.[2] 

Linear regression is a machine learning algorithm based on supervised learning. It can be optimized using Ridge regression and Lasso regression. These three models will be studied to build a model that can predict housing prices accurately and overcome the noise created by human bias. In addition, the model can be further refined by adding new housing data to improve performance in predicting housing prices and assessing the investment potential of a property.

## 3. Data Dictionary
Please refer to the link for the data documentation. http://jse.amstat.org/v19n3/decock/DataDocumentation.txt 

## 4. Summary of Analysis
The data from Ames Assessor's Office used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010 is used in developing the machine learning model. The data was cleaned by identifying, converting or filling up the null values found in the dataset. Most of the null values corresponded to 0 or 'None' values. 

After which, the ordinal variables were converted from strings to numeric format and the nominal variables were converted to numeric format using dummy coding. Next, the variables that showed a direct relationship with each other were removed from the dataset to reduce collinearity. The properties from the non-residential zones, A, C and I, were dropped from the dataset as the model is meant to focus on residential properties only. To reduce the interference by outliers, properties that had sale prices of more than 419,088 were dropped from the dataset.

The dataset was partitioned using a 70/30 train/test split. The dataset was fit to the three models, linear regression, ridge regression and lasso regression. A 5-fold Cross-validation was also used to evaluate each model performance. Of the three models, ridge regression showed the best performance score with the lowest difference in train/test scores. The R^2 train score from the cross validation method was 0.850 and the R^2 test score was 0.785. In comparison, Lasso regression showed a R^2 CV train score of 0.876 and R^2 test score of 0.808. When running the Ridge Regression model to predict sale prices, the R2 score for the test and predicted sale price was 0.785. This implies that 78.5% of the variability in y is explained by the x-variables in our model. 

The RMSE for the ridge model is 30,796 while the RMSE for the null model is 68,353. This shows that the ridge model performs better than the null model in predicting the sale price. 

## 5. Conclusions and Recommendations
The Ridge Regression model is a good model to use to predict the sale price of properties in Ames. It would perform better than the baseline model since it has a lower RMSE score. However, the model performance can be improved by refining the features in the dataset. More analysis can be done to examine the collinearity between the features. Those that show high collinearity can be refined by dropping the feature that has lower colinearity to the sale price. 

## 6. References
1. Amidu, Abdul-Rasheed. “Research in Valuation Decision Making Processes: Educational Insights and Perspectives.” Journal of Real Estate Practice and Education, vol. 14, no. 1, 2011, pp. 19–34. JSTOR, www.jstor.org/stable/24863123. Accessed 12 July 2021.

2. Steve Gaenzler, May 20, 2021, "Will AI solve the problem of appraisal bias?", https://www.housingwire.com/articles/appraisal-bias-ai-solution/. Accessed 12 July 2021
