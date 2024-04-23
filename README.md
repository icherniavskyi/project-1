# project-1
# SP500 Stock performance and REITS( Real Estate Interest Trusts) in the year 2020

## This project explores the relationships between the stock performances of the top companies in the united states based on the S&P index.It further delves into the analysis of comapnies across the real estate industry, Healthcare and Technology sectors in 2020 and key economic indicators including mortgage rates, inflation, and unemployment. The analysis addresses the following key questions:

  - What was the annual performance of REITs across and their geographical locations?
  - How did mortgage rates affect the stock performance of REITs?
  - What impact did inflation have on the stock performance of REITs?
  - How did unemployment rates influence the stock performance of REITs?
  - How did stocks perform in the healthcare and Technology sector?
  - What impacts did stock prices have on revenue growth and company size?

## Data Summary and Acquisition

The analysis leverages four datasets to investigate the aforementioned questions:

### S&P 500 Companies Dataset:
  - Details: Contains comprehensive information on companies listed in the S&P 500.
  - Columns: 16 (e.g., tickers, sectors, industries, EBITDA, revenue growth, locations)
  - Rows: 503
### S&P 500 Stocks Dataset:
  - Details: Provides trading data for the tickers on specific trading days.
  - Columns: 8 (e.g., open prices, close prices, highs, lows)
  - Rows: 1,805,770
### Inflation Dataset:
  - Details: Captures monthly U.S. inflation rates.
  - Time Range: 2014 – 2024
  - Columns: 15
  - Rows: 10
### Unemployment Dataset:
  - Details: Includes monthly U.S. unemployment rates.
  - Time Range: 2014 – 2024
  - Columns: 13
  - Rows: 10
### Mortgage Dataset:
  - Details: Lists bi-monthly mortgage rates in the U.S.
  - Time Range: 2005 – 2022
  - Columns: 2
  - Rows: 932

## Analysis Goals
The ultimate aim is to utilize these datasets to draw insights into how major economic indicators affect the financial performance of Healthcare companies, Technology companies, real estate companies, specifically REITs, during the economically turbulent year of 2020.
Analysis Presentation : https://docs.google.com/presentation/d/1n67gkTu9tx_g2f6br0v94TxOjDFKTYprEh44wrhTVZY/edit#slide=id.g2cd668485f1_0_6

## Data Preparation:

To effectivaely analize abovementioned datasets whent to significant transformations:

### S&P 500 Stocks Dataset
<img width="575" alt="Stock_data" src="https://github.com/icherniavskyi/project-1/assets/160045374/6145f47a-d6ed-465b-9654-3e75d354cc98">
<img width="655" alt="Stock_data2" src="https://github.com/icherniavskyi/project-1/assets/160045374/75c5dea5-4ae0-4e56-b426-12ee4db3674e">

### S&P 500 Companies Dataset:
<img width="647" alt="Company_data" src="https://github.com/icherniavskyi/project-1/assets/160045374/902acbe8-10ea-4152-ae27-04dd7bd3dbc2">

### Inflation Dataset
<img width="332" alt="Inflation_data" src="https://github.com/icherniavskyi/project-1/assets/160045374/f364e951-94b1-451c-9b45-7d4fcc58103e">
  
  - Inflation, Mortgage and Unemployment shair the methods used in the shippet above. 

## Findings and Outcomes:

### Geographic locations of the companies:
![image](https://github.com/icherniavskyi/project-1/assets/160045374/335bda6b-b384-4a4d-a613-598eaa0d5b77)

The heat map serves as a powerful tool for data storytelling. In this case, users can interact with a map by hovering on points which represent companies. Hover displays information about the companies such as Name, EBITDA, Industry, Revenue Growth and City. This information is useful for investor interested in particular area or city.

# Annual Performance Rate

![image](https://github.com/icherniavskyi/project-1/assets/160045374/3a455790-797e-4e29-8964-f12b613914b8)

#### Findings:
  1. Significant disparity in performance among the companies. For instance, CSGP and EQIX, have shown growth with 38.37% and 18.43% annual performance. On the other end of     the spectrum, SPG shows decline in -39.82% annual performance.
  2. Few companies managed to record positive growth. This  might suggest this companies have resilient business models and adaptability.
  3. The wide range of performance across companies, from significant gains to steep losses, suggests high volatility within the real estate sector in 2020.
  4. Identifying top ten performing stocks and bottom ten performing stocks in Healthcare and technology for the year 2020.
  5. A slight correlation between unemployment and ROR

 
# Getting Started

## Dependencies and Installation
Before running the scripts, please ensure that all the necessary libraries are installed. The project relies on several Python libraries for data manipulation, visualization, and geolocation services. Follow the steps below to set up your environment:

### Required Libraries
* pandas: For data manipulation and analysis.
* matplotlib: For creating static, interactive, and animated visualizations in Python.
* geopandas: For working with geospatial data in Python.
* hvplot: For creating interactive visualizations with HoloViews.
* numpy: For numerical operations.
* geopy: For geocoding through the Nominatim service.
  
To install obovementioned packages please use this code in your terminal: pip install pandas matplotlib geopandas hvplot numpy geopy. Before running the script import this dependanices to your enviornment. 

Additionaly, to use geopy please import Nominatim and specify the name for your project. 
from geopy.geocoders import Nominatim
geolocator = Nominatim(user_agent="your_project_name")

## Data Access and Import:

* To access the datasets for the analysis please use this link: https://drive.google.com/drive/folders/17UnABE7xp6zeR05I0eqgJl03bJhQZ6tC?usp=drive_link
* After downloading the data please provide their pathes to the objects on top of the script:
  - stock_data = pd.read_csv()
  - companies_data = pd.read_csv()
  - inflation = pd.read_excel()
  - unemployment = pd.read_excel()
  - mortgage = pd.read_csv()

    ADITYA 
## Calculating Monthly ROR
using the basic formula for ror 
(initial-final)/ final *100

#Monthly ROR of all REITS from S&P500 
using group by with date and creating and new data frame dropping unnecessary columns to create datafram to show ROR by month
##Philliphs Curve
using a scatter plot to plot to plt the data set for unemployment and inflation and run a regression on it to show data trend 
#Unemp vs ror 
plotting on a scatter unemployment and ROR agaisnt time to see a side by side visual

#economic insights and break down of factors to measure and how to measure them and to create a scale to measure ROR and its affects from other economic factors.
#
