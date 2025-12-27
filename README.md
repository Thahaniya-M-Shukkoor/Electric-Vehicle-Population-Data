# # Exploratory Data Analysis of Electric Vehicle Population
**Domain:** Environmental & Transportation Analytics

---

## 1. Introduction & Problem Definition (Task 1)

### 1.1 Aim of the Project
The primary aim of this project is to conduct a comprehensive **Exploratory Data Analysis (EDA)** on a sample of the electric vehicle population data. This study seeks to identify and quantify key trends in EV adoption, technology preferences, and policy alignment across various geographical segments.

### 1.2 Problem Definition
The global transition to Electric Vehicles (EVs) is essential for mitigating the environmental impact of transportation, primarily by reducing Greenhouse Gas (GHG) emissions and improving urban air quality. However, EV adoption is not uniform; it varies significantly by location, technology type (Battery Electric Vehicles vs. Plug-in Hybrid Electric Vehicles), and the presence of government incentives.

### 1.3 Problem Statement
The heterogeneous and rapidly evolving nature of EV adoption presents a challenge for effective environmental policy and infrastructure planning. Local governments and utility providers require clear, data-driven insights into where adoption is succeeding, what vehicle types are preferred, and how key technological factors (like range) influence policy eligibility to support a sustainable and accelerated transition to electric mobility.

### 1.4 Objectives of the Study
To address the problem statement, the project is guided by the following five key objectives:

1.  **Geographic Concentration:** To rank and quantify the concentration of EV adoption across different Counties and Cities to identify high-adoption hubs.
2.  **Adoption Growth:** To analyze and visualize the historical rate of EV adoption based on the 'Model Year' to understand market momentum.
3.  **Technological Progress:** To assess the improvement and evolution of the median 'Electric Range' over time as an indicator of battery technology advancement.
4.  **Market Preference:** To determine the market share split between Battery Electric Vehicles (BEV) and Plug-in Hybrid Electric Vehicles (PHEV) to understand consumer and manufacturer trends.
5.  **Policy Evaluation:** To examine the relationship between vehicle type, electric range, and CAFV (Clean Alternative Fuel Vehicle) Eligibility status to measure policy alignment.

---

## 2. Dataset Overview
To address the problem statement, we are utilizing a high-quality dataset containing information on the Electric Vehicle population.

* **Source:** Electric Vehicle Population Data (Washington State / Data.gov)
* **Dataset Size:** 2,000 records and 17 columns.
* **Data Variety:** The dataset includes a mix of:
    * **Categorical Data:** Make, Model, County, City, Electric Vehicle Type.
    * **Numerical Data:** Model Year, Electric Range, Base MSRP.
    * **Geospatial/Policy Data:** Legislative District, Vehicle Location, and CAFV Eligibility.

---
## 3. Data Loading and Initial Overview
* Libraries used:
   * **Pandas:** For data manipulation and structure.
   * **NumPy:** For numerical operations.
   * **Matplotlib & Seaborn:** For creating high-quality static visualizations.
* Structural Inspection: Performed initial checks using .info(), .head(), and .describe() to understand data types and numerical distributions.
* Inventory: Confirmed the presence of 17 initial columns, identifying mixed data types and potential areas for cleaning (e.g., null values in legislative districts).
---
## 4. Data Cleaning & Pre-processing
* **Data Integrity:** Conducted a thorough check for duplicates and handled missing values in geographic columns to ensure statistical accuracy.
* **Feature Engineering (Derived Columns):**
  * Categorizing CAFV Eligibility into three distinct groups: 'Eligible', 'Not Eligible', 'Unknown'
  * Categorizing Model Year into Eras for trend analysis: 'Early Adopters (<2015)','Mass Market Growth (2015-2019)','Current Expansion (2020+)'
  * Categorizing Electric Range: 'Unknown', 'Standard', 'Long', 'Ultra-High'
* **Data Aggregation:** Prepared summary tables for market share and geographic proportions to streamline the visualization process.
---
## 5. Exploratory Data Analysis & Visualization
This section presents a tiered analysis of the 2,000-record EV dataset, moving from basic distributions to complex variable interactions.
### I. Univariate Analysis
* **Focus:** Understanding the distribution and frequency of individual variables.
  * **Electric Range Distribution** – A histogram/KDE plot showing the spread of battery capabilities across the fleet.
  * **CAFV Eligibility Analysis** – A donut/pie chart illustrating the proportion of vehicles qualifying for Clean Alternative Fuel Vehicle incentives.
  * **Distribution of EV Types (BEV vs. PHEV)** – A breakdown of pure battery electric vs. plug-in hybrid models.
  * **Range Category Distribution** – A count plot of engineered categories (Standard, Long, Ultra-High Range).
### II. Bivariate Analysis
* **Focus:** Exploring the relationship between two distinct variables.
  * **Top 10 Countries by EV Adoption** – A bar chart mapping geographic locations against vehicle counts to identify adoption hotspots.
  * **EV Adoption Trends Over Time** – A line chart showing the relationship between Model Year and registration volume.
  * **Market Share by Manufacturer** – A ranking of top brands to identify market dominance.
  * **Top 10 Most Popular EV Models** – Identifying specific model performance within the dataset.
  * **Average Electric Range Evolution** – A time-series trend showing how battery technology (Mean Range) has improved by Model Year.
  * **Dominant Electric Utility Providers** – A categorical comparison of utility companies and the number of vehicles they serve.
### III. Multivariate Analysis
* **Focus:** Analyzing three or more variables to uncover deep correlations and patterns.
  * **Statistical Correlation Analysis** – A heatmap matrix analyzing the simultaneous interaction between Model Year, Electric Range, and Vehicle Age. This visual identifies the strength and direction of
              relationships across all numerical features in the dataset.

---
## 6. Conclusion and Recommendations (Task 4)
* **Project Summary**
This analysis of 2,000 electric vehicle records has provided a comprehensive look into the current state of EV adoption. Through extensive data cleaning and visualization, we have met all five project objectives.
* **Key Findings**
  * Geographic Concentration: Adoption is not uniform; it is heavily concentrated in specific urban hubs (e.g., King County), which account for the vast majority of registrations.
  * Adoption Growth: There has been an exponential surge in EV registrations since 2020, suggesting that the market has moved from "Early Adopters" to "Mass Market" growth.
  * Technological Advancement: The average electric range has steadily increased over the last decade, with modern vehicles frequently exceeding the 200-mile threshold, effectively reducing "range anxiety."
  * Market Leadership: While Tesla remains the dominant market leader, the increasing share of traditional manufacturers (Nissan, Kia, Chevrolet) indicates a maturing and more competitive marketplace.
  * Policy Impact: A significant portion of the fleet is CAFV-eligible, proving that government incentives remain a primary driver for consumer vehicle choice.
* **Recommendations**
  * Infrastructure Prioritization: Utility companies and government agencies should prioritize the installation of high-speed charging stations in high-density "County" clusters identified in our geographic analysis.
  * Targeted Incentives: As the market matures, incentives should shift from general rebates to targeted support for "Standard Range" affordable models to help lower-income segments transition to electric.
  * Grid Readiness: Major utility providers should accelerate smart-grid upgrades to handle the localized power demand spikes caused by high EV concentration in specific regions.
