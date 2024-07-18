# 🦄 Unicorn Growth

**Authors**: Athena Wu, Ian Nguyen, Lana Huyen, Oty Baasandorj

---

[Project Overview](#project-overview) | [Background](#background) | [Data Sources](#data-sources) | [Data Processing](#data-processing) | [Analysis and Visualization](#analysis-and-visualization) | [Notebooks Description](#notebooks-description) | [Key Insights](#key-insights) | [Summary and Conclusions](#summary-and-conclusions) | [Installation Instructions](#installation-instructions) | [Usage Instructions](#usage-instructions) | [Appendix](#appendix)

---

## 🌟 Background

Unicorn companies, privately held startups with valuations above 1 billion USD, have significantly impacted global entrepreneurship by creating innovative solutions and driving economic growth. This project aims to analyze the growth rates of unicorn companies from 2022 to 2024, focusing on their industry, location, date joined, and investors. By understanding these factors, stakeholders can gain insights into the dynamics influencing unicorn companies and identify key trends that contribute to their success.

## 🚀 Project Overview

Using datasets of unicorn companies, we analyze the growth of these companies versus multiple variables. Our analysis involves examining the growth trends based on industry, geographic location, and date of attaining unicorn status. We also investigate the impact of investors on the growth rates of these companies. The ultimate goal is to provide an understanding of the factors that influence the growth and success of unicorn companies.

---

## 📊 Data Sources

The data for this analysis was sourced from multiple repositories, primarily Kaggle and CB Insights. The datasets include:

- **unicorn_startups_sept_2022.csv**: Contains unicorn company data as of September 2022.
- **unicorn_startups_may_2024.xlsx**: Contains unicorn company data as of May 2024.
- **unicorn_startups_july_2023.csv**: Contains unicorn company data as of July 2023.

These datasets include information on company valuations, industries, geographic locations, dates of attaining unicorn status, and investors.

---

## 🛠️ Data Processing

### Data Cleaning and Preparation

1. **Filtering Industries**: We retained only the rows where the "Industry" column matched a predefined list of relevant and emerging sectors such as Artificial Intelligence, E-commerce, Cybersecurity, etc.
2. **Handling Missing Values**: Rows with missing values in critical columns like “2022_Valuation,” “2023_Valuation,” or “2024_Valuation” were removed to ensure a complete and accurate dataset for analysis.
3. **Converting Valuation Data**: The valuation columns, initially in string format with dollar signs and commas, were converted to numeric values for accurate calculations.

### Growth Calculation

We calculated the percentage growth for three periods:
- **22 Growth**: The percentage change from 2022 to 2023 valuations.
- **23 Growth**: The percentage change from 2023 to 2024 valuations.
- **Total Growth**: The overall percentage change from 2022 to 2024 valuations.

### Merging Data

The first step involved merging data from different files to create a merged dataset. This was done in the `merged_df_setup.ipynb` notebook. The merged dataset was then used for further analysis and visualization.

---

## 📈 Analysis and Visualization

The analysis was conducted through a series of Jupyter Notebooks, each focusing on a specific aspect of the data. The visualizations provide insights into the growth trends and patterns of unicorn companies.

### Key Analysis:

- **Industry Analysis**: Examining the growth rates of different industries.
- **Country Analysis**: Analyzing growth trends across various countries.
- **Date of Entry Analysis**: Investigating the impact of the date of attaining unicorn status on growth.
- **Investor Analysis**: Identifying key investors and their frequency.

### Visualizations:

#### Industry Growth Analysis:

1. **Boxplots**: 
   - **Industry vs. 2022 Growth**: Visualizes the distribution of growth across different industries from 2022 to 2023.
   - **Industry vs. 2023 Growth**: Shows the growth trends from 2023 to 2024 across various industries.
   - **Industry vs. Total Growth**: Displays the total growth from 2022 to 2024 for different industries.
   - ![Total Growth Box Plot](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/industry_growth_total.png)

2. **Bar Graphs**:
   - **Average Growth per Industry**: Compares the average growth rates across different industries for 2022, 2023, and the total growth period.
   - **Industry Growth Trends**: Highlights key growth trends in leading industries such as Artificial Intelligence, E-commerce, and Cybersecurity.
   - **Total Growth Bar**: ![Total Growth Bar](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/average_growth_total.png)


#### Country Analysis:

1. **Line Graphs**:
   - **Total Valuations by Country**: Compares the total valuations of unicorn companies across different countries for 2022, 2023, and 2024.
   - **Country Growth Trends**: Points out growth trends in countries like the United States, China, India, and the UK.
   - **2022-2023-2024 Graph (No US, China)**: ![2022-2023-2024 Graph (No US, China)](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/2022-23-24graph_no_us_china.png)
   - **2022-2023-2024 Graph**: ![2022-2023-2024 Graph](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/2022-23-24graph.png)

2. **Bar Graphs**:
   - **Average Growth per Country**: Shows the average growth rates for unicorn companies in different countries.
   - **Country Growth Comparison**: A visual comparison of growth rates across top-performing countries.
   - **CAGR by Country**: ![CAGR by Country](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/cagr_by_country.png)

3. **Geographic Maps**:
   - **Unicorn Distribution**: Maps out the geographic distribution of unicorn companies, highlighting hubs of startups.
   - **Growth Hotspots**: Identifies regions with the highest growth rates and the most significant concentration of unicorn companies.

#### Date of Entry Analysis:

1. **Scatter Plots**:
   - **Date Joined vs. Growth**: Looks at the relationship between the date a company joined the unicorn club and its growth rate.
   - **Entry Trends**: Shows how the entry year impacts the growth trajectory of unicorn companies.

2. **Trend Lines**:
   - **Growth Over Time**: Visualizes how the growth of unicorn companies has evolved over different entry years.
   - **Impact of Entry Year**: Analyzes the effect of joining the unicorn club in specific years on overall growth rates.

#### Investor Analysis:

1. **Bar Graphs**:
   - **Top Investors**: Identifies the most frequent investors in unicorn companies and their investment areas.
   - **Investor Frequency**: ![Investor Frequency](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/investor_frequency.png)

2. **Network Diagrams**:
   - **Investor Connections**: Visualizes the network of top investors and their relationships with unicorn companies.
   - **Investment Patterns**: Highlights patterns in investments made by leading venture capital firms.

### Additional Visualizations:

- **Country vs Industry**: ![Country vs Industry](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/country_industry.png)
- **Greatest CAGR**: ![Greatest CAGR](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/df_greatest_cagr.png)
- **Greatest Number Declining**: ![Greatest Number Declining](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/df_greatest_number_declining.png)
- **Greatest Number Growing**: ![Greatest Number Growing](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/df_greatest_number_growing.png)
- **Greatest Number Startups**: ![Greatest Number Startups](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/df_greatest_number_startups.png)
- **Greatest Percent Declining**: ![Greatest Percent Declining](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/df_greatest_percent_declining.png)
- **Greatest Percent Growing**: ![Greatest Percent Growing](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/df_greatest_percent_growing.png)
- **Greatest Percent Startups**: ![Greatest Percent Startups](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/df_greatest_percent_startups.png)
- **Lowest CAGR**: ![Lowest CAGR](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/df_lowest_cagr.png)
- **Average Growth Rate by Year (Interval One)**: ![Average Growth Rate by Year (Interval One)](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/GrowthvsDateJoined/Average%20Growth%20Rate%20by%20Year%20(Interval%20One).png)
- **Average Growth Rate by Year (Interval Two)**: ![Average Growth Rate by Year (Interval Two)](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/GrowthvsDateJoined/Average%20Growth%20Rate%20by%20Year%20(Interval%20Two).png)
- **Average Growth Rate by Year (Overall)**: ![Average Growth Rate by Year (Overall)](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/GrowthvsDateJoined/Average%20Growth%20Rate%20by%20Year%20(Overall).png)
- **Number of Unicorn Companies Joining Per Year (2024)**: ![Number of Unicorn Companies Joining Per Year (2024)](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/GrowthvsDateJoined/Number%20of%20Unicorn%20Companies%20Joining%20Per%20Year%20(2024).png)
- **Number of Unicorn Companies Joining Per Year Overall**: ![Number of Unicorn Companies Joining Per Year Overall](https://github.com/lanahuyen/Group_Project_1/blob/main/output_data/GrowthvsDateJoined/Number%20of%20Unicorn%20Companies%20Joining%20Per%20Year%20Overall.png)

---

## 📚 Notebooks Description

### 1. Industry_vs_DateJoined.ipynb
Analyzes the relationship between the industry and the date the company joined the unicorn status. Key visualizations include boxplots and bar graphs that illustrate growth trends across different industries and years.

### 2. Growth_vs_DateJoined.ipynb
Examines growth trends relative to the date companies achieved unicorn status. This analysis helps understand whether earlier or later entry into the unicorn club affects growth rates.

### 3. Country_vs_DateJoined.ipynb
Looks at country-specific trends in relation to the date companies achieved unicorn status. This notebook provides insights into the geographic distribution of unicorn companies and how different regions have evolved over time.

### 4. Unicorn_oty_condensed.ipynb
Focuses on country-wise growth analysis, identifying which countries experienced the most significant growth in unicorn valuations over the specified period.

### 5. Unicorns_oty.ipynb
A continuation of the previous notebook that provides a more detailed breakdown of country-wise growth trends, highlighting key factors contributing to growth in different regions.

### 6. Final_Industry.ipynb
Analyzes industry-wise growth over the years, identifying which sectors have performed the best and worst. Special attention is given to sectors like Artificial Intelligence and E-commerce.

### 7. merged_df_setup.ipynb
This notebook handles the initial merging of data from various sources to create a comprehensive dataset. It ensures that all necessary information is included for further analysis.

### 8. geoapify_df_setup.ipynb
Sets up the Geoapify API for geographic analysis. This notebook is needed for visualizing the location-based trends of unicorn companies.

### 9. cagr_by_country.ipynb
Calculates the average Compounded Annual Growth Rate (CAGR) by country, providing insights into which regions have the highest growth trajectories.

### 10. map_visualizations.ipynb
Generates visualizations to show the distribution of unicorn companies. These visualizations include maps highlighting key innovation hubs and growth patterns.

---

## 🔍 Key Insights

### Industry Growth Analysis

- **2022 Growth**: Artificial Intelligence experienced the highest average growth rate, while the E-commerce & Direct-to-Consumer and Edtech industries saw significant declines.
- **2023 Growth**: Data Management & Analytics and Artificial Intelligence industries had notable growth, whereas the Internet and Supply Chain Logistics & Delivery industries experienced a decrease.
- **Total Growth**: Artificial Intelligence and Other industries demonstrated the most substantial average total growth.

### Country Analysis

- **Highest Growth**: China had the highest growth from 2022 to 2023, while the United States experienced the largest growth from 2023 to 2024.
- **Geographic Distribution**: The United States and China dominated with the largest number of unicorn companies. Other countries like India and the United Kingdom also show a sizeable presence.

### Date of Entry Analysis

- **Trends**: There is a significant increase in unicorn companies in 2021, likely due to COVID-19 and the developments pushed by it
- **Insights**: The year of joining the unicorn club can significantly impact growth rates, with certain years seeing higher growth trends due to a better economy.

### Investor Influence

- **Top Investors**: Accel is the most frequent investor, with investments in 62 unicorn companies. Other top investors include Sequoia Capital and Andreessen Horowitz.
- **Impact**: Prominent investors play important roles in the success and growth of unicorn companies, often providing the necessary capital and expertise to scale quickly.

---

## 📜 Summary and Conclusions

### Key Findings

1. **Artificial Intelligence and Other Industries**: These sectors consistently showed the highest average growth rates across all periods, indicating strong market performance and investor interest.
2. **Declining Industries**: Sectors like E-commerce & Direct-to-Consumer and Edtech experienced significant declines in valuation growth, suggesting challenges in these markets.
3. **Geographic Influence**: Companies from major tech hubs like the United States and China dominate the dataset, with cities such as San Francisco and Beijing being prominent.
4. **Investor Impact**: Leading venture capital firms like Sequoia Capital and Andreessen Horowitz were frequently involved in high-growth companies, highlighting their role in driving industry success.

### Conclusions

The analysis reveals that industry and the year of joining significantly influence valuation growth. Artificial Intelligence stands out as a leading growth sector, while certain industries face market challenges. Geographic location and investor backing also play important roles in determining company success. 

---

## 🛠️ Installation Instructions

To replicate this analysis, ensure you have the following libraries installed:
python
```import pandas as pd
from pathlib import Path
import hvplot.pandas
import requests
import json
from pprint import pprint
from api_keys import geoapify_key
import matplotlib.pyplot as plt
import seaborn as sns
from matplotlib.backends.backend_pdf import PdfPages

---

```
## 💻 Usage Instructions
Run the Jupyter notebooks in the following order for a complete analysis:

1. **merged_df_setup.ipynb**
This notebook merges data from various sources to create a comprehensive dataset. Ensure all necessary files are in the correct directory before running this notebook.

2. **geoapify_df_setup.ipynb**
Sets up the Geoapify API for geographic analysis. This step is crucial for visualizing the geographic distribution of unicorn companies.

3. **cagr_by_country.ipynb**
Calculates the average Compounded Annual Growth Rate (CAGR) by country. This notebook provides insights into which regions have the highest growth trajectories.

4. **Industry_vs_DateJoined.ipynb**
Analyzes the relationship between the industry and the date the company joined the unicorn status. This notebook includes key visualizations like boxplots and bar graphs to illustrate growth trends across different industries and years.

5. **Growth_vs_DateJoined.ipynb**
Examines growth trends relative to the date companies achieved unicorn status. This analysis helps understand whether earlier or later entry into the unicorn club affects growth rates.

6. **Country_vs_DateJoined.ipynb**
Looks at country-specific trends in relation to the date companies achieved unicorn status. This notebook provides insights into the geographic distribution of unicorn companies and how different regions have evolved over time.

7. **Unicorn_oty_condensed.ipynb**
Focuses on country-wise growth analysis, identifying which countries experienced the most significant growth in unicorn valuations over the specified period.

8. **Unicorns_oty.ipynb**
Similar to the previous notebook but provides a more detailed breakdown of country-wise growth trends, highlighting key factors contributing to growth in different regions.

9. **Final_Industry.ipynb**
Analyzes industry-wise growth over the years, identifying which sectors have performed the best and which have faced challenges. Special attention is given to sectors like Artificial Intelligence and E-commerce.

10. **map_visualizations.ipynb**
Generates visualizations to show the geographic distribution of unicorn companies. These visualizations include maps highlighting key innovation hubs and growth patterns.

Ensure you have the necessary API keys and data files in the correct directories before running the notebooks.

##📎 Appendix
Data Sources:
CB Insights
Kaggle Datasets
Presentation
The detailed analysis and visualizations have been compiled into a presentation. You can view the full presentation here.
(https://github.com/lanahuyen/Group_Project_1/blob/main/Presentation/Presentation_Group%207.pptx)

### Additional Notes
**Data Limitations:** While the data is comprehensive, it is essential to acknowledge potential limitations, such as missing values and varying data formats.
**Future Work:**Future analyses could benefit from additional data points, such as age, chronic ailments, or sleep disorders, which may provide a more holistic understanding of unicorn growth trends.
This README provides a comprehensive overview of the unicorn growth project, detailing the data processing steps, analysis, and visualizations used to derive insights from the data.
