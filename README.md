# Books to Scrape — Web Scraping & Exploratory Data Analysis

An end-to-end Python data extraction, cleaning, and exploratory analysis pipeline built on [Books to Scrape](https://books.toscrape.com/).

## Project Workflow
1. **Web Requests & HTML Parsing:** Fetched catalogue and product detail pages using `requests` and parsed nested DOM elements (`<h1>`, `.breadcrumb`, `.star-rating`, `.price_color`, `.availability`) with `BeautifulSoup`.
2. **Regex & Data Cleaning:** Extracted numeric prices (`float`) and stock counts (`int`) from raw strings using Python's `re` module, and mapped text star ratings (`"One"`–`"Five"`) to integers (`1`–`5`).
3. **Structured Export:** Serialized cleaned records into `books_data.json` and `books_data.csv`.
4. **Exploratory Data Analysis (EDA):** Used `pandas` to compute summary statistics, rank top-priced titles, calculate average pricing per category via `.groupby()`, and filter 5-star rated books.

## Key Insights (Page 1 Sample — 20 Books)
* **Average Book Price:** £38.05 (Range: £13.99 – £57.25)
* **Average Rating:** 2.85 / 5.0
* **Top-Rated Titles:** 4 books achieved a 5-star rating

## Tech Stack
* **Language:** Python 3
* **Libraries:** `requests`, `beautifulsoup4`, `re`, `pandas`, `json`
* **Environment:** Jupyter Notebook

## Repository Structure
* `books_scraper.ipynb` — Complete step-by-step scraping, cleaning, and EDA notebook
* `books_data.json` — Cleaned dataset in JSON format
* `books_data.csv` — Cleaned dataset in CSV format
* `README.md` — Project documentation

## Author
**Yaqoob Khan** — [GitHub (@yaqoobkhangtr-ux)](https://github.com/yaqoobkhangtr-ux)