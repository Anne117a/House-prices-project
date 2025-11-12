# House-prices-project
# King County House Price Analysis (Regression Project)

This project analyzes and models house prices from King County, WA. The project is in two parts:
1.  **A Data Analyst Dashboard** built in Tableau to find market insights.
2.  **A Data Scientist Model** built in Python to predict sale prices.

---

## Part 1: Dashboard

I acted as a Data Analyst for a real estate firm. My goal was to clean the data and build an interactive dashboard to identify key market drivers.

### Live Tableau Dashboard 
You can view and interact with the full, live dashboard here:

**[https://public.tableau.com/app/profile/annamaria.benakova/viz/HousePriceAnalysisofKingCounty/Dashboard1](https://public.tableau.com/app/profile/annamaria.benakova/viz/HousePriceAnalysisofKingCounty/Dashboard1)**

*(Optional: Add your dashboard screenshot here)*

### Key Insights from the Dashboard:
* **Location is Key:** The median house price in "Medina" (over $2.1M) is much higher than in other cities.
* **Condition Matters:** There is a clear positive correlation between a house's "condition" (rated 1-5) and its median sale price.
* **Outliers:** The market has significant outliers, with a few properties selling for over $10M, which can skew simple "average" calculations.

---

## Part 2: Predictive Model

The second goal was to build a machine learning model to predict a house's sale price based on its features.

* **Business Problem:** To create a tool that can accurately estimate a house's value.
* **Model Iteration:**
    1.  My first model, a **Linear Regression**, failed badly (**R² = -6.67**). I identified this was because the model could not handle the extreme price outliers (the mansions).
    2.  I iterated to a new model, a **RandomForestRegressor**, which is robust to outliers.
* **Final Result:** The new model performed significantly better, achieving an **R-squared (R²) of 0.619**. This means the model can successfully explain **61.9%** of the variation in house prices based on features like `sqft_living`, `city`, and `condition`.

---

## Technical Details

* **Tools Used:** Python (Pandas, Numpy, Scikit-learn), Tableau
* **Analysis:** You can see the full, commented Python code (including data cleaning, model iteration, and evaluation) in the `analysis.ipynb` notebook in this repository.
