# Pharma_Spending_Pattern

This project analyzes pharmaceutical drug spending across OECD countries, highlighting significant variations in expenditure. By examining key metrics like USD per capita and total health spending, we aim to uncover different facets of healthcare financing. Our analysis identifies the top 5 most promising markets for pharmaceutical companies.

## Team Members

<br>📈 Biswapriya Manna    - [@Bishudsi](https://github.com/Bishudsi)
<br>📈 Hiroyoshi Hiratsuka - [@pim61sit](https://github.com/pim61sit)
<br>📈 Melanie Ramnauth    - [@melram17](https://github.com/melram17) - [Link to Melanie's final video](https://www.loom.com/share/f0ff2eb9f2cd41eca72b48118695c63e?sid=b26916d7-1265-49dc-b57f-fe318f5f428a)
<br>📈 Oleksandr Lebediuk  - [@olebediuk](https://github.com/olebediuk)
<br>📈 Vidhi Patel         - [@Patelvidhim](https://github.com/Patelvidhim)
<br>📈 Zeinab Sadrosadat   - [@zsadr2002](https://github.com/zsadr2002)

📝Project Overview: 
This project intends to identify potential new markets for pharmaceutical companies. The data on pharmaceutical drug spending across the OECD member countries will be examined to generate evidence of high potential markets for major pharmaceutical companies and startups. Data Science approaches are employed to investigate the data from the OECD.

📦 Deliverables
This project provides the following deliverables:

- A comprehensive final report (presented within this README).
- A semi-dynamic web visualization (HTML or other forms) for interactive data exploration.[Click here to view our project site](https://bishudsi.github.io/Pharma_Spending_Pattern/)

📚Introduction and 🚨Problem Statement: 
The pharmaceutical industry is characterized by ever-increasing costs due to its industrial nature: i.e., High research and development costs, a need for high profits, monopoly tendencies, and an impact on patients. These sector-specific high-cost characteristics require continuous exploration of new drug markets. The need for effective and efficient strategies to identify a new drug market is a significant challenge for many pharmaceutical companies.

🏆Business Goal: 
This project intends to identify new markets for pharmaceutical companies by the data analysis and visualization. Through evidence-informed approaches, this project aims to identify potential new markets, using high pharmaceutical drug spending as a key indicator for decision-making. The intended objectives of this project are to identify potential new market countries in the form of:

- the top five (5) countries with the highest pharmaceutical drug spending and strong gross domestic product per capita (USD per capita)
- a group of countries with similar characteristics
- factors contributing to high pharmaceutical drug spending at the country level

Possible clients for this project include pharmaceutical stakeholders, both major companies and startups:
- Sales teams
- Executives

The project assumes these stakeholders are non-technical members of these companies and startups. 

📐Data Scope: The original OECD-derived dataset comprises 1,341 observations across 44 countries (primarily OECD members plus Brazil, Chile, Colombia and Costa Rica) from 1970 to 2022. All six core fields (LOCATION, TIME, PC_HEALTHXP, PC_GDP, USD_CAP, TOTAL_SPEND) are complete. Country‐level reporting is uneven for some nations (e.g. Chile, Brazil) span only a handful of years, so it was decided by the group to use 2011-2020 years for analysis as these years represent higher coverage by reporting countries. Per-capita spending (USD_CAP) is PPP-adjusted, smoothing exchange-rate volatility but potentially masking recent cost shocks, and TOTAL_SPEND (in millions USD) reflects only national aggregates, with no sub-national, disease-specific or outcome measures.

These limitations introduce several risks: biased growth estimates from short or gappy series and blind spots for major non-OECD markets.


🤖Data Science Approach: This project employs data science (DS) approaches. The data for this DS method come from pharmaceutical drug spending data by the Organisation for Economic Co-operation and Development (OECD). Three primary methods are proposed: Time-series analysis, clustering and trend-analysis/predictive modelling. 

The data for this DS method come from pharmaceutical drug spending data by the Organisation for Economic Co-operation and Development (OECD). 
The dataset can be accessed [here] (https://datahub.io/core/pharmaceutical-drug-spending#readme)

Additionally, population data from the World Bank was appended to the dataset to allow for further analysis in terms of population growth rates.
The population dataset can be accessed [here] (https://datahub.io/core/population)

Our methodology encompasses data acquisition, rigorous preparation, clustering analysis, and comprehensive data visualization.

1. Data Acquisition and Preparation

The foundation of our analysis is data sourced from the OECD, made accessible through DataHub.io. To ensure data quality and consistency, we followed a structured workflow:

Data Integration: Combining World Bank population data into the dataset sourced from OECD.

Data Cleaning and Filtering: Identifying and rectifying inconsistencies, missing values, and irrelevant entries to ensure accuracy.

Feature Manipulation: Transforming raw data into suitable features for analysis, such as calculating growth rates or per capita spending.

These steps were primarily executed using Python, leveraging the powerful data manipulation capabilities of pandas and numerical computing support from NumPy. 
Our development environment utilized Jupyter Notebooks for iterative development and analysis, with GitHub serving as the central repository for code and dataset management, including updating the project's README with data scope details.

2. Time-Series Analysis: Initial Market Scan

We performed time-series analysis to visualize pharmaceutical drug spending trends across OECD countries. This gave us a quick overview of current spending patterns and helped us:

- Identify Initial Top Spenders: Pinpoint countries with historically high or rapidly growing pharmaceutical expenditure.

- Guide Deeper Exploration: This initial scan served as a critical first step, informing where to focus our more in-depth analyses (e.g., clustering) to truly understand market potential beyond surface-level trends.


3. Clustering Analysis (Market Segmentation)

To identify groups of countries with similar pharmaceutical market characteristics, we applied K-Means clustering:

Data Aggregation: Initially, data was grouped by country, and key metrics like Total Spend and USD Per Capita

Feature Standardization: To ensure that all features contributed equally to the clustering process, they were standardized (scaled to a common range). This prevents features with larger numerical values from disproportionately influencing the clustering outcome. This was performed using StandardScaler from scikit-learn.

K-Means Clustering: We employed the K-Means algorithm from scikit-learn with k=3 clusters. The algorithm operates iteratively:

It begins by randomly selecting three initial "centroid" (center) points.

Each country is then assigned to the closest centroid based on its standardized features.

The centroids are recalculated as the mean of all countries assigned to that cluster.

Steps 2 and 3 are repeated until the cluster assignments no longer change significantly, indicating convergence.

This approach allows us to objectively segment countries into distinct market groups, providing a clear basis for targeted strategic planning.

By the end of the clustering process, we had three market clusters:

(1) Low Potential Markets - countries with declining health spending and USD per capita
(2) Stable Markets - countries with relatively stable health spending and USD per capita
(3) High Potential Markets - countries with high health spending and high USD per capita

3. Data Analysis and Visualization

For deriving insights and presenting our findings in an intuitive and accessible manner, we utilized a suite of Python libraries:

NumPy: Employed for efficient numerical computations and array operations throughout the analysis.

pandas: Crucial for all aspects of data manipulation, cleaning, and analysis, particularly for working with DataFrames and Series.

seaborn: Used to create visually appealing and informative statistical data visualizations, building upon Matplotlib's capabilities.

plotly.express: Leveraged for generating interactive plots, most notably for creating choropleth visualizations that effectively illustrate geographical spending patterns.

matplotlib.pyplot: Utilized for creating various static visualizations to support our analytical findings.


📝 Conclusion: This evidence-informed DS project is ideal for solving the existing challenges of identifying new drug markets for global pharmaceutical companies. The target audience of this project is executives and sales teams from major pharmaceutical companies and startups. The DS approaches for this project will uncover the top five (5) countries, clustering characteristics and possible factors contributing to drug spending at the country level. The data from the OECD will be examined to achieve the business goal and project objectives. The project team will spend the next five (5) days devising, analyzing and disseminating the evidence and deliverables for potential pharmaceutical clients. 

⚠️ Limitations and Future Work
It's important to acknowledge certain limitations of this analysis and consider recommendations for future work:

Data Timeliness: The data is only present up until 2022 with missing entries and reporting for different countries (likely due to COVID). As a result, our data and insights are based on pre-COVID economic and health spending trends.

Historical Data Gaps: Not all countries have extensive historical records (e.g., less than 10 years of lookback data). We made a decision on which countries to examine and what timeframe captured the most relevant data. In this case, a 10-year lookback was deemed strong and relevant to the present day.

OECD Scope: Our scope is limited to OECD member nations, as not all countries are members.

For future iterations, we recommend:

Updated Data Collection: Ensuring all countries are captured in future data collection will be crucial for analyzing post-COVID trends.

Expanded Analytical Scope: Due to time constraints, we focused primarily on clustering. Incorporating classification and regression models could provide deeper predictive insights and opportunity identification.
