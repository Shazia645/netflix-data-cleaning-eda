# Netflix Dataset Cleaning & Exploratory Data Analysis (EDA)

This repository contains a Data Cleaning and Analysis workflow performed on the official Netflix Titles dataset using Python and Pandas.

## Project Overview
The goal of this project is to clean, transform, and prepare raw Netflix data for further exploratory data analysis (EDA) and visualization. It resolves missing values, corrects data types, and prepares the dataset for trends evaluation (e.g., content distribution, release trends, genres, and ratings).

---

## Dataset Details
- **Raw File:** `netflix_titles.csv`
- **Cleaned File:** `netflix_clean.csv`
- **Total Records:** 8,807 rows × 12 columns

### Features / Columns:
- `show_id`: Unique identifier for each show
- `type`: Content category (`Movie` or `TV Show`)
- `title`: Name of the title
- `director`: Director of the show/movie
- `cast`: Actors involved
- `country`: Country of production
- `date_added`: Date when the content was added on Netflix
- `release_year`: Actual release year
- `rating`: Content rating (e.g., TV-MA, PG-13)
- `duration`: Duration in minutes (Movies) or seasons (TV Shows)
- `listed_in`: Genres / categories
- `description`: Short summary of the show

---

## Data Cleaning Steps Taken
1. **Initial Inspection:** Evaluated dataframe shape, missing values count, and checked for duplicate rows.
2. **Handling Missing Values:**
   - Critical null entries in `date_added`, `rating`, and `duration` were dropped due to low missing counts.
   - Categorical missing values in `director`, `cast`, and `country` were filled with `'Unknown'`.
3. **Data Type Parsing:** Converted string-formatted dates in `date_added` to standard `datetime64` format.
4. **Data Export:** Exported the final processed data to `netflix_clean.csv`.

---

##  Recommended Future Enhancements
- [ ] Parse `duration` into two distinct numeric columns: `duration_min` for Movies and `seasons` for TV Shows.
- [ ] Extract `year_added` and `month_added` from `date_added` for visual time-series trends.
- [ ] Unnest / Explode multi-value columns (`cast`, `country`, `listed_in`) for localized and actor-specific analysis.
- [ ] Add Matplotlib/Seaborn visual charts (Top Producing Countries, Movie vs TV Show split, Content Addition Trends).

---

##  How to Run
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Install required dependencies:
   ```bash
   pip install pandas notebook matplotlib seaborn
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```