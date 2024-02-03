# Hospitality Cancellation Rate Prediction🏨

In this project, we will be exploring hotel booking data of a city hotel and resort in Portugal, public data, and governmental data to identify hotel cancellation trends and their relationships with weather and economic conditions. We will be building a Random Forest model to assess the key features affecting hotel cancellation rates.

Team Members:
- [Sally Lee](https://github.com/sallylee0801)
- Reina Chen
- Kitae Kim

The README contains only a brief overview of our goals, investigation process, analysis, and recommendations.

For detailed documentation/analysis/findings, please refer to our [final presentation](https://github.com/sallylee0801/Hospitality-Cancellation-Rate-Prediction/blob/main/Hospitality%20Cancellation%20Rate%20Prediction.pdf).
## Business Objective
We aim to leverage historical data, consider consumer behavior and external factors, and implement machine learning to maximize the hotel's revenue through:
1. Maximizing the overbook rate by increasing the accuracy of cancellation rate prediction
2. Optimizing operational efficiency and marketing strategies through precision customer targeting
## Data Sources
We utilized hotel booking data from [ScienceDirect website](https://doi.org/10.1016/j.dib.2018.11.126), economic indicator data from [IMF](https://data.imf.org/regular.aspx?key=61545849), weather data from [Visual Crossing](https://www.visualcrossing.com/), and tourist data from [Instituto Nacional de Estadística](https://www.ine.es/jaxiT3/Datos.htm?t=10822#!tabs-table).
## Data Modelling
We utilized Google Cloud Platform (GCP) to create a central accessible database for our team, and GitHub to share DML/DDL scripts throughout the modelling process. We used Excel and Jupyter Notebooks to wrangle the data from its base form, and MySQL workbench to change the database into our desired OLAP format. We then used Tableau and built a Random Forest Model to create visualizations and draw insights.

We transformed our initial OLTP model into an OLAP snowflake schema, to structure our data more effectively, making it easier for us to analyze our data in Tableau to create valuable insights. We created 4 fact tables for hotel booking, weather, economic indicator, and tourist data, and created dimensions to link different fact tables.
## EDA
After analysis of data distributions and univariate trends, we identified some findings that guided our final investigations:

1. Relationship between weather and cancellation rate is insignificant
2. PPI is negatively related with cancellation rates, whereas unemployment rate has a positive relationship with cancellation rates
3. Domestic travellers have a higher cancellation rates
4. Non-refundable payment reservations have the highest cancellation rate at 99%
5. Group segment has the highest cancellation rate at 58%, for TA/TO is about 40%
6. The length of lead time is positively related to the cancellation rate 

We also built a Random Forest Model with 84% precision, AUC 92% score of ROC curve for both test and train data. Based on our machine learning model, we identified that deposit type, origin of country, lead time, and market segment are the significant features that impact cancellation rates. On the other hand, external factors have a weak impact on cancellation rates. Thus, we will focus on these features when deriving our business strategies.
<img width="815" alt="image" src="https://github.com/sallylee0801/Hospitality-Cancellation-Rate-Prediction/assets/121594845/d3f8298e-606a-44c1-b889-1d627b360e07">

## Insights: We have identified 4 key features that affect the hospitality cancellation rate:
1. **Groups and TA/TO have higher cancellation rates** as these agents buy bulk tickets upfront, and the hotel provides more flexible cancellation  policies in contract. The over-pre-order and low opportunity cost lead to a higher cancellation rate.
  <img width="462" alt="image" src="https://github.com/sallylee0801/Hospitality-Cancellation-Rate-Prediction/assets/121594845/f19130e6-3bf6-4ddf-b6d5-f7325c9a8603">

2. **No-Deposit & Refundable deposit type has a lower cancellation rate** as cheaper offers will normally have a no-refund policy. As the price is relatively low, the opportunity cost for clients to cancel is acceptable,  which leads to a higher cancellation rate.
  <img width="275" alt="image" src="https://github.com/sallylee0801/Hospitality-Cancellation-Rate-Prediction/assets/121594845/477a7e93-421a-4666-8a37-57747990a0e4">

3. **The length of lead time is positively related to the cancellation rate** as it is difficult to predict future travel.
  <img width="583" alt="image" src="https://github.com/sallylee0801/Hospitality-Cancellation-Rate-Prediction/assets/121594845/e224ebcb-ea42-485c-9352-7810a9e45ef7">

4. **Domestic clients have a higher cancellation rate** as they are more flexible with travel plans and the travel costs are relatively low compared to international clients.
  <img width="334" alt="image" src="https://github.com/sallylee0801/Hospitality-Cancellation-Rate-Prediction/assets/121594845/ed6d44cd-3543-4492-8dab-ea128226bc1c">

## Recommendations
Based on our insights, we have provided several recommendations to reach our intended goal of maximizing the overbook rate and optimizing marketing and operation strategies:
1. Change pricing strategy to mid-price with a deposit
2. Consider long lead time cancellations and near-to-date order demand and calculate the optimal cancellation due day to maximize occupancy
3. Secure higher placement through paid bids on Google Search and TA/TO search results for searches originating from websites outside Portugal
4. Cooperate with Corporate, Aviation, and Complimentary clients and review contracts signed with Group and TA/TO
