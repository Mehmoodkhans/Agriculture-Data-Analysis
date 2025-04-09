# Agricultural Crop Yield Prediction Report

**Author**: Mehmood Ahmed

## Introduction

In this analysis, I explore the factors influencing agricultural crop yields, focusing on key variables such as annual rainfall, temperature fluctuations, and pesticide usage. By leveraging machine learning techniques, I aim to predict future crop yields based on these critical environmental and agricultural factors.

The dataset utilized in this study is sourced from reputable organizations such as the Food and Agriculture Organization (FAO) and the World Data Bank, ensuring the accuracy and relevance of the data. Yield measurements are provided in hectograms per hectare, offering a precise metric for assessing crop productivity.

Through this analysis, I strive to uncover insights that can support agricultural planning and help forecast future trends in crop production.

---

## 🔍 Model Evaluation Metrics

| Model         | RMSE       | MSE            | R² Score |
|---------------|------------|----------------|----------|
| LightGBM      | 6362.36    | 40479669.76    | 0.9950   |
| Random Forest | 3914.36    | 15322231.10    | 0.9981   |
| CatBoost      | 7645.58    | 58454874.06    | 0.9927   |
| XGBoost       | 4294.43    | 18442140.75    | 0.9977   |

---

## 📊 Feature Importance (Top Contributors)

| Feature                            | CatBoost | LightGBM | XGBoost | Random Forest |
|------------------------------------|----------|----------|---------|----------------|
| Item Code                          | 67.55    | 23.43    | 26.47   | 75.15          |
| Area Code                          | 6.42     | 35.50    | 35.49   | 7.12           |
| Year Code                          | 3.41     | 19.43    | 29.24   | 3.09           |
| pesticides_tonnes                  | 5.91     | 12.53    | 6.23    | 3.69           |
| average_rain_fall_mm_per_year_x   | 10.22    | 5.03     | 0.00    | 5.54           |
| avg_temp                           | 6.48     | 4.07     | 2.57    | 5.41           |
| Domain Code                        | 0.00     | 0.00     | 0.00    | 0.00           |
| Element Code                       | 0.00     | 0.00     | 0.00    | 0.00           |

---

## 🔁 Cross-Validation Results

### RMSE Scores

| Model         | RMSE Scores                                             | Mean RMSE ± Std       |
|---------------|---------------------------------------------------------|------------------------|
| Random Forest | [4276.60, 4034.32, 4145.38, 4266.31, 4862.22]           | 4316.97 ± 286.65       |
| XGBoost       | [7332.96, 7204.79, 7175.45, 6953.14, 7861.03]           | 7305.47 ± 303.50       |
| LightGBM      | [10415.55, 9750.35, 9793.07, 9822.98, 9941.60]          | 10044.71 ± 314.38      |
| CatBoost      | [8115.18, 8255.75, 7804.41, 8210.77, 8309.57]           | 8148.93 ± 189.21       |

### R² Scores

| Model         | R² Scores                                               | Mean R² ± Std          |
|---------------|---------------------------------------------------------|------------------------|
| Random Forest | [0.9978, 0.9980, 0.9979, 0.9977, 0.9971]                | 0.9977 ± 0.0003        |
| XGBoost       | [0.9934, 0.9935, 0.9936, 0.9939, 0.9924]                | 0.9933 ± 0.0005        |
| LightGBM      | [0.9867, 0.9881, 0.9880, 0.9878, 0.9866]                | 0.9874 ± 0.0007        |
| CatBoost      | [0.9919, 0.9914, 0.9924, 0.9915, 0.9914]                | 0.9917 ± 0.0004        |

---

## ✅ Conclusion

Among the models tested, **Random Forest** performed the best overall, achieving the lowest RMSE and highest R² both on test and cross-validation sets. This suggests it is the most reliable for predicting crop yields in this context.

The analysis highlights the dominant influence of **Item Code**, **Area Code**, and **Year Code** on yield prediction, with moderate contributions from **pesticide usage**, **rainfall**, and **temperature**.

This comprehensive approach, combining multiple data sources and robust evaluation, provides a strong foundation for future agricultural planning and machine learning research in crop yield forecasting.