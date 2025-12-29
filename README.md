How to run and test

open any jupyter notebook (Google Colab would be good) and, inside the environment, open the FinalScrping file by clicking:
  file>open notebook>*select the script named FinalScraping*

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
