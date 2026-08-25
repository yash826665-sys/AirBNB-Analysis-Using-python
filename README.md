# 🏠 Airbnb New York 2024 Data Analysis

## 📌 Project Overview

This project analyzes **Airbnb listing data for New York in 2024** using Python. The goal is to explore pricing, availability, room types, neighbourhoods, reviews, and other listing characteristics to identify useful patterns and relationships within the dataset.

The project covers the complete data analysis workflow, including **data loading, exploratory data analysis (EDA), data cleaning, feature engineering, visualization, and correlation analysis**.

## 📊 Dataset

The dataset contains **20,770 Airbnb listings** and **22 initial features**.

Some of the key columns include:

* `price` - Listing price
* `neighbourhood_group` - New York borough
* `neighbourhood` - Specific neighbourhood
* `room_type` - Type of accommodation
* `minimum_nights` - Minimum number of nights required
* `number_of_reviews` - Total number of reviews
* `reviews_per_month` - Average monthly reviews
* `availability_365` - Number of available days in a year
* `rating` - Listing rating
* `bedrooms` - Number of bedrooms
* `beds` - Number of beds
* `baths` - Number of bathrooms
* `latitude` and `longitude` - Geographic location

## 🛠️ Technologies & Libraries

* **Python**
* **Pandas** - Data manipulation and analysis
* **NumPy** - Numerical operations
* **Matplotlib** - Data visualization
* **Seaborn** - Statistical visualization
* **Jupyter Notebook** - Development environment

## 🔍 Project Workflow

### 1. Importing Dependencies

The project uses Python's major data analysis and visualization libraries:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### 2. Loading the Dataset

The Airbnb dataset was loaded using Pandas:

```python
data = pd.read_csv('new_york_listings_2024.csv', encoding_errors='ignore')
```

### 3. Initial Data Exploration

The dataset was explored using:

* `head()`
* `tail()`
* `shape`
* `info()`
* `describe()`
* Data type inspection

The initial dataset contained **20,770 rows and 22 columns**.

### 4. Data Cleaning

The following cleaning steps were performed:

* Identified missing values
* Removed rows containing missing values
* Checked for duplicate records
* Removed duplicate rows
* Converted `id` and `host_id` to object data types
* Verified the resulting dataset structure

After cleaning, the dataset contained no missing values or duplicate rows.

### 5. Exploratory Data Analysis

Several types of analysis were performed to understand the Airbnb market.

#### Price Distribution

A box plot and histogram were used to investigate the distribution of listing prices and identify extreme values.

For visualization purposes, listings with prices below **$1,500** were used to make the price distribution easier to interpret.

The price distribution is strongly right-skewed, with most listings concentrated at relatively lower prices and a smaller number of high-priced listings.

#### Availability Analysis

The distribution of `availability_365` was analyzed to understand how frequently listings are available throughout the year.

#### Borough-Level Pricing

Average listing prices were compared across New York's neighbourhood groups:

| Neighbourhood Group | Average Price |
| ------------------- | ------------: |
| Bronx               |       $107.99 |
| Brooklyn            |       $155.14 |
| Manhattan           |       $204.15 |
| Queens              |       $121.68 |
| Staten Island       |       $118.78 |

The analysis shows that **Manhattan has the highest average listing price** among the five boroughs in the analyzed data.

## 🧮 Feature Engineering

A new feature called **`price per bed`** was created to better understand the value of listings relative to their number of beds.

```python
df['price per bed'] = df['price'] / df['beds']
```

The average price per bed by neighbourhood group was then analyzed.

| Neighbourhood Group | Average Price per Bed |
| ------------------- | --------------------: |
| Bronx               |                $74.71 |
| Brooklyn            |                $99.79 |
| Manhattan           |               $138.71 |
| Queens              |                $76.34 |
| Staten Island       |                $67.73 |

Manhattan has the highest average price per bed in the analysis.

## 📈 Bivariate Analysis

The project investigates relationships between multiple variables, including:

* Price vs. neighbourhood
* Price vs. room type
* Price vs. number of reviews
* Minimum nights vs. price
* Availability vs. price
* Number of reviews vs. availability

A bar chart was used to compare prices across neighbourhood groups and room types, while scatter plots were used to examine relationships between numerical variables.

## 🗺️ Geographical Analysis

The latitude and longitude of Airbnb listings were visualized to understand their geographic distribution across New York.

Listings were categorized by room type to observe how different accommodation types are distributed geographically.

## 🔥 Correlation Analysis

A correlation heatmap was created for important numerical variables, including:

* Latitude
* Longitude
* Price
* Minimum nights
* Number of reviews
* Reviews per month
* Availability
* Beds

One notable relationship in the analysis is the positive correlation between **price and number of beds**, with a correlation of approximately **0.42**.

The strongest relationship among the analyzed variables is between **number of reviews and reviews per month**, at approximately **0.63**.

## 💡 Key Insights

* **Manhattan** has the highest average Airbnb listing price.
* Manhattan also has the highest average **price per bed**.
* Airbnb prices show a highly right-skewed distribution.
* Listing prices vary considerably across neighbourhood groups and room types.
* The geographic visualization shows a dense concentration of listings across New York City.
* The number of beds has a moderate positive relationship with listing price.
* Number of reviews and reviews per month show a relatively strong positive relationship.
* Availability varies significantly across listings throughout the year.

## 📁 Project Structure

```text
Airbnb-New-York-2024-Analysis/
│
├── AirBnb Python Project.ipynb
├── new york listings 2024.csv
└── README.md
```

## 🚀 How to Run the Project

1. Clone this repository.

2. Make sure Python is installed.

3. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

4. Place the dataset in the same directory as the Jupyter Notebook.

5. Launch Jupyter Notebook:

```bash
jupyter notebook
```

6. Open:

```text
AirBnb Python Project.ipynb
```

7. Run the notebook cells sequentially.

## 🎯 Project Purpose

This project demonstrates practical skills in:

* Data Cleaning
* Exploratory Data Analysis
* Data Visualization
* Feature Engineering
* Statistical Analysis
* Python/Pandas
* Identifying patterns and relationships in real-world datasets

## 👨‍💻 Author

**Yash Chaudhary**

Data Analytics Project | Python | Pandas | Data Visualization
