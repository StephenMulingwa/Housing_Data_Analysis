# Housing_Data_Analysis
![image](https://github.com/user-attachments/assets/359ae2e1-ad47-4f87-a2c5-0aefa6203074)

## Overview
The Boston Housing dataset provides valuable insights into the real estate market, particularly in predicting housing prices based on various socio-economic and environmental factors. The dataset includes information such as the crime rate, property tax, number of rooms, and distance to key services, all of which contribute to the valuation of homes in the Boston area. Predictive models built using this dataset can help forecast future housing prices and identify trends that may influence the real estate market. This analysis is useful for stakeholders who need accurate data to make informed decisions regarding home purchases, investments, or regulatory policies, allowing them to better understand the factors driving housing prices in Boston.

### Business Problem
The Boston housing market is influenced by a wide range of factors, making it challenging to predict accurate property values. These factors include socio-economic variables such as crime rates, proximity to key services, environmental quality, and infrastructure development. Accurately forecasting housing prices is crucial for stakeholders like investors, homebuyers, real estate developers, and policymakers, as it directly impacts their decision-making processes. The complexity of the relationships between these variables presents a challenge, requiring the development of a reliable predictive model to inform real estate strategies and market interventions. The study aims to:

1. Develop a predictive model to accurately estimate housing prices in the Boston area, using various machine learning and statistical techniques.
2. Identify the most significant factors that influence housing prices, helping stakeholders understand the driving forces behind property valuation.
3. Provide actionable insights to support decision-making for investors, homebuyers, policymakers, and real estate developers, aiding in investment strategies and policy formulation.
4. Analyze patterns and trends in the Boston housing market over time, offering a comprehensive understanding of how changing factors impact housing prices in different neighborhoods.

Data
The dataset contains 506 observations and was sourced from [Kaggle](https://www.kaggle.com/datasets/altavish/boston-housing-dataset/data). It includes 14 variables that capture various socio-economic and environmental factors influencing housing prices in Boston. Key features include the crime rate, number of rooms, property tax, and proximity to highways, among others. This rich set of variables provides a foundation for building predictive models to estimate housing prices and identify the most important factors driving property values.

## Methods
### Data Cleaning
All rows with missing data were dropped thus remaining with 394 rows and 14 columns.

### Data Visualizations
The Housing Data is analysed by use of visualizations. Sample visualizations include:

i. Scatter Plot of Housing Prices and Number of rooms

![image](https://github.com/user-attachments/assets/d25b19c6-9650-4b81-b211-5e1843ef9abc)

The scatter plot shows a positive relationship between the number of rooms and the median value of houses, indicating that homes with more rooms tend to have higher prices. While the trend is generally upward, there is some variability, suggesting that other factors also influence housing prices aside from the number of rooms.

ii. Scatter Plot on the distance to 5 employment centers and the Nitric Polution

![image](https://github.com/user-attachments/assets/c2a22ca9-a393-4861-8b6e-98d53e9cb52a)

The scatter plot shows a clear inverse relationship between the distance to employment centers and nitric pollution levels. As the distance from employment centers increases, nitric pollution tends to decrease, indicating that areas closer to employment centers experience higher pollution levels. This pattern suggests that industrial or high-traffic zones near employment hubs contribute significantly to local pollution levels, while more distant areas are less affected.


iii. Box Plot

![image](https://github.com/user-attachments/assets/edeb8483-0123-40d2-bf94-41abc522c2ee)

The boxplot for the TAX variable shows the distribution of property tax rates in the Boston housing dataset. The median tax rate appears to be around 300, with the interquartile range (IQR) extending from approximately 300 to 600, indicating moderate variability in tax rates. There are no apparent outliers, as the whiskers reach the minimum and maximum values without any points beyond them, suggesting that the tax rates are fairly evenly distributed across the dataset.

## Models
### Linear Regression
MSE: 0.0314

R²: 0.8115

### Decision Tree

![image](https://github.com/user-attachments/assets/24010d40-ab0d-4903-b6ab-fc87779cfad2)

MSE: 8.9286

R²: 0.8481

### Random Forest

![image](https://github.com/user-attachments/assets/bb3871d4-3bee-4053-91d8-3bc25226bbf4)

MSE: 12.9733

R²: 0.8440

### Support Vector Machines
MSE: 7.1518

R²: 0.9299

The performance metrics across different models—Linear Regression, Decision Trees, Random Forest, and Support Vector Machines (SVM)—show varying degrees of accuracy in predicting housing prices. The **mean squared error (MSE)**, which measures the average squared difference between actual and predicted values, is lowest for the Linear Regression model (0.0314), indicating that it produces the most precise predictions in this context. However, when examining the **R-squared (R²)** score, which reflects the proportion of variance explained by the model, the Decision Trees model achieves a higher R² score (0.848) than Linear Regression (0.811). This suggests that while Decision Trees may have a higher error rate, they explain a greater amount of the variance in housing prices.

Support Vector Machines (SVM) stand out as the best-performing model with an R² score of **0.93**, indicating that it explains over 93% of the variance in the housing prices, with relatively low MSE (7.15). This makes SVM the most accurate model overall for this dataset, despite the somewhat higher MSE compared to the Linear Regression model. In contrast, the Random Forest model, while generally robust for handling complex data, has a higher MSE (12.97) and a slightly lower R² (0.84) than the Decision Trees and SVM. Based on these metrics, SVM offers the most reliable predictions, followed closely by Decision Trees, while Random Forest and Linear Regression trail behind in this particular case.

## Conclusion
In this analysis of the Boston Housing dataset, various machine learning models were employed to predict housing prices based on socio-economic and environmental factors. The results revealed that Support Vector Machines (SVM) provided the most accurate predictions, with the highest R² score (0.93), explaining over 93% of the variance in housing prices. The Decision Trees model also performed well, with an R² score of 0.848, suggesting its suitability for this task. On the other hand, while Linear Regression had the lowest mean squared error (MSE), its R² score of 0.811 indicated it explained less variance in the data compared to the other models. Random Forest, despite being a commonly used model, had relatively higher error rates and a slightly lower R² compared to the Decision Trees and SVM models. Overall, SVM proved to be the most reliable model for predicting housing prices, making it a strong candidate for future applications in real estate forecasting and decision-making.

### Recommendations
1. Use Support Vector Machines (SVM) for Future Predictions: Given its high accuracy and ability to explain a significant portion of variance in housing prices, SVM should be the preferred model for predictive analysis in the Boston housing market.
2. Explore Feature Engineering and Hyperparameter Tuning: Additional techniques such as feature engineering and tuning model hyperparameters could further enhance the performance of Decision Trees and Random Forest models, potentially reducing error rates and increasing predictive power.
3. Incorporate More Data: To further improve the models, more recent or additional housing data could be incorporated, capturing new variables or trends in the housing market that may impact predictions.
4. Implement for Real Estate Stakeholders: The predictive models developed, especially SVM, can be employed by real estate investors, developers, and policymakers to make informed decisions on property investments, pricing strategies, and urban planning. These models provide actionable insights into the factors influencing housing prices and can support data-driven decision-making in the housing market.