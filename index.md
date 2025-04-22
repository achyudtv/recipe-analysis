---
layout: default
---
## Recipes and Data

# Introduction
This dataset is based off recipes and their ratings/reviews posted on food.com since 2008. There are two datasets, recipes and ratings, which we are combining to get one big dataset which contains 234,429 reviews (rows in our dataset) of over 80,000 recipes. This vast dataset gives us a great way to predict a recipe's ratings (which is the average rating column we created) based on numerous columns in our combined dataset like 'minutes' (amount of time to prepare a recipe), 'nutrition' (nutrition information of a recipe in the form of an array including its calories, total fat, sugar, sodium, protein, saturated fat, and carbohydrates), 'n_steps' (number of steps of a recipe) and 'n_ingredients' (the number of an ingredients needed for a recipe). This well help us understand which qualities are more or less useful in getting good rated recipes, meaning if someone wants good reviews to the recipe online, they know what factors would most influence their recipe's ratings. 

---

## Data Overview

### Data Cleaning
---
Firstly, since we are originally two datasets, we did a left merge on between the datasets recipes and ratings. In our merged dataset, we replaced all ratings that contained a 0 with 'np.nan' as the number 0 may indicate a person gave a review without giving an official rating, messing up a recipe's average rating as a result. We than created a new column called 'average_rating' to give a recipes average rating, which is helpful to our analysis as that is what we are investigating. We then dropped duplicate recipes with the same id, as we got our average rating per recipe, which is enough. 

Furthermore, we have to split the column 'nutrition' into 7 different columns containing the values for a recipe's calories, total fat, sugar, sodium, protein, saturated fat, and carbohydrates. This was easy as we just pieced apart an array and created a new column for each nutrition value. 

We then removed the columns 'id', 'contributor_id', 'nutrition', 'steps', 'tags', 'ingredients', 'submitted', 'description', 'user_id', 'recipe_id', 'date', 'rating', and 'review' as these columns aren't neccessary for our analysis. We also drop any 'nan' values at this point as well.

We then get dataframe cleaned for our analysis. Here is a look at the head below:
| index | name | minutes | n_steps | n_ingredients | average_rating | calories | total fat | sugar | sodium | protein | saturated fat | carbohydrates | 
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| Header | Title |
| Paragraph | Text |


### Univariate Analysis
---

### Bivariate Analysis
---

### Interesting Aggregates
---

### Imputation
---

---

# Problem Identification

---

# Baseline Model

---

# Final Model

---

### GitHub & Sources
