# Daily Expenses Analysis 

## Project Overview
This project involves a comprehensive analysis of personal spending data for January 2026. By applying data cleaning techniques and exploratory data analysis (EDA), the project identifies spending patterns, calculates categorical impacts, and investigates financial outliers using Python.

## Dataset Description
The dataset, `dailyexpenses.csv`, contains transaction records with the following attributes:
* **Item**: Description of the expense.
* **Date**: Transaction date.
* **Amount**: Cost in RM.
* **Category**: Expense classification (Food, Transport, Education, etc.).

## Project Structure

### 1. Data Cleaning & Pre-processing 
To ensure data integrity, the following steps were taken:
* **Missing Value Detection**: Used `df.isnull().sum()` to identify gaps in the dataset.
* **Targeted Imputation**: Handled missing values in the `Amount` column by calculating the **median specifically for the Education category**, ensuring that typical spending levels were maintained without introducing bias from other categories.
* **Data Refinement**: Missing item descriptions were filled with "Unknown" to maintain record counts.

### 2. Summary Statistics 
* **Descriptive Analysis**: Generated a statistical summary using `.describe()` to understand the mean, median, and spread of spending.
* **Categorical Frequency**: Analyzed which habits occur most often (Food).
* **Total Cost Impact**: Compared the frequency of transactions against the total monetary sum per category.

### 3. Data Visualisation 
The analysis is supported by three key visual perspectives:
* **Line Plot**: Visualising daily spending trends to identify peak days.
* **Bar Chart**: Comparing total expenditure across different categories.
* **Box Plot**: Identifying price distribution and outliers within categories like Education and Entertainment.

## Key Insights & Conclusion 
* **The Frequency vs. Cost Paradox**: While the **Netflix Subscription (RM 55.00)** was the highest single transaction, the **Food** category had the most significant impact on the overall budget, accounting for the highest frequency (22 times) and the highest total cost (RM 238.50).
* **Volatility in Education**: The Education category showed high inconsistency (std of 14.89 vs mean of 14.76), proving that academic spending is driven by irregular, high-cost events rather than a steady daily cost.
* **Budgeting Action Plan**: Future budgeting efforts should focus on managing the frequency of small food expenses, as they accumulate more significantly than isolated large purchases.

## Technologies Used
* **Python 3.12**
* **Pandas**: Data manipulation.
* **Matplotlib & Seaborn**: Data visualisation.

---

### How to Run
1. Clone this repository.
2. Ensure you have the `dailyexpenses.csv` file in the same directory as the notebook.
3. Install dependencies: `pip install pandas matplotlib seaborn`.
4. Run `Daily_Expenses_Analysis.ipynb` to view the full report.
