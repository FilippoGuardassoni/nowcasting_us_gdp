![](https://github.com/FilippoGuardassoni/nowcasting_us_gdp/blob/main/img/headerheader.jpg)

# Nowcasting US GDP Growth With Automated Machine Learning - Master Thesis

![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/pragyy/datascience-readme-template?include_prereleases)
![GitHub last commit](https://img.shields.io/github/last-commit/FilippoGuardassoni/nowcasting_us_gdp)
![GitHub pull requests](https://img.shields.io/github/issues-pr/FilippoGuardassoni/nowcasting_us_gdp)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![contributors](https://img.shields.io/github/contributors/FilippoGuardassoni/nowcasting_us_gdp) 
![codesize](https://img.shields.io/github/languages/code-size/FilippoGuardassoni/nowcasting_us_gdp)

# Project Overview

This research paper presents a comprehensive evaluation of Automated Machine Learning (AutoML) techniques in the domain of economic nowcasting. AutoML, which automates the
machine learning pipeline, is examined for its potential to outperform traditional statistical models min predicting economic indicators, specifically Gross Domestic Product (GDP) growth. The study compares various AutoML frameworks, including H2O, Auto-Sklearn, AutoGluon, TPOT, and AutoKeras, against established statistical models like Dynamic Factor Models (DFM) and ARIMA. The comparison encompasses different evaluation periods, capturing both periods of economic stability and turbulence, such as the COVID-19 recession. Key findings reveal that AutoML models consistently outperform traditional statistical models, particularly Extra Trees and XGBoost, showcasing their potential for enhancing the accuracy of economic nowcasting. Feature importance analysis highlights the distinct patterns in variable contributions among these models, shedding light on their interpretability. The research also emphasizes the importance of systematically selecting features and fine-tuning hyperparameters to improve AutoML model performance further. The Diebold-Mariano test is employed to determine the statistical significance of these improvements, providing valuable insights into the models' forecasting capabilities. In conclusion, this study underscores the promising role of AutoML in advancing the field of economic nowcasting. The results suggest that well-tailored AutoML models can offer superior predictive performance, challenging the dominance of traditional statistical models. These findings contribute to the ongoing discourse on the adoption of cutting-edge machine learning techniques in economic forecasting.


# Installation and Setup
See Google Colab Notebook

## Codes and Resources Used
- Python 2.7 - 3.0
- Google Colab

## Python Packages Used
See Google Colab Notebook

# Data
It comprises 134 monthly time series, categorized into eight distinct groups, encompassing a wide range of indicators and features, all of which are publicly available
and consistently updated on a monthly basis. These 134 time-series encompass various macroeconomic aspects, and can be grouped in the following categories:

1. Output and Income;
2. Labor Market;
3. Housing;
4. Consumption, Orders and Inventories;
5. Money and Credit;
6. Interest and Exchange Rates;
7. Prices;
8. Stock Market Data.
   
Thereby it offers an extensive array of variables for analysis and research purposes. The complete list of the data and the series-related data transformations are described in detail in Appendix as well as the recent modifications. Monthly indicator data are available from 1960:M1 to 2023:M6, so we have 760 observations for the potential regressors at
the moment in which this research is conducted.

## Source Data & Data Acquisition
Michael W. McCracken, a. S. (n.d.). FRED-MD: A Monthly Database for Macroeconomic Research. Retrieved from Federal Reserve Bank of St. Louis: https://doi.org/10.20955/wp.2015.012

## Data Pre-processing
As the datasets are imported raw, even though the series could be used right out-of-thebox, for this application, some preprocessing is needed. Preprocessing is a crucial step in
machine learning that involves transforming raw data into a format suitable for training machine learning models. It is essential because raw data often contains noise, missing
values, irrelevant information, and inconsistencies that can negatively impact the performance and accuracy of machine learning algorithms. Furthermore, as the work involves time series, transformations are also crucial. In fact, previous empirical studies found that on average better predictive performance can be expected when data is
stationary and seasonally adjusted (Nemeth and Hadházi, 2023). In particular, the steps followed are presented below.


# Project structure

```bash
├── dataset
│   ├── FRED Dataset
│   │   ├── fred-database_code
│   │   ├── fred-md
│   │   ├── FRED-MD Appendix
│   │   ├── Historcial FRED-MD Vintages Final
│   ├── Final
│   ├── Predictions
│   ├── Results
│   ├── Source
├── code
│   ├── automl.py
├── report
│   ├── nowcasting_us_gdp.pdf
├── img
│   ├── headerheader.jpg      
├── LICENSE
└── README.md
```

# Results and evaluation
With the exception of the PyCaret framework, the other packages showed relatively similar performance. On average, they achieved an RMSE of approximately 0.2181. Notably, two packages, AutoKeras and TPOT, performed better overall. Among them, AutoKeras stood out as the top performer, surpassing the average RMSE score with an average value of 0.0631. It's interesting to observe that in the simulated nowcasting scenario, where more information becomes available from month to month, one might expect that the models' accuracy would progressively improve. However, the reality is more nuanced. While it is theoretically plausible that the Root Mean Squared Error (RMSE) should decrease over time as more data becomes available, this isn't always the case. In fact, in most of the models, the RMSE is barely decreasing and in for the LSTM model is particularly noteworthy as it increases. See the report/nowcating_us_gdp.pdf for more details.


# Acknowledgments/References
See report/nowcating_us_gdp.pdf for references.

# License
For this github repository, the License used is [MIT License](https://opensource.org/license/mit/).
