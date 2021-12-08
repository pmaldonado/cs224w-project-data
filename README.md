# cs224w-project-data
Data and preprocessing code for the Autumn 2021 CS 224W project.

To run the preprocessing notebook, download the data files from [Food.com Recipes and Interactions](https://www.kaggle.com/shuyangli94/food-com-recipes-and-user-interactions?select=RAW_recipes.csv) and extract into the `raw/` directory.

To ensure the quality of the dataset, we filter use the 5-core setting, i.e., retaining users and recipes with at least five highly-rated interactions (those with a rating above 3).

We sample training, validation, and test data with proportions of 0.7, 0.1, and 0.2, respectively. Summaries of the training, validation, and test interaction sets are included below:

Train:

Int64Index: 287360 entries, 381178 to 240853
Data columns (total 7 columns):
 #   Column     Non-Null Count   Dtype  
---  ------     --------------   -----  
 0   index      287360 non-null  int64  
 1   user_id    287360 non-null  int64  
 2   recipe_id  287360 non-null  int64  
 3   date       287360 non-null  object 
 4   rating     287360 non-null  float64
 5   u          287360 non-null  int64  
 6   i          287360 non-null  int64  
dtypes: float64(1), int64(5), object(1)

Validation:

Int64Index: 41052 entries, 365552 to 179980
Data columns (total 7 columns):
 #   Column     Non-Null Count  Dtype  
---  ------     --------------  -----  
 0   index      41052 non-null  int64  
 1   user_id    41052 non-null  int64  
 2   recipe_id  41052 non-null  int64  
 3   date       41052 non-null  object 
 4   rating     41052 non-null  float64
 5   u          41052 non-null  int64  
 6   i          41052 non-null  int64  
dtypes: float64(1), int64(5), object(1)

Test: 

Int64Index: 82103 entries, 335732 to 305711
Data columns (total 7 columns):
 #   Column     Non-Null Count  Dtype  
---  ------     --------------  -----  
 0   index      82103 non-null  int64  
 1   user_id    82103 non-null  int64  
 2   recipe_id  82103 non-null  int64  
 3   date       82103 non-null  object 
 4   rating     82103 non-null  float64
 5   u          82103 non-null  int64  
 6   i          82103 non-null  int64  
dtypes: float64(1), int64(5), object(1)

We also include a mapping from recipe_id to recipe name for downstream use.
