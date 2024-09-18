# Critical Evaluation of Time Series Foundation Models in Demand Forecasting

## 🌐 Abstract
This research aims to benchmark and evaluate the performance of various foundation models in time series forecasting especially in the domain of demandforecasting. This study uses established methods of Statistical, Machine Learning,and Deep Learning models and compares their forecasting performance with some of the popular pretrained models for time series forecasting. This paper evaluates both accuracy and uncertainty metrics to establish a credible framework for comparison and benchmarking. Also, we will present a comprehensive comparison on the features and architectures of various foundational models that are currently available and highlight the limitations in the practical implementation of pre trained models for forecasting.This Study has shown that Machine Learning models are usually the best performing models across various error metrics and various time granularities followed by Deep Learning models. However, it was also noticed that pretrained models ocassionally perform better than all other established models. Study has used real life demand data set from a e-grocery innovator. 

## 📈 Data
The data used for the study is taken from [Rohlik Orders Forecasting Challenge](https://www.kaggle.com/competitions/rohlik-orders-forecasting-challenge). Rohlik is a leading European e-grocery innovator that is revolutionizing the food retail industry. The study has used the data from 4 warehouses Prague_1, Prague_2, Prague_3 and Brno_1. The dataset, originally recorded on a daily basis and it has been aggregated to both weekly and monthly level. Since this a very recent data set, none of the pretrained models would have been trained on this dataset, giving a fair and impartial way to judge capability of all models in comparision.

## 📄 Algorithms
The statistical forecasting has been carried out by using AutoARIMA, AutoETS and AutoTBATS from StatsForecast library. The study also uses Bagging methods like Random Forest and Boosting algorithms like XGBoost and Light GBM using the MLForecast library. Amongst the neural network architectures the study has chosen TFT and NHITS from NeuralForecast library [24]. The study has also used the Foundational Models TimeGPT [17] and TimesFM [19] for comparison with the other three broad classes of models

## 🛠️ Daily Data 
- The monthly forcasting data and notebook can be found [here](https://github.com/Satyajit-Chaudhuri/Critical_Evaluation-of_Foundational_Models_in_Demand_Forecasting/tree/main/Daily_Forecasting).
  
## 🛠️ Weekly Data
- The weekly forcasting data and notebook can be found [here](https://github.com/Satyajit-Chaudhuri/Critical_Evaluation-of_Foundational_Models_in_Demand_Forecasting/tree/main/Weekly_Forecasting).

## 🛠️ Monthly Data
- The monthly forcasting data and notebook can be found [here](https://github.com/Satyajit-Chaudhuri/Critical_Evaluation-of_Foundational_Models_in_Demand_Forecasting/tree/main/Monthly_Forecasting).

## 🛠️ Monthly Data with Finetuning
- The monthly forcasting data and notebook can be found [here](https://github.com/Satyajit-Chaudhuri/Critical_Evaluation-of_Foundational_Models_in_Demand_Forecasting/tree/main/Monthly_Forecasting_with_TimeGPT_Finetuned).

✅ **Results:** 

- On daily data -  LGB performs best closely followed by TimesFM Zeroshot. Also, TimesFM outperformed TimeGPT on all metrics.
- On weekly data - TFT performs best closely followed by TimeGPT Finetune. Also, TimeGPT outperformed TimesFM, machine learning and statistical models on all metrics. On Monthly data, when accuracy is measured over last 8 months data, LGB performs best closely followed by RF. Also, Foundational models perform better than statistical and deep learning models on all metrics.
- On Monthly data - when accuracy is measured over last 3 months data, again LGB performs best closely followed by XGB. Also, statistical and deep learning models are performing better than foundational models.
- Overall, machine learning based models almost were majorly the top performing models than all other forecasting methods across time granularities. But Foundational models for time series also provide good forecasts, at times even outperforming much established methods.

