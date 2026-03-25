# Retail Customer Revenue Prediction | EDA, OLS Regression, sklearn Modeling

## Objective

The objective of this project is to analyze customer-level retail behavior and build an interpretable regression model capable of predicting annual customer revenue. The project focuses not only on predictive performance but also on identifying the business variables that truly drive revenue generation across different customer segments.

## Problem Statement

Retail businesses often collect rich customer-level transactional data, but converting that data into actionable revenue insights requires understanding how demographic, behavioral, financial, and category-level variables interact. The goal of this project is to determine which customer characteristics most strongly influence annual revenue and to build a statistically validated linear regression model that explains these relationships in a business context.

## Dataset Note

This project uses a synthetic retail customer dataset designed to simulate realistic business conditions. Synthetic data was intentionally chosen to allow full control over customer attributes, hidden patterns, multicollinearity scenarios, skewness, category interactions, and revenue behavior commonly seen in real-world retail environments.

The dataset includes:

* Demographic variables
* Financial indicators
* Transaction behavior
* Product category preferences
* Geographic segmentation
* Revenue outcomes

## Exploratory Data Analysis (EDA)

### Key Business Insights

The analysis reveals that annual revenue is driven by the interaction of multiple customer dimensions rather than any single variable alone.

### Geographic and Gender Revenue Patterns

Women consistently generate stronger revenue in Tier 2 and Tier 3 cities, while men contribute relatively more in Tier 1 metropolitan regions. This suggests that revenue strategy should vary by geography rather than applying uniform customer targeting across markets.

A high-value niche segment also appears within the "Other" gender category in Tier 1 cities, where premium spending behavior is significantly higher than expected.

### Product Category Revenue Structure

Electronics emerges as the strongest total revenue driver, particularly in Tier 1 cities, making it the dominant commercial category.

However:

* Fashion produces higher average transaction values in Tier 1 markets
* Luxury reaches the highest mean transaction value in Tier 2 cities
* Grocery remains the most stable category across all regions

This shows that high total revenue and high transaction value do not always come from the same category.

### Behavioral Revenue Drivers

Spending score consistently outperforms basic demographic variables in explaining annual revenue.

Within similar income levels:

* Customers with higher spending scores generate significantly higher revenue
* Basket size contributes more than purchase frequency
* Transaction quality matters more than transaction count

### Discount Sensitivity

Electronics remains dominant even under high discount usage, indicating strong price responsiveness in that category and suggesting that discount-led campaigns are especially effective there.

### Financial Behavior

Revenue concentration is strongest among mid-range credit score customers, indicating that extremely high creditworthiness does not necessarily imply higher spending.

## Feature Engineering and Statistical Preparation

The modeling pipeline included:

* Missing value treatment
* Outlier inspection
* Log transformation for skewed variables
* Feature refinement
* Scaling using StandardScaler
* Multicollinearity reduction
* Train-test split before modeling

## Regression Modeling

Two modeling approaches were used:

### 1. OLS Regression

Used for statistical interpretation and coefficient significance analysis.

Performed:

* significance testing
* coefficient interpretation
* residual diagnostics
* heteroscedasticity testing
* multicollinearity checks

### 2. sklearn Linear Regression

Used for predictive modeling and test-set evaluation.

Performed:

* train/test prediction
* residual extraction
* model evaluation using R², MAE, RMSE

## Diagnostics Performed

The final model was validated using:

* VIF (Variance Inflation Factor)
* Residual analysis
* Q-Q plot inspection
* Breusch-Pagan test
* Influence analysis preparation

## Most Important Features Influencing Revenue

Strongest predictors:

* income
* spending_score
* average_transaction_value
* preferred_category
* city_tier
* discount_usage
* credit_score

Moderate contextual effect:

* gender (when interacting with category and geography)

Lower standalone influence:

* number_of_transactions
* raw gender distribution

## Final Business Conclusion

Revenue growth is not primarily driven by demographic counts but by customer behavior, spending intensity, and category-region interaction.

The strongest business opportunities lie in:

* Electronics volume retention
* Premium category expansion in Tier 2 cities
* Female-led growth in developing urban markets
* High-value customer targeting using spending behavior

## Tools Used

* Python
* pandas
* matplotlib
* scikit-learn
* statsmodels

## Author

Shorya Bisht
LinkedIn: https://www.linkedin.com/in/shorya-bisht-a20144349/
