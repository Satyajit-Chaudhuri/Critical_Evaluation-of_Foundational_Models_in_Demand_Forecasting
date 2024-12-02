# Critical Evaluation of Time Series Foundation Models in Demand Forecasting  

## 🌐 Abstract  
Accurate forecasts are crucial as they enable organizations to make informed decisions about their supply chain. This research aims to benchmark and evaluate the efficiency of various foundation models in time series forecasting, especially in the domain of demand forecasting. The research employs traditional statistical, machine learning, and deep learning algorithms and compares their forecasting performance with popular foundational models **TimeGPT** and **TimesFM**. Both accuracy and uncertainty metrics are considered to establish a credible framework for benchmarking.  

This study demonstrates that **TimesFM** emerged as the better-performing model across MASE and SMAPE and different time granularities. Foundational models were found to be at par with traditional models, presenting a strong case for wider research and adoption in industrial demand forecasting.  

📄 Read the Full Publication [here.](https://openreview.net/forum?id=TS42sRKINd)

## 📈 Data  
The data used for the study is sourced from two datasets:  
1. **Daily Time Granularity**: The dataset is from the [Rohlik Orders Forecasting Challenge](https://www.kaggle.com/competitions/rohlik-orders-forecasting-challenge). Data from four warehouses (**Prague_1**, **Prague_2**, **Prague_3**, and **Brno_1**) was utilized.  
2. **Weekly and Monthly Granularity**: Data with 5,800 unique combinations from the [**VN1 Forecasting Accuracy Challenge dataset**](https://www.datasource.ai/en/home/data-science-competitions-for-startups/vn1-forecasting-accuracy-challenge-phase-1/description) was aggregated to weekly and monthly levels.  

These datasets, being recent, ensure that no pretrained models were exposed to them, enabling an unbiased evaluation.  

## 📄 Algorithms  
### **Statistical Models**:  
- **AutoARIMA**, **AutoETS**, and **AutoTBATS** (StatsForecast library).  

### **Machine Learning Models**:  
- Bagging methods: **Random Forest (RF)**.  
- Boosting algorithms: **XGBoost** and **LightGBM (LGBM)** (via MLForecast library).  

### **Deep Learning Models**:  
- **Temporal Fusion Transformer (TFT)**.  
- **NHITS** (NeuralForecast library).  

### **Foundation Models**:  
- **TimeGPT** and **TimesFM** were compared with the above models.  

## 🛠️ Notebooks and Data  
- **Daily Forecasting**: [GitHub Link](https://anonymous.4open.science/r/Critical_Evaluation-of_Foundational_Models_in_Demand_Forecasting-BB71/)  
- **Weekly Forecasting**: [GitHub Link](https://anonymous.4open.science/r/Critical_Evaluation-of_Foundational_Models_in_Demand_Forecasting-BB71/)  
- **Monthly Forecasting**: [GitHub Link](https://anonymous.4open.science/r/Critical_Evaluation-of_Foundational_Models_in_Demand_Forecasting-BB71/)  

## ✅ Results  
### **Daily Data**  
- **TimesFM** outperformed traditional algorithms.  
- **LGBM** performed well, reinforcing the strength of machine learning models.  
- **TimeGPT**, in both zeroshot and finetuned forms, lagged behind.  

### **Weekly Data**  
- **TimesFM** demonstrated the best performance across metrics (SMAPE, MASE).  
- Deep learning models like TFT and NHITS were competitive.  
- **TimeGPT** showed strong performance compared to statistical methods.  

### **Monthly Data**  
- **TimesFM** excelled in accuracy metrics (MASE, SMAPE).  
- Limited fine-tuning was feasible with **TimeGPT** due to its data requirements.  

### **Overall Insights**  
- Foundational models provide competitive forecasts and simplify workflows, especially in new data distributions.  
- Machine learning models remain strong contenders across granularities.  

## 📊 Evaluation Metrics  
1. **Accuracy Metrics**:  
   - SMAPE (Scaled Mean Absolute Percentage Error).  
   - MASE (Mean Absolute Scaled Error).  

2. **Uncertainty Metrics**:  
   - CRPS (Continuous Ranked Probability Score).  

## 🔍 Key Areas for Further Research  
1. **More FMs**: Evaluate additional foundational models.  
2. **Cross-Domain Testing**: Apply models to datasets from diverse industries.  
3. **Ensembles**: Explore hybrid approaches combining FMs and traditional models.  
4. **Uncertainty Quantification**: Improve prediction interval calibration for FMs.  

## 🏁 Conclusion  
This research has used demand forecasting datasets from forecasting competitions to establish a
comparative study between the performances of Statistical, ML, DL and FMs across daily, weekly and
monthly time horizons. To evaluate the performances of the algorithms, MASE & SMAPE were used
as scaled errors are independent of the scale of the data. TimesFM emerged as the best performing
algorithm across all time granularities. These were closely followed by the DL & vanilla ML models.
TimeGPT has also outperformed the statistical and ML models across some time horizons. Overall, it
can be concluded that the foundational models, although being very new members of a forecasters’
toolkit, has shown impressive performance and can be used to establish a strong baseline for further
research. The FMs can adapt to new data distributions with minimal tuning and do not require manual
feature engineering and careful selection of lagged variables unlike ML regressors and thus allow the
users to build and deploy forecasting solutions quickly and easily
