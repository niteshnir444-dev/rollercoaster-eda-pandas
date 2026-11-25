# rollercoaster-eda-pandas
Exploratory Data Analysis (EDA) of 1,000+ roller coasters using Python, Pandas, Matplotlib, and Seaborn—covering data cleaning, univariate distributions, and feature relationships.
# Exploratory Data Analysis: Roller Coaster Database

An end-to-end Exploratory Data Analysis (EDA) project built in Python using **Pandas**, **NumPy**, **Matplotlib**, and **Seaborn**. This notebook explores historical and physical attributes of over 1,000 roller coasters—walking through initial data inspection, cleaning, deduplication, univariate distributions, and multivariate feature relationships.

> **Reference:** Follows the Pandas EDA workflow tutorial from the [Medallion Data Science YouTube Channel](https://www.youtube.com/channel/UCxladMszXan-jfgzyeIMyvw).

---

## Project Structure

```text
├── introduction-to-exploratory-data-analysis.ipynb   # Main Jupyter Notebook with code & visualizations
├── coaster_db.csv                                    # Raw roller coaster dataset (1,087 rows × 56 columns)
└── README.md                                         # Project documentation

Dataset Overview
Source File: coaster_db.csv

Raw Dimensions: 1,087 records × 56 features

Cleaned Dimensions: 990 unique roller coasters × 13 core features

Key Features Analyzed:

Coaster_Name, Location, Status, Manufacturer, Type_Main (Steel, Wood, Other)

Year_Introduced, Opening_Date

Speed_mph, Height_ft, Inversions, Gforce

latitude, longitude

Analysis Workflow
Step 0 – Imports & Data Loading: Configured Pandas display options (display.max_columns = 200), set the Matplotlib ggplot visual style, and loaded coaster_db.csv.

Step 1 – Data Understanding: Audited dataset shape, data types (dtypes), summary statistics (describe()), and sample rows (head()).

Step 2 – Data Preparation:

Filtered 56 raw columns down to 13 relevant analytical features.

Parsed Opening_Date into standard datetime format and standardized column names.

Audited missing values (isna()) and removed duplicate coaster entries based on Coaster_Name, Location, and Opening_Date.

Step 3 – Feature Understanding (Univariate Analysis):

Analyzed coaster construction trends by year (peaking in 1999 with 46 introductions and 2000 with 45).

Examined primary track material counts (Steel: 728, Wood: 191, Other: 71).

Visualized top introduction years via bar charts and coaster speed distributions using histograms and Kernel Density Estimate (KDE) plots.

Step 4 – Feature Relationships (Multivariate Analysis):

Explored correlations between Speed_mph, Height_ft, and Year_Introduced using scatter plots, pairplots, heatmaps, and grouped aggregations.
