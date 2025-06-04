# 📦 Trade Data Analytics

This project provides a comprehensive analysis of international trade data (import and export) from 2010 to 2021. Using Python and visualization libraries like Matplotlib, it explores trends and patterns in global trade by year, country, and commodity classification (HS Code).

---

## 📊 Dataset Overview

The project merges two datasets:
- `2010_2021_HS2_export.csv`
- `2010_2021_HS2_import.csv`

These are combined into a unified trade dataset with the following columns:

| Column Name | Description |
|-------------|-------------|
| `year`      | Year of the trade transaction |
| `country`   | Trading partner country |
| `HSCode`    | Harmonized System code for product classification |
| `commodity` | Description of the traded product |
| `value`     | Trade value in USD |
| `flag`      | Trade type: "import" or "export" |

---

## 📈 Key Features

- 📌 Cleans and standardizes trade data
- 📈 Plots total trade value per year (2010–2021)
- 🔄 Combines import/export data for unified analysis
- 🧹 Handles missing data with `dropna()`
- 📁 Exports clean data to `new trade dataset.csv`

---

## 📂 File Structure

- `trade.ipynb` – Jupyter notebook with all code and visualizations
- `new trade dataset.csv` – Output of merged and cleaned trade data

---

## 📌 Example Visualization

The notebook includes a time-series line chart of total trade value by year:

```python
total_by_year = df_trade.groupby('year')['value'].sum()
plt.plot(total_by_year.index, total_by_year.values)
