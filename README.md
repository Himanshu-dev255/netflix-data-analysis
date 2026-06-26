# 🎬 Netflix Content Analysis

An exploratory data analysis (EDA) of Netflix's movies and TV shows catalog, exploring content type distribution, country-wise production, and growth trends over time.

## 📁 Dataset

- **Source:** [Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows) (Kaggle)
- **Size:** 8,807 titles → cleaned to 8,790 after removing rows with missing `date_added`, `rating`, or `duration`
- **Columns:** `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`

## 🧹 Data Cleaning

| Column | Missing Values | Treatment |
|---|---|---|
| director | 2,634 | Filled with `"Unknown"` |
| cast | 825 | Filled with `"Unknown"` |
| country | 831 | Filled with `"Unknown"` |
| date_added | 10 | Row dropped |
| rating | 4 | Row dropped |
| duration | 3 | Row dropped |

## 📊 Key Findings

### 1. Movies dominate the catalog
Netflix's library is split roughly **70% movies (6,126 titles)** and **30% TV shows (2,664 titles)**, suggesting a historical focus on acquiring standalone films over deep TV libraries.

![Movies vs TV Shows](movies_vs_tv.png)

### 2. The US and India lead content production
**United States** contributes the most content by far (**2,809 titles**), followed by **India** (**972 titles**) as a clear second. The UK, Japan, and South Korea also show meaningful representation, reflecting Netflix's international content investment.

![Top 10 Countries](top_countries.png)

### 3. Content growth peaked in 2019, then declined
Additions were minimal before 2015, then grew sharply — from **426 titles in 2016** to a peak of **2,016 in 2019**. Additions declined for two straight years after (**1,879 in 2020**, **1,498 in 2021**), possibly reflecting a shift toward fewer, higher-budget originals or pandemic-related production slowdowns.

![Content Added Per Year](content_per_year.png)

## 🛠️ Tools Used

`Python` · `Pandas` · `Seaborn` · `Matplotlib` · Google Colab

## 🚀 How to Run

1. Clone this repo
2. Download `netflix_titles.csv` from Kaggle and place it in the project folder
3. Open the notebook in Jupyter or Google Colab
4. Run all cells

---

*Project by Himanshu — built while learning Python for data analysis.*
