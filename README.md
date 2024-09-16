# Boticário Project

# Exploratory Analysis for Sales Forecasting

This repository contains the final exploratory analysis notebook for the sales forecasting project. The goal of this analysis is to understand sales variability and identify significant patterns that can guide marketing strategies and resource optimization.

## Analysis Summary

### 1. **Data Preparation**

- **Missing Data Treatment:** A large proportion of null values ​​were identified in the `VL_RECEITA_BRUTA` variable, which impacts modeling and sales forecasting.
- **Date Format:** The date column has an inadequate format (`YYYYWW`), making temporal analysis and sales forecasting difficult. Converting this date to a standard `datetime` format is essential for accurate analysis.

### 2. **Descriptive Analysis**

- **Distribution of Variables:**
- **`FLG_DATA`:** Binary indicator of commemorative date, with approximately 29% of observations associated with special dates.
- **`COD_CANAL`:** Two distinct sales channels, which allow comparison between online and physical sales.
- **`DES_CATEGORIA_MATERIAL`:** Six categories of materials, allowing analysis of performance by type of product.
- **`COD_REGIAO`:** Two sales regions, facilitating comparison of regional performance.
- **`COD_MATERIAL`:** 2252 distinct materials, representing the diversity of products.
- **`VL_PRECO`:** Two price values, indicating a simple price structure.

### 3. **Visualization and Analysis**

- **Correlation between Variables:**
- **`FLG_CAMPANHA_MKT_B`** has a significant correlation (0.91) with **`QT_VENDA_BRUTO`**.
- **`QT_VENDA_BRUTO`** has a strong correlation (0.91) with **`VL_REVENUE_NET`**.
- **`FLG_CAMPANHA_MKT_A`** and **`FLG_CAMPANHA_MKT_C`** have a significant correlation (0.69).
- **`FLG_CAMPANHA_MKT_A`** shows a perfect correlation (1.00) with **`VL_REVENUE_NET`**.

### 4. **Insights and Recommendations**

- **High Variability:** Some groups, such as **`COD_CHANNEL = 0`** and **`COD_REGIAO = 0`**, show high variability in gross revenue, which may indicate large transactions or high-value customers.

- **Average Revenue Difference:** The **`COD_CHANNEL = 0`** and **`COD_REGIAO = 0`** group has the highest average gross revenue, suggesting that these areas may be more profitable.

- **High Maximum Values:** Certain groups have high maximum values, indicating large transactions that impact total revenue.

- **High Standard Deviation:** High standard deviations indicate significant variations in gross revenue, reflecting different transaction patterns across channels and regions.

### 5. **Conclusion and Recommended Actions**

- **Investigate Large Transactions:** Analyzing high-value transactions can reveal opportunities to replicate or expand those revenues.
- **Adjust Strategies:** Tailor marketing and sales strategies based on average revenue differences across channels and regions.
- **Manage Variability:** Monitoring and understanding high variability can help optimize revenue management and improve forecasting.
-

# Sales Forecasting

### 1. **Objective**

The objective of this project is to predict future sales based on historical data and relevant variables. We use advanced machine learning techniques to provide accurate forecasts and assist in strategic decision making.

### 2. **Process**

The data was divided into training and testing sets. After normalizing the data with StandardScaler, we applied the Random Forest Regressor model. We tuned the model using Grid Search to find the best hyperparameters, ensuring the best possible performance.

### 3. **Results**
- **Mean Absolute Error (MAE):** 52.88
- **Root Mean Squared Error (RMSE):** 233.88
- **R² (Coefficient of Determination):** 0.91

### 4. **Results by best-selling SKU**
**177396**
- **Mean Absolute Error (MAE):** 896.74
- **Root Mean Squared Error (RMSE):** 1757.5
- **R² (Coefficient of Determination):** 0.955

**69198**
- **Mean Absolute Error (MAE):** 69198
- **Root Mean Squared Error (RMSE):** 1379.97
- **R² (Coefficient of Determination):** 0.961

**152982**
- **Mean Absolute Error (MAE):** 862.60
- **Root Mean Squared Error (RMSE):** 1897.5
- **R² (Coefficient of Determination):** 0.716
-
### Interpreting the Metrics

- **MAE (Mean Absolute Error):** Measures the average of the absolute errors between the predictions and the actual values. Smaller values ​​indicate more accurate predictions.
- **RMSE (Root Mean Squared Error):** Penalizes large errors more heavily than MAE. Smaller values ​​indicate better model performance.
- **R² (Coefficient of Determination):** Measures the proportion of data variability that is explained by the model. Values ​​closer to 1 indicate better model fit.
-
### 5. **Insights**
- **Model Accuracy:** The Random Forest Regressor model had an R² of 0.91, indicating
