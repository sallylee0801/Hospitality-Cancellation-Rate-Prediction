# University of Chicago - Data Engineering Platforms for Analytics (ADSP 31012) Final Project
Hospitality Cancellation Rate Prediction: Evaluation of key features towards hotel cancellation rates to optimize operation efficiency and maximize the overbook rate 
Team Members:
- [Sally Lee](https://github.com/sallylee0801)
- Reina Chen
- Kitae Kim

The README contains only a brief overview of our goals, investigation process, analysis, and recommendations.
For detailed documentation/analysis/findings, please refer to our [final presentation](https://github.com/sallylee0801/Hospitality-Cancellation-Rate-Prediction/blob/main/Hospitality%20Cancellation%20Rate%20Prediction.pdf) and report.
## Business Objective
We aim to leverage historical data, consider consumer behavior and external factors, and implement machine learning to increase cancellation rate prediction accuracy, optimize hotel resource allocation, and maximize revenue.
## Data Sources
We utilized hotel booking data from [ScienceDirect website](https://doi.org/10.1016/j.dib.2018.11.126), economic indicator data from [IMF] (https://data.imf.org/regular.aspx?key=61545849), weather data from [Visual Crossing](https://www.visualcrossing.com/), and tourist data from [Instituto Nacional de Estadística](https://www.ine.es/jaxiT3/Datos.htm?t=10822#!tabs-table).
## EDA
After analysis of data distributions and univariate trends, we identified three findings that guided our final investigations:

1. Groups and TA/TO have higher cancellation rates
2. No-Deposit & Refundable has a lower cancellation rate
3. The length of lead time is positively related to the cancellation rate
4. Domestic clients have a higher cancellation rate

## Data Modelling
We utilized Google Cloud Platform (GCP) to create a central accessible database for our team, and GitHub to share DML/DDL scripts throughout the modelling process. We used Excel and Jupyter Notebooks to wrangle the data from its base form, and MySQL workbench to change the database into our desired OLAP format. We then used Tableau to create visualizations and draw insights.

We transformed our initial OLTP model into a OLAP snowflake schema, to structure our data more effectively, making it easier for us to analyze our data in Tableau to create valuable insights. We created 4 fact tables for hotel booking, weather, economic indicator, and tourist data, and created dimensions to link different fact tables.
