# 🎬 Netflix Movie Data Analysis

An exploratory data analysis (EDA) project on a Netflix movie dataset, uncovering trends in genres, popularity, vote ratings, and release years using Python.

---

## 📁 Dataset

**File:** `mymoviedb.csv`

The dataset contains **9,827 movies** with the following columns:

| Column | Description |
|---|---|
| `Release_Date` | Date the movie was released |
| `Title` | Movie title |
| `Overview` | Short description of the movie |
| `Popularity` | Popularity score |
| `Vote_Count` | Number of votes received |
| `Vote_Average` | Average vote score (0–10) |
| `Original_Language` | Language the movie was originally in |
| `Genre` | Comma-separated list of genres |
| `Poster_Url` | URL to the movie poster |

---

## 🔍 Project Overview

This notebook performs a full EDA pipeline:

1. **Data Loading & Inspection** — shape, dtypes, nulls, duplicates
2. **Data Cleaning & Preprocessing**
   - Cast `Release_Date` to datetime and extract the year
   - Drop low-value columns: `Overview`, `Original_Language`, `Poster_Url`
   - Categorize `Vote_Average` into 4 bins: `not_popular`, `below_avg`, `average`, `popular`
   - Explode multi-valued `Genre` column into individual rows
3. **Data Visualization** — bar charts and histograms using Seaborn & Matplotlib

---

## 📊 Key Questions Explored

- What are the most frequent movie genres on Netflix?
- How are vote ratings distributed across movies?
- Which movie has the highest popularity, and what genre is it?
- Which release year had the most movies?

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** — data manipulation
- **NumPy** — numerical operations
- **Matplotlib** — plotting
- **Seaborn** — statistical visualizations

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/netflix-data-analysis.git
cd netflix-data-analysis
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Run the notebook

```bash
jupyter notebook netflix_data_analysis.ipynb
```

Make sure `mymoviedb.csv` is in the same directory as the notebook.

---

## 📂 Project Structure

```
netflix-data-analysis/
│
├── netflix_data_analysis.ipynb   # Main analysis notebook
├── mymoviedb.csv                 # Dataset
└── README.md                     # Project documentation
```

---

## 📌 Key Findings

- **Drama** and **Comedy** are the most frequently occurring genres in the dataset.
- Most movies fall in the `average` vote category based on the quartile-based classification.
- The dataset is clean — no null values or duplicates were found in the raw data.
- Movie releases are concentrated heavily in recent years, with a clear spike visible in the release year histogram.
