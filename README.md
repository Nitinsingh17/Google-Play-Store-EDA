# Google Play Store | App Market Intelligence & Exploratory Data Analysis

**Python • Pandas • NumPy • Matplotlib • Seaborn • Statistical Analysis • Data Visualization**

[![Python](https://img.shields.io/badge/Python-Data%20Analysis-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Cleaning-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-20BEFF?logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/lava18/google-play-store-apps)
![Status](https://img.shields.io/badge/Status-Exploratory%20Analysis-success)

## Executive Summary

**What drives app popularity on Google Play Store, and how do app characteristics relate to user ratings, installations, and engagement?**

This project explores a historical Google Play Store dataset containing **10,841 app records** to identify meaningful patterns across app categories, ratings, installations, pricing, reviews, and app sizes.

Using Python, the project covers the complete exploratory analytics workflow from raw-data inspection and cleaning to statistical comparisons, visualizations, and interpretation.

The analysis is organized around **25 analytical questions**, progressing from foundational data exploration to more advanced comparisons.

The focus is not simply on producing charts, but on understanding what the available data can and cannot tell us about app marketplace behavior.

### Project at a Glance

| Metric | Result |
|:---|---:|
| Raw Dataset | 10,841 records |
| Final Cleaned Dataset | 10,358 records |
| Original Features | 13 |
| Duplicate Records Removed | 483 |
| Valid App Categories | 33 |
| Average App Rating | 4.19 / 5 |
| Free App Share | ~92.6% |
| Rating vs. Installs Correlation | ~0.05 |
| Analytical Questions | 25 |

*Metrics represent the historical dataset and analysis results, not current Google Play Store statistics.*

---

## Explore the Project

### [View Full Analysis Notebook](https://github.com/Nitinsingh17/Google-Play-Store-EDA/blob/main/app-insights-for-google-play-data.ipynb)

Explore the Python code, preprocessing steps, analytical questions, tables, visualizations, and documented findings.

**[View Repository](https://github.com/Nitinsingh17/Google-Play-Store-EDA)** | **[Access Original Dataset](https://www.kaggle.com/datasets/lava18/google-play-store-apps)** | **[Download Notebook](https://github.com/Nitinsingh17/Google-Play-Store-EDA/raw/refs/heads/main/app-insights-for-google-play-data.ipynb)**

---

## 1. Business Problem

The Google Play Store contains applications spanning multiple categories, pricing models, audiences, and installation levels.

Understanding these differences can help frame questions relevant to:

- **App developers:** How do ratings, size, and app categories differ across the market?
- **Product analysts:** Which characteristics are associated with higher installation thresholds?
- **Marketing teams:** What categories and genres contain more highly installed applications?
- **Business stakeholders:** How do free and paid app listings differ in ratings, reviews, and market representation?

### Central Research Question

**How are app characteristics associated with ratings, installation thresholds, and user engagement in the historical Google Play Store dataset?**

This is an exploratory, descriptive study. It does not claim to establish causal factors behind app success.

---

## 2. Project Objectives

The analysis was designed to:

1. Clean and transform an inconsistent real-world dataset into an analysis-ready format.
2. Understand the distribution of applications across categories, genres, and pricing models.
3. Investigate differences in ratings, reviews, and installations.
4. Examine associations between app size, price, ratings, and installs.
5. Explore patterns in app last-update dates.
6. Present meaningful insights through Python-based visualizations.
7. Identify data limitations that affect business interpretation.

---

## 3. Technology Stack

| Technology | Application |
|:---|:---|
| Python | Analytical programming |
| Pandas | Data cleaning, filtering, grouping, aggregation |
| NumPy | Numerical preprocessing and operations |
| Matplotlib | Exploratory charts and plots |
| Seaborn | Statistical and comparative visualizations |
| Jupyter Notebook | Interactive analysis, execution, and documentation |
| Kaggle | Historical dataset source |

### Technical Skills Demonstrated

`Data Cleaning` `Data Wrangling` `Missing Value Treatment` `Data Type Conversion` `GroupBy & Aggregation` `Correlation Analysis` `Exploratory Data Analysis` `Statistical Interpretation` `Data Visualization` `Analytical Storytelling`

---

## 4. Dataset Description

**Dataset:** Google Play Store Apps

**Source:** [Kaggle - Google Play Store Apps](https://www.kaggle.com/datasets/lava18/google-play-store-apps)

The dataset contains information on mobile applications listed on the Google Play Store.

### Original Features

| Feature | Description |
|:---|:---|
| App | Application name |
| Category | Primary application category |
| Rating | Average user rating |
| Reviews | Number of user reviews |
| Size | Application download size |
| Installs | Installation count bracket |
| Type | Free or paid |
| Price | Application price |
| Content Rating | Intended audience classification |
| Genres | Application genre |
| Last Updated | Recorded last-update date |
| Current Ver | Current app version |
| Android Ver | Android compatibility information |

### Data Quality Challenges

The original dataset required cleaning due to:

- Missing numerical and categorical values
- Duplicate application records
- Inconsistent numerical formatting
- Installation values containing commas and plus signs
- Price values containing currency symbols
- App sizes represented in KB, MB, or `Varies with device`
- A malformed category entry
- Date values requiring conversion

These issues were addressed before performing the main exploratory analysis.

---

## 5. Analytical Methodology

The project follows a five-stage analytical workflow:

**Data Acquisition → Data Quality Assessment → Data Cleaning → Exploratory Analysis → Insight Interpretation**

### Phase 1: Data Inspection

- Loaded the dataset into a Pandas DataFrame.
- Inspected column names, data types, and sample records.
- Identified missing values and duplicate records.
- Reviewed the data structure before transformation.

### Phase 2: Data Cleaning

- Filled missing ratings using the dataset's average rating.
- Handled selected missing categorical values using their mode or `Unknown`.
- Converted installation brackets into numeric lower-bound values.
- Removed currency symbols from app prices.
- Standardized app-size values into MB where available.
- Converted last-update fields to datetime format.
- Removed 483 duplicate records and one malformed category record.

**Result:** A cleaned dataset containing 10,358 records.

### Phase 3: Exploratory Data Analysis

Organized the analysis into three levels:

| Level | Questions | Analytical Focus |
|:---|---:|:---|
| Basic | 10 | Ratings, category counts, installs, free/paid split, app sizes |
| Intermediate | 10 | Correlation, pricing, category comparisons, genre patterns |
| Advanced | 5 | Rating rankings, update-date trends, install bins, genre analysis, sentiment feasibility |

Some advanced questions require additional data or methodological corrections before they can be considered resolved.

### Phase 4: Visualization

Used Matplotlib and Seaborn to examine:

- Distribution of app sizes
- Content ratings versus app ratings
- App size versus installation thresholds
- Last-update year trends
- Category-level comparisons

### Phase 5: Interpretation

Connected numerical results to practical business questions while distinguishing descriptive patterns from evidence of causation.

---

## 6. Key Findings & Business Interpretation

### Finding 01: Free Apps Dominate the Dataset

**~92.6% of the recorded app listings are free.**

At the relevant analysis stage, the notebook identifies:

| App Type | Records |
|:---|---:|
| Free | 9,593 |
| Paid | 765 |

**Interpretation**

Free-to-download applications represent the overwhelming majority of this historical sample.

For a market analyst, this makes pricing model an important variable when comparing app distribution and engagement.

**Business implication:** Free and paid app segments should be analyzed separately before drawing conclusions about audience reach.

### Finding 02: Average App Ratings Are Generally Positive

**Average Rating: 4.19 / 5**

The analysis reports that 8,413 listings have ratings of 4.0 or higher at the corresponding stage of the notebook.

**Interpretation**

Most recorded ratings fall toward the favorable end of the scale.

However, missing ratings were replaced with the overall mean during preprocessing. Therefore, some reported rating statistics include imputed rather than directly observed values.

**Business implication:** Analysts should consider both rating values and rating availability when comparing app quality.

### Finding 03: Higher Installs Do Not Necessarily Mean Higher Ratings

**Pearson Correlation: Approximately 0.05**

The analysis measures a very weak positive linear relationship between app ratings and normalized installation threshold values.

**Interpretation**

Applications with higher recorded installation brackets do not consistently have higher user ratings.

**Business implication:** Installation scale and user satisfaction should be considered separate performance dimensions.

This finding does not prove that ratings have no influence on installs. It only describes the measured linear association in this dataset.

### Finding 04: Rating Performance Varies by Category

The notebook reports the following leading average-rated categories:

| Category | Average Rating |
|:---|---:|
| EDUCATION | 4.37 |
| EVENTS | 4.36 |
| ART_AND_DESIGN | 4.35 |

**Interpretation**

Average ratings differ across categories, potentially reflecting differences in audience expectations, app characteristics, and sample composition.

**Business implication:** Category-level comparisons can provide useful context, but category sample sizes and rating availability must also be considered.

### Finding 05: Free Apps Have Higher Average Review Counts

| App Type | Mean Review Count |
|:---|---:|
| Free | 437,328 |
| Paid | 11,900.55 |

**Interpretation**

Free apps have substantially higher mean review counts in this historical dataset.

Averages may be influenced by exceptionally popular applications.

**Business implication:** Review counts should be interpreted alongside the distribution of reviews, installation brackets, and differences in app reach.

These findings do not establish that making an app free will cause more reviews.

### Finding 06: Installation Activity Is Concentrated in Selected Categories

The notebook's category-level analysis places the following categories prominently in summed installation threshold values:

- GAME
- COMMUNICATION
- SOCIAL
- PRODUCTIVITY
- TOOLS

**Interpretation**

A relatively small set of categories accounts for substantial recorded installation activity.

Because installs are represented as lower-bound brackets, summing them gives an approximate comparison metric rather than actual cumulative downloads.

### Finding 07: App Size Alone Does Not Explain Installation Levels

The size-versus-installs scatterplot shows applications with different sizes across a wide range of installation brackets.

**Interpretation**

No simple relationship is visually established between app size and recorded installs.

**Business implication:** App performance should be evaluated using multiple characteristics rather than a single variable.

---

## 7. Visual Analysis

The notebook includes graphical exploration to support the numerical findings.

| Visualization | Purpose |
|:---|:---|
| App Size Distribution | Understand the distribution of application sizes |
| Content Rating vs. Rating | Compare ratings across audience classifications |
| App Size vs. Installs | Explore the relationship between size and adoption levels |
| Last-Update Year Trend | Analyze the distribution of recorded last-update years |

**[Open Notebook to Explore Charts and Results](https://github.com/Nitinsingh17/Google-Play-Store-EDA/blob/main/app-insights-for-google-play-data.ipynb)**

---

## 8. Analytical Limitations

A reliable data analysis must explain the limitations of its evidence.

**Historical data:** This dataset is a historical snapshot and does not represent the current Google Play Store.

**Installation brackets:** Values such as `1,000,000+` indicate minimum installation thresholds, not exact downloads.

**Imputed ratings:** Some missing values were replaced with statistical estimates.

**Update frequency:** The dataset contains last-update dates, not complete update histories. Therefore, actual update intervals cannot be reliably determined.

**Review sentiment:** Sentiment analysis cannot be completed using review counts alone. Individual review text would be required.

**Review rankings:** The existing notebook includes a review-ranking calculation that requires correction before its results are used as verified rankings.

**Causality:** Correlations and group comparisons do not establish causal relationships.

These limitations are documented to prevent misleading conclusions.

---

## 9. Repository Structure

```text
Google-Play-Store-EDA/
│
├── app-insights-for-google-play-data.ipynb
│   │
│   ├── Dataset Inspection
│   ├── Missing Value Treatment
│   ├── Data Cleaning & Transformation
│   ├── Basic EDA Questions
│   ├── Intermediate EDA Questions
│   ├── Advanced Analysis Questions
│   ├── Data Visualizations
│   └── Findings & Conclusions
│
└── README.md
    └── Project Overview & Documentation
```

*The original dataset is hosted on Kaggle and is not included in this repository.*

---

## 10. Getting Started

### Prerequisites

- Python 3
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

### Step 1: Clone the Repository

```bash
git clone https://github.com/Nitinsingh17/Google-Play-Store-EDA.git
cd Google-Play-Store-EDA
```

### Step 2: Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn notebook
```

### Step 3: Download the Dataset

Download `googleplaystore.csv` from:

[Google Play Store Apps - Kaggle Dataset](https://www.kaggle.com/datasets/lava18/google-play-store-apps)

### Step 4: Launch the Notebook

```bash
jupyter notebook
```

Open:

`app-insights-for-google-play-data.ipynb`

### Step 5: Configure the Dataset Path

The notebook originally references this Kaggle dataset path:

```python
data = pd.read_csv(
    "/kaggle/input/datasets/lava18/google-play-store-apps/googleplaystore.csv"
)
```

For local execution, place the CSV in the repository directory and change the loading code to:

```python
data = pd.read_csv("googleplaystore.csv")
```

Run the notebook cells sequentially.

**Note:** A successful run requires the dataset to be downloaded and available at the configured path.

---

## 11. Future Improvements

Potential next steps for expanding this project:

- Correct the highest-reviewed app ranking.
- Strengthen missing-value treatment and compare results before and after imputation.
- Add sample-size-aware category comparisons.
- Use logarithmic scales for highly skewed review and installation data.
- Add interactive visualizations or a dashboard.
- Incorporate actual review text for sentiment analysis.
- Add automated data quality checks and validation.
- Improve reproducibility through a dependency file and dataset-loading instructions.

These are planned enhancements, not features already implemented.

---

## 12. Conclusion

This project demonstrates how Python can be used to transform a real-world dataset into structured analytical findings.

It highlights the importance of:

- Preparing inconsistent data before analysis
- Understanding the effects of missing values
- Examining relationships across multiple variables
- Choosing appropriate visualizations
- Interpreting statistical results carefully
- Communicating insights with their limitations

The analysis illustrates how descriptive data analytics can support informed exploration of app marketplace behavior while avoiding unsupported claims about what drives app success.

---

## Author

**Nitin Singh**

Data Analytics Project | Python | Exploratory Data Analysis

[GitHub Profile](https://github.com/Nitinsingh17) | [Project Repository](https://github.com/Nitinsingh17/Google-Play-Store-EDA)

---

*If you found this analysis useful, consider starring the repository.*
