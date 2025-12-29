# Real Estate Scraper - Imobiliária Chave de Ouro

## Overview

This project scrapes real estate listings from [Imobiliária Chave de Ouro](https://imobiliariachavedeouro.com.br/imoveis/) and collects detailed information about each property. It supports:

- Automatic paging through the website’s AJAX listing system.
- Extraction of property details: type, neighborhood, area, rooms, suites, parking spaces, and price.
- Collection of property images.
- Robust handling of HTTP 403 errors using a **header pool** to rotate User-Agent headers.
- Graceful error handling to skip invalid or missing data without stopping the scraper.

## Features

- **Header Pool:** Rotates User-Agent headers to avoid frequent 403 errors.  
- **Incremental Scraping:** Processes one page at a time, avoiding memory overload.  
- **Data Cleaning:** Converts area, price, and numeric fields into usable formats.  
- **Safe Execution:** Continues execution even if some properties fail to load.  
- **CSV Export:** Saves all collected data to a CSV file, ready for analysis.

## Data

- **Raw Data:** All scraped data is stored in the `data/raw/` folder.  
- **Clean Data:** A processed and cleaned version of the data is available in `data/processed/imoveis_clean.csv`.  
- **Analysis:** The cleaned dataset is ready for exploration, visualization, and modeling.  

## Exploratory Data Analysis (EDA)

We performed an exploratory analysis on the cleaned data, which includes:

- Distribution of properties by type (`house`, `apartment`, `land`, `other`).  
- Price distribution and boxplots per type of property.  
- Correlation analysis (heatmaps) between numeric features such as area, number of rooms, suites, parking spaces, and price.  
- Scatter plots of internal area vs. price to observe trends and outliers.  
- Top neighborhoods by number of properties.  
- Histograms of price and price per square meter.  

These EDA steps help to understand the market trends, identify patterns, and prepare the dataset for further predictive modeling or visualization.

## How to Run and Test

Open any Jupyter Notebook (Google Colab is recommended) and, inside the environment, open the `FinalScraping` notebook by clicking:

File > Open Notebook > select the script named FinalScraping

## License

This project is for educational and demonstration purposes.
