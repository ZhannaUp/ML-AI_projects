# [Integration of Large Language Models and Time Series Analysis in Demand Forecasting for E-Commerce](https://github.com/ZhannaUp/ML-AI_projects/blob/main/LLM%26%20Time%20Series%20in%20Demand%20Forecasting/LLM_%26_Time_Series_for_forecasting_.ipynb)
________
## Project Status - Completed.

## Problem Description


The company wants to optimize inventory planning for a seasonal product (e.g., winter boots) by accurately forecasting customer demand in Moscow. Traditional time series models alone are insufficient to capture the complex factors influencing demand, such as competitor behavior, weather, customer feedback, and seasonal fluctuations.

## Problem Goal

To build an advanced, hybrid forecasting model that accurately predicts future sales of a seasonal product by combining time series models, external data (e.g. reviews, weather, competitors), and language modeling (LLM-based topic modeling from customer reviews).

## Problem Statement


Design a demand forecasting pipeline that integrates:\
	•	historical sales data\
	•	weather conditions\
	•	competitor activity\
	•	customer sentiment and review topics (using LLM) and temporal patterns (holidays, seasons, trends).\
The aim is to produce accurate short-term and long-term sales forecasts and assist in better supply chain and inventory decisions.

## Data Description

The dataset includes the following CSV files:\
	•	`sales.csv`: Daily product sales, price, discount (36 datasets)\
	•	`competitors.csv`: Competitor sales, prices, and ratings\
	•	`reviews.csv`: Customer comments and ratings\
	•	`weather.csv`: Temperature, precipitation, weather conditions\
	All data is filtered for the city and spans multiple months or seasons.
    Input datasets: 36 monthly datasets (2022 to 2024)+ one dataset with comments of one ProductID.

## Tools Used
### Python Libraries:
- pandas
- numpy
- matplotlib 
- seaborn
- sklearn
- holidays

### Forecasting Models:
• Prophet for trend extraction\
• XGBoost for final supervised learning
### Natural Language Processing:
•	SentenceTransformers for BERT-based embeddings\
•	BERTopic for extracting dominant customer concerns
### Time Series Features: 
Lag, rolling average, calendar-based variables

## Work Plan:
1.	Load and clean all data (sales, reviews, weather, competitor metrics).
2.	Create calendar-based features (month, season, holiday).
3.	Use LLM (BERT) to embed and classify customer reviews into topics using BERTopic.
4.	Aggregate external signals (weather, competitors, reviews) by date.
5.	Merge all data into a unified dataset by date.
6.	Apply feature engineering (lags, rolling means, Prophet-generated trend/seasonality).
7.	Train XGBoost on engineered features and evaluate on test set.
8.	Visualize and interpret forecast vs actual demand.

## Research Findings
•	Incorporating external variables significantly improved forecasting performance.\
•	BERT + BERTopic effectively extracted meaningful product-related issues and customer sentiment from review text.\
•	Prophet helped isolate the long-term trend, which boosted the final model’s performance.\
•	XGBoost achieved a low RMSE on test data, indicating good generalization.\
•	The combination of temporal, textual, and behavioral features provides a robust foundation for forecasting.

## Recommendations and Future Work
  •	Use TimeSeriesSplit or rolling cross-validation to improve generalizability across seasons.\
	•	Fine-tune LLM and BERTopic for domain-specific topic modeling (e.g., footwear-related themes).\
	  Expand model to include:\
	•	Store-level predictions (if applicable)\
	•	More granular weather data (e.g., snow vs rain vs clear)\
	•	Integrate CatBoost or LightGBM for better handling of categorical/temporal features.\
	•	Deploy the model into a live forecasting pipeline with monthly retraining.

**Our model accurately predicts the demand for seasonal goods and has demonstrated an RMSE of 4.04!**
<p class="aligncenter">
  <img src="https://ibb.co/vCVMFc2N"><img src="https://i.ibb.co/DPzjJ13B/result.png" width="1000">
</p>
________

## Acknowledgements
Special thanks to [Sanjana Sanjeev Deshpande](https://github.com/sanjana3014), my teammate, for the preprocessing efforts and project collaboration.

________
## License
MIT License — Free to use, share and modify with attribution.

