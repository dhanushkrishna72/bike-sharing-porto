# Bike Sharing Demand Analysis

An exploratory data analysis project using Python to understand bike-sharing demand, customer behaviour, and the factors associated with rental activity.

This project explores the [UCI Bike Sharing Dataset](https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset), focusing on hourly rental records from the Capital Bikeshare system in Washington, D.C. The analysis uses Pandas, NumPy, and Matplotlib to identify patterns and translate them into possible operational insights.

## Project Overview

The goal of this project is to understand how bike rental demand changes with time, weather, temperature, and customer type.

The analysis focuses on questions such as:

- During which hours is rental demand highest?
- How do registered and casual customers use the service differently?
- How does demand vary between working days and non-working days?
- What relationship exists between weather conditions and rentals?
- How are temperature and rental demand related?
- How does demand change across seasons and months?
- What can the distribution of rental counts and outliers tell us?

## Dataset

- **Source:** [UCI Machine Learning Repository – Bike Sharing Dataset](https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset)
- **Original system:** Capital Bikeshare, Washington, D.C.
- **Period:** 2011–2012
- **File used:** `hour.csv`
- **Observations analysed:** 17,379 hourly records

The dataset includes time-related, weather-related, and rental-count variables.

Some important columns:

| Column | Description |
|---|---|
| `season` | Season code |
| `hr` | Hour of the day |
| `weekday` | Day of the week |
| `workingday` | Whether the day is a working day |
| `weathersit` | Weather condition category |
| `temp` | Normalised temperature |
| `atemp` | Normalised feels-like temperature |
| `hum` | Normalised humidity |
| `windspeed` | Normalised wind speed |
| `casual` | Rentals by casual customers |
| `registered` | Rentals by registered customers |
| `cnt` | Total rental count |

**Note:** `cnt` is the sum of `casual` and `registered`. The `temp`, `atemp`, `hum`, and `windspeed` columns are normalised values, not direct readings in their usual physical units. The `workingday` column groups weekends and holidays as non-working days.

## Tools and Libraries

- **Python** – Core programming language
- **Pandas** – Data loading, cleaning, grouping, and aggregation
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualisation
- **Jupyter Notebook** – Interactive analysis

## Analysis and Visualisations

The notebook explores the dataset through the following analyses:

1. Hourly bike rental demand
2. Casual vs. registered customer demand
3. Working-day vs. non-working-day demand
4. Hourly demand across weather conditions
5. Average rentals by weather category
6. Temperature vs. rental demand
7. Feels-like temperature vs. rental demand
8. Seasonal rental demand
9. Customer demand by season
10. Rental-count distributions
11. Yearly rental demand comparison
12. Monthly rental trends
13. Outlier analysis
14. Correlation analysis

Visualisations are saved in the `images/` directory.

## Key Observations

- Registered customers show stronger morning and evening demand peaks, while casual customers show relatively higher activity during afternoon hours.
- Working days and non-working days have different hourly demand patterns.
- Average rental demand decreases as weather conditions become less favourable.
- Temperature has a moderate positive correlation with rental demand (approximately **0.40** in this dataset).
- Actual temperature and feels-like temperature are highly correlated (approximately **0.988**).
- Outliers in rental counts may represent genuine periods of high demand and should not automatically be treated as incorrect data.

These are exploratory observations, not proof of causation. Some operational recommendations, especially location-based allocation and dynamic pricing, would require additional station-level, geographical, and pricing data.

## Running the Project

### 1. Clone the repository

```bash
git clone https://github.com/dhanushkrishna72/bike-sharing-porto.git
cd bike-sharing-porto
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
```

macOS / Linux:

```bash
source .venv/bin/activate
```

Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install pandas numpy matplotlib jupyter
```

### 4. Download the dataset

Download the Bike Sharing Dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset).

Extract the files and place `hour.csv` in the project's `data/raw/` directory.

### 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the project's analysis notebook and run the cells.

## Project Structure

```text
bike-sharing-porto/
├── data/
│   └── raw/
│       └── hour.csv              # Download separately
├── images/
│   └──                         # Analysis visualisations
├── notebooks/
│   └── bike_sharing_eda.ipynb
├── .gitignore
└── README.md
```

The structure above describes the intended organisation of the project. Adjust the notebook filename or folder paths if your repository uses different names.

## What's Next?

This project currently focuses on exploratory data analysis. The next step is to use the patterns identified here to explore bike rental demand prediction.

Planned work includes comparing feature combinations, preparing data for modelling, and evaluating machine learning models using appropriate validation metrics.

## References

Fanaee-T, H. (2013). *Bike Sharing* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5W894

- [UCI Bike Sharing Dataset](https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset)
- [Medium Article – Beyond the Graphs: Exploring Bike Sharing Demand with Python](https://pluto-explain.medium.com/beyond-the-graphs-exploring-bike-sharing-demand-with-python-d5ad871f282f)
- [Previous Project – RetailPulse](https://pluto-explain.medium.com/retailpulse-revisiting-python-libraries-through-a-small-data-analytics-project-e208a4978c48)

---

This project is a learning exercise focused on strengthening practical data analysis skills and developing the habit of connecting analytical results to real-world questions.
