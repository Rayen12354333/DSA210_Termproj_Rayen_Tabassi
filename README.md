# DSA210_Termproj_Rayen_Tabassi
# DSA210 Term Project – Rayen Tabassi (33581)

## Project Title
Recipe Popularity on MealMate

## Description
This project analyzes what makes a recipe popular using data from the Food.com platform, enriched with MealMate-specific features. The goal is to explore relationships between recipe attributes (cuisine, prep time, calories, ingredients) and user engagement, and to build a model that predicts whether a user will like a recipe.

## Dataset
This project uses the [Food.com Recipes and Interactions](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions) dataset from Kaggle.
### How to reproduce
1. Create a free Kaggle account at kaggle.com
2. Download the dataset from the link above
3. Extract and place `RAW_recipes.csv` and `RAW_interactions.csv` into a `/data` folder in the root of this repo
4. Install dependencies: `pip install -r requirements.txt`
5. Run the notebooks in order inside the `/notebooks` folder

The `/data` folder is excluded from this repo via `.gitignore`.

## Repository Structure
```
DSA210_Termproj_Rayen_Tabassi/
├── data/               # Not tracked – download instructions above
├── notebooks/          # Jupyter notebooks for analysis
├── requirements.txt    # Python dependencies
└── README.md
```

## Timeline
- ✅ March 17 – Repo created
- ✅ March 31 – Proposal submitted
- April 14 – EDA and hypothesis testing
- May 5 – ML methods
- May 18 – Final report
