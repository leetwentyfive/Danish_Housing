# Danish Housing
Examining the factors associated with residential sale prices and developing a machine learning model to estimate property values.

### Summary
An analysis of Danish home sales from 1992 through 2023 to determine the key factors driving residential sales prices in an effort to use a machine learning model to predict sales prices. The project used a dataset found on Kaggle.com and was composed of ≈1.5 million historic residential sales. Sales records from 2024 only held the first three quarters of the year, so those were set aside as a holdout test set.

It was observed that location overwhelmingly influenced purchase prices more than other variables. Modeling was performed with XGBoost after Random Forest Regression proved to be computationally inefficient for this dataset. XGBoost produced an initial R² score of 0.468, before parameters were tuned and housing size was limited to 350 m². The final model retained 99.59% of regular residential sales and ultimately improved the R² score to 0.7036 on the unseen 2024 holdout dataset. 

Model estimates were compared with actual 2024 residential sales. The predictive model generates a narrower range of estimates than actual sales, producing a cluster of predictions that remain close to price-per-square-meter trend lines. As a result, the model was mostly unable to predict lower prices per square meter, with differing thresholds across house types. Overall, it was observed that the model overestimates purchase prices at lower levels and underestimates them at higher levels. This pattern likely exists because the dataset lacks qualitative variables, meaning the model cannot account for the condition of properties.

### Research Questions
- Which property characteristics are most associated with Danish residential sale prices?
- Using machine learning models, can these characteristics be used to predict home prices?

### Key Findings
* Postal codes affected price estimates more than any other variable
* The highest average prices per square meter were in and around the Danish capital, Copenhagen
* Villas had the highest sales count, while Apartments were the most expensive per m²
* Q2 was marginally busier than other times of the year, but prices across quarters maintained similar price trends

### Tools & Technologies
* Python
* Tableau
* XGBoost
* scikit-learn
