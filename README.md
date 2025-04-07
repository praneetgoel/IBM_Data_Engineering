# 🌍 World Economies ETL Project

This project automates the extraction and processing of country GDP data from an archived Wikipedia page. It simulates a real-world scenario where you, a junior data engineer at an international firm, must create a repeatable ETL pipeline for economic analysis.

---

## 📖 Project Scenario

An international firm is expanding globally and needs up-to-date GDP data for strategic planning. You've been hired to:

- Extract GDP (in billions of USD) from a reliable source (IMF data via Wikipedia)
- Convert it to usable formats (CSV, JSON, SQLite DB)
- Provide a filtered query showing countries with economies > $100 billion
- Log all ETL steps to a file for transparency and auditing

---

## ⚙️ Tech Stack

- Python 3
- pandas
- BeautifulSoup (bs4)
- SQLite (`sqlite3`)
- JSON
- NumPy

---

## 📂 Project Files


---

## 🔄 ETL Pipeline

### ✅ Extract
Scrapes nominal GDP data from this archived Wikipedia page:
[Archived Link](https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29)

### 🔧 Transform
- Removes commas from numeric values
- Converts GDP from millions to billions
- Rounds values to 2 decimal places

### 💾 Load
- Saves clean data to:
  - `Countries_by_GDP.csv`
  - `Countries_by_GDP.json`
  - SQLite table `Countries_by_GDP`

### 🔍 Query
Filters for countries with GDP > $100 billion using SQL

### 🧾 Logging
Every step is logged with timestamps in `etl_project_log.txt`

---

## 🚀 How to Run

```bash

# Install dependencies
pip install pandas beautifulsoup4 numpy

# Run the script
python etl_project_gdp.py
