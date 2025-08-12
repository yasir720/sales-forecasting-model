# Sales Forecasting Model

This project demonstrates building a sales forecasting model using historical sales data enriched with external features. The notebook leverages **Upgini** feature enrichment and **CatBoost** regression to improve predictions of future sales.

---

## Overview

Sales forecasting is a critical task for businesses to manage inventory, optimize operations, and plan marketing strategies. This notebook walks through a practical approach to forecasting sales using time-series data from a retail dataset.

---

## Dataset

- The data contains daily sales records for multiple items across stores.
- The dataset is sourced from the [Upgini sample dataset](https://github.com/upgini/upgini) and includes sales, store, item, and date features.
- A subset of 19,000 rows is used for faster prototyping.

---

## Methodology

### Data Preparation

- Convert relevant columns to appropriate types.
- Split the dataset into training and testing sets based on time, training on data before 2017 and testing on data from 2017 onward.

### Feature Enrichment

- Use **Upgini FeaturesEnricher** to augment the dataset with additional temporal features based on the date column.
- This enrichment helps the model better understand seasonal and calendar effects impacting sales.

### Model Training

- Train a CatBoost regression model on both original and enriched features.
- Evaluate performance using SMAPE (Symmetric Mean Absolute Percentage Error).

---

## Key Results

- The enriched model outperforms the base model, demonstrating the value of external feature enrichment.
- Visualization of actual vs predicted sales shows a tighter correlation for the enriched model.
- Some outliers remain, indicating opportunities for further improvements.

---

## Insights & Next Steps

- Feature enrichment significantly improves forecast accuracy by capturing complex time-based patterns.
- Future work could include hyperparameter tuning, incorporating additional external data, and exploring advanced time-series models or ensembling.
- API usage limits for enrichment should be considered when scaling.

---

## How to Use This Notebook

1. Clone this repository.
2. Install required packages: `upgini`, `catboost`, `matplotlib`, `seaborn`.
3. Open and run the notebook in Google Colab or Jupyter.
4. Follow the steps to train and evaluate the model.
5. Experiment by tuning parameters or adding new features.

---

## Contact

For questions or feedback, feel free to reach out!

---

*Happy forecasting! 🚀*
