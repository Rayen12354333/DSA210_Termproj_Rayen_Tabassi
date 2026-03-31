# 🍽️ Recipe Popularity on MealMate

**DSA 210 – Introduction to Data Science | Term Project**
**Rayen Tabassi | 33581 | Spring 2026**

---

## 📌 Overview

This project investigates **what makes a recipe popular** among users of MealMate, a recipe-sharing and food discovery app. Using over 180,000 recipes and 700,000 interaction records from the Food.com platform, the goal is to analyze and predict user engagement — specifically whether a user will like or save a recipe — based on attributes like cuisine type, preparation time, calorie content, and ingredient count.

The analysis works with a filtered subset of ~500 recipes and 5,000–8,000 interactions across ~150 users for a focused, manageable scope.

---

## 📊 Dataset

The data comes from the [Food.com Recipes and Interactions](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions) dataset on Kaggle.

**Recipe fields:**

| Feature | Description |
|---|---|
| `name` | Recipe title |
| `minutes` | Total preparation time |
| `ingredients` | List of ingredients used |
| `nutrition` | Calories, fat, sugar, protein, etc. |
| `n_steps` | Number of preparation steps |
| `tags` | User-assigned recipe tags |

**Interaction fields:**

| Feature | Description |
|---|---|
| `user_id` | Unique user identifier |
| `recipe_id` | Associated recipe |
| `rating` | 1–5 star score |
| `review` | Written feedback text |

### Derived Features

To connect the dataset to the MealMate context, several features are engineered:

- **Ingredient Count** — parsed from the raw ingredients list
- **Simplicity Score** — computed from prep time and ingredient count
- **Liked (binary)** — 1 if rating ≥ 4, 0 otherwise
- **Saved Flag** — simulated from rating + review length as a proxy for strong engagement
- **Cuisine Label** — assigned using the [Kaggle Recipe Ingredients Dataset](https://www.kaggle.com/datasets/kaggle/recipe-ingredients-dataset) as a secondary source

---

## 🔬 Methodology

1. **Exploratory Data Analysis** — distributions of ratings, prep time, calories; engagement patterns across cuisines and complexity levels
2. **Hypothesis Testing** — statistical tests on factors like simplicity, calorie content, and cuisine vs. likelihood of being liked/saved
3. **Predictive Modeling** — classification model to predict the `liked` indicator from recipe attributes, evaluated with accuracy and AUC-ROC

---
## 🚀 How to Reproduce

1. Clone this repository
2. Create a free [Kaggle](https://www.kaggle.com) account if you don't have one
3. Download the dataset from [here](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions)
4. Extract and place `RAW_recipes.csv` and `RAW_interactions.csv` into the `/data` folder
5. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
6. Run the notebooks in order inside `/notebooks`

> The `/data` folder is excluded via `.gitignore` — the dataset is not uploaded to this repo.

---

## 📅 Timeline

| Milestone | Date | Status |
|---|---|---|
| Repository created | March 17  |
| Proposal submitted | March 31 |
| EDA & hypothesis testing | April 14  |
| ML methods | May 5 |
| Final report | May 18  |

---

## 📎 Links

- **Primary Dataset:** [Food.com Recipes and Interactions – Kaggle](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions)
- **Secondary Source:** [Recipe Ingredients Dataset – Kaggle](https://www.kaggle.com/datasets/kaggle/recipe-ingredients-dataset)
