# 🎬 Netflix Content Analysis

An exploratory data analysis (EDA) of Netflix's global content catalog using Python. This project uncovers trends in content type, country of origin, genres, ratings, directors, and release patterns.

---

## 📌 Project Overview

This notebook performs end-to-end data analysis on the `netflix_titles.csv` dataset — from raw ingestion and cleaning to insightful visualizations. It answers questions like:

- How does Netflix's movie vs. TV show split look?
- Which countries dominate the platform?
- What genres are most prevalent?
- How has Netflix's content library grown over time?
- Who are the most prolific directors on the platform?

---

## 📂 Dataset

| Field | Description |
|---|---|
| `title` | Name of the movie or TV show |
| `type` | Movie or TV Show |
| `director` | Director(s) of the title |
| `cast` | Main cast members |
| `country` | Country of origin |
| `date_added` | Date the title was added to Netflix |
| `release_year` | Original release year |
| `rating` | Content rating (e.g., TV-MA, PG-13) |
| `duration` | Length in minutes (movies) or seasons (TV shows) |
| `listed_in` | Genre categories |

> **Source:** [Netflix Movies and TV Shows — Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** — data manipulation
- **NumPy** — numerical operations
- **Matplotlib** — plotting
- **Seaborn** — statistical visualizations
- **Google Colab** — notebook environment

---

## 🔍 Analysis Workflow

### 1. Data Loading & Initial Exploration
- Load `netflix_titles.csv` into a DataFrame
- Inspect shape, columns, data types, and a sample of rows

### 2. Data Cleaning
- Visualize missing values with heatmaps
- Fill nulls: `director`, `country`, `cast` → `"Unknown"`; `rating` → mode
- Remove duplicate rows
- Drop remaining rows with missing values

### 3. Exploratory Data Analysis

| Analysis | Visualization |
|---|---|
| Movies vs. TV Shows | Count plot |
| Top 10 Countries by Content | Bar chart |
| Content Rating Distribution | Horizontal count plot |
| Titles Released by Year | Line chart |
| Top 10 Genres | Horizontal bar chart |
| Top 10 Directors | Horizontal bar chart |
| Content Added to Netflix by Year | Line chart |
| Longest Movies | Sorted table |

---

## 💡 Key Insights

1. **Movies dominate** — Netflix's catalog has significantly more movies than TV shows.
2. **US leads content** — The United States contributes the largest share of titles on the platform.
3. **Drama rules** — Drama and International Movies are the most represented genres.
4. **Post-2015 boom** — Netflix saw rapid content growth starting around 2015, reflecting its global expansion strategy.
5. **Mature audience focus** — The majority of titles carry TV-MA or TV-14 ratings.
6. **Director concentration** — A small number of directors have multiple titles; most appear only once.
7. **Movie durations** — Most films fall in a moderate runtime range, with only a handful of outliers exceeding 3 hours.

---

## 🚀 Getting Started

### Run on Google Colab (Recommended)

1. Open the notebook in [Google Colab](https://colab.research.google.com/)
2. Upload `netflix_titles.csv` when prompted by the file upload cell
3. Run all cells in order (`Runtime → Run all`)

### Run Locally

```bash
# Clone the repo
git clone https://github.com/your-username/netflix-analysis.git
cd netflix-analysis

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Launch Jupyter
jupyter notebook netflix_analysis.ipynb
```

> **Note:** Replace the Google Colab file upload cell with:
> ```python
> df = pd.read_csv("netflix_titles.csv")
> ```

---

## 📁 Repository Structure

```
netflix-analysis/
│
├── netflix_analysis.ipynb   # Main analysis notebook
├── netflix_titles.csv       # Dataset (download from Kaggle)
└── README.md                # Project documentation
```

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
