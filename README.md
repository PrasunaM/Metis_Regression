# Predicting Recipe Ratings

Goal of this project was to use linear regression to predict recipe ratings by scraping vegetarian recipe data from [allrecipes.com](https://www.allrecipes.com/). Data scraping was performed using selenium and beautiful soup and imported into a pandas dataframe. Data was cleaned and exploratory analysis was conducted on jupyter notebooks. Finally, cleaned data was modeled using linear regression and polynomial regression. 


## Data

1000 recipes were scraped with 11 features related to a recipe such as title, rating, prep time, cook time, recipe category, yield, servings, calories, protein, carbohydrates, fat, and sodium. Most of the features were continuous numerical variables. Categorical variables were discarded for modeling. Rows with nulls for recipe rating were discarded and nulls in nutrient info were replaced with average values from the respective subcategories.

# Workflow
1. [Web Scraping](https://github.com/PrasunaM/Predict_Recipe_Rating-MetisRegression/blob/0ee936eb397f92b00064e8600fc22a39f6ca942c/AllRecipes_Scraping%20Part1.ipynb)
2. [EDA & Baseline Regression](https://github.com/PrasunaM/Predict_Recipe_Rating-MetisRegression/blob/0ee936eb397f92b00064e8600fc22a39f6ca942c/AllRecipes_EDA%20&%20Baseline%20Regression.ipynb)
3. [LR with log transformation and Polynomial Regression](https://github.com/PrasunaM/Predict_Recipe_Rating-MetisRegression/blob/0ee936eb397f92b00064e8600fc22a39f6ca942c/AllRecipes_EDA%20&%20Baseline%20Regression.ipynb)
4. [Presentation Slides](https://github.com/PrasunaM/Predict_Recipe_Rating-MetisRegression/blob/0ee936eb397f92b00064e8600fc22a39f6ca942c/Regression_presentation.pdf)


## Conclusion

Logistic regression and polynomial regression with Lasso regularization modelling techniques were opted for modeling. Unfortunately, the target variable had no linear relationship with any of the features and hence linear regression performed poorly. Polynomial regression performed well on training data only indicating that the model was overfit. Hence, Lasso regularization was performed to address the overfit but could not be eliminated. Kfold cross validation was conducted between the models and linear regression performed better than polynomial.

But it is important to note that none of the modelling techniques would be recommended to predict the ratings because of the low accuracy. However, future goals of the project include gathering more diverse data and features that can explain the nature of ratings on the recipes.

## Tools

* Selenium and Beautifulsoup for scraping
* Numpy and Pandas for data manipulation
* Scikit-learn for modeling
* Matplotlib and Seaborn for plotting



