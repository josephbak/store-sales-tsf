
# Store Sales - Time Series Forecasting

This README provides an overview of the Kaggle competition **[Store Sales - Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/overview)**, detailing its objectives, dataset structure, evaluation criteria, and guidelines for participation.

## Overview

In this competition, participants are tasked with predicting daily sales for various products at multiple stores using historical sales data. The challenge is to develop a robust forecasting model that captures trends, seasonality, and other relevant patterns in the data.

### Objective

To predict the sales (`sales`) for each store-product combination on specific future dates, using the provided historical data.

---

## Dataset Description

The dataset includes the following files:

### Files

- **`train.csv`**: Historical sales data for training your model.
- **`test.csv`**: Data for which sales predictions are to be made.
- **`stores.csv`**: Metadata about the stores.
- **`oil.csv`**: Daily oil prices, which may impact sales.
- **`holidays_events.csv`**: Holidays and events that might influence sales.
- **`transactions.csv`**: Weekly transaction counts at each store.
- **`sample_submission.csv`**: Format for the required submission.

### Columns in `train.csv` and `test.csv`

- **`id`**: Unique identifier for each prediction.
- **`date`**: Date of the observation.
- **`store_nbr`**: Store identifier.
- **`family`**: Product family category.
- **`sales`** (in `train.csv`): Target variable (sales figures).
- **`onpromotion`**: Number of items on promotion.

### Additional Files

1. **`stores.csv`**
   - `store_nbr`: Store identifier.
   - `city`: City where the store is located.
   - `state`: State of the store.
   - `type`: Store type.
   - `cluster`: Store cluster group.

2. **`oil.csv`**
   - `date`: Date of the observation.
   - `dcoilwtico`: Daily oil price.

3. **`holidays_events.csv`**
   - Information about holidays and events.

4. **`transactions.csv`**
   - `store_nbr`: Store identifier.
   - `date`: Date of observation.
   - `transactions`: Number of transactions at the store.

---

## Evaluation

Submissions are evaluated using the **Root Mean Squared Logarithmic Error (RMSLE)**. The formula for RMSLE is:

\[
RMSLE = \sqrt{\frac{1}{n} \sum_{i=1}^n \left(\log(y_i + 1) - \log(\hat{y}_i + 1)\right)^2}
\]

Where:
- \( y_i \): True sales.
- \( \hat{y}_i \): Predicted sales.
- \( n \): Number of predictions.

---

## Guidelines for Submission

1. **Format**: Submissions must match the format in `sample_submission.csv`.
   - Include `id` and the predicted `sales` columns.
2. **Rows**: Ensure all rows in `test.csv` are included.
3. **Evaluation Metric**: Aim to minimize RMSLE for better rankings.

---

## Getting Started

1. **Explore the Data**:
   - Investigate historical trends in sales.
   - Analyze correlations with oil prices, promotions, holidays, etc.

2. **Model Development**:
   - Consider time-series forecasting techniques (ARIMA, Prophet, etc.).
   - Explore machine learning approaches (XGBoost, LightGBM, etc.).
   - Use external datasets to enrich your model (if applicable).

3. **Feature Engineering**:
   - Create features to capture seasonality, trends, and store/product attributes.

---

## Resources

- **Competition Page**: [Kaggle Store Sales Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/overview)
- **Kaggle Forum**: Collaborate and discuss strategies with other participants.
- **Kernels**: Check out community-submitted notebooks for inspiration.

---

## Rules

- Follow [Kaggle’s competition rules](https://www.kaggle.com/rules).
- Ensure fair play and proper attribution of external datasets or solutions.

---

Happy Forecasting! 🌟