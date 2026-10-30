# CASPTON-PROJECT-2
# 🎬 IMDb Movie Insights | Movie Industry Data Analysis

An Exploratory Data Analysis (EDA) project exploring IMDb's Top 1000 Movies dataset to uncover insights into movie ratings, box-office revenue, genres, directors, audience engagement, and movie runtime.

---

## 📑 TABLE OF CONTENTS

- [PROJECT OVERVIEW](#-project-overview)
- [OBJECTIVE](#-objective)
- [DATASET](#-dataset)
- [KEY FEATURES](#-key-features)
- [DATA CLEANING AND PREPROCESSING](#-data-cleaning-and-preprocessing)
- [EXPLORATORY DATA ANALYSIS](#-exploratory-data-analysis)
- [KEY FINDINGS](#-key-findings)
- [BUSINESS RECOMMENDATIONS](#-business-recommendations)
- [TOOLS AND TECHNOLOGIES](#-tools-and-technologies)
- [PROJECT STRUCTURE](#-project-structure)
- [HOW TO RUN THE PROJECT](#-how-to-run-the-project)
- [CONCLUSION](#-conclusion)

---

## 🎥 PROJECT OVERVIEW

The movie industry generates substantial amounts of data, ranging from audience ratings and critic reviews to box-office revenue and audience engagement.

This project explores the **IMDb Top 1000 Movies dataset**, containing information on 1,000 highly rated movies, to understand the factors associated with movie popularity, audience preferences, and commercial performance.

Using Python, Pandas, NumPy, and Matplotlib, the project applies data cleaning, manipulation, statistical analysis, and visualization techniques to transform raw movie data into meaningful insights.

The analysis also approaches the dataset from a business perspective, examining which movie genres generate the highest average revenue and what factors a production studio could consider when making investment decisions.

## 🎯 OBJECTIVE

The primary objective of this project is to investigate movie industry data and answer important analytical and business questions.

The analysis focuses on:

1. Identifying the ten highest-grossing movies in the dataset.
2. Comparing the top five movies based on IMDb audience ratings and Metascore critic ratings.
3. Identifying the five directors with the highest number of movies and evaluating their average gross revenue.
4. Determining which primary movie genre generates the highest average gross revenue.
5. Investigating the relationship between audience votes and box-office revenue.
6. Examining whether movie runtime influences audience ratings.
7. Recommending a suitable movie genre for a production studio based on average gross revenue.
8. Identifying age-rating certificates associated with more consistent box-office revenue.

## 📊 DATASET

The project uses the **IMDb Top 1000 Movies dataset**.

The dataset contains:

- 1,000 movie records.
- 16 original columns.
- Movie titles and release years.
- Audience and critic ratings.
- Movie genres and runtime.
- Directors and cast information.
- Audience voting statistics.
- Box-office gross revenue.

### Dataset Source

The dataset is commonly available through Kaggle under the title IMDb Movies Dataset (Top 1000).

[Explore IMDb Top 1000 Movies datasets on Kaggle](https://www.kaggle.com/datasets?search=imdb+top+1000+movies)

## 🔑 KEY FEATURES

The dataset contains the following important columns:

| Column | Description |
|---|---|
| Poster_Link | URL of the movie poster |
| Series_Title | Title of the movie |
| Released_Year | Year the movie was released |
| Certificate | Movie age-rating classification |
| Runtime | Duration of the movie in minutes |
| Genre | Genre classification of the movie |
| IMDB_Rating | Audience rating on IMDb |
| Overview | Short description of the movie |
| Meta_score | Professional critics' score |
| Director | Name of the movie director |
| Star1 | First leading actor |
| Star2 | Second leading actor |
| Star3 | Third leading actor |
| Star4 | Fourth leading actor |
| No_of_Votes | Number of audience votes |
| Gross | Box-office gross revenue |

Additional analytical features were created during preprocessing, including:

- `Primary_Genre` – Extracted the first listed genre from the original Genre column.
- `Runtime_Bin` – Grouped movie durations into 30-minute intervals.

## 🧹 DATA CLEANING AND PREPROCESSING

Before performing the analysis, the dataset was inspected and prepared using Pandas and NumPy.

The following operations were performed:

- Imported the dataset using Pandas.
- Examined the dataset structure using `info()` and `dtypes`.
- Converted the Gross column from comma-separated text into numerical values.
- Replaced missing Gross values with zero.
- Replaced missing Meta_score values with zero.
- Replaced missing Certificate values with `NON`.
- Removed the `min` text from the Runtime column and converted it into an integer.
- Extracted the first genre from the Genre column to create `Primary_Genre`.
- Configured numerical display formatting for better readability.

## 📈 EXPLORATORY DATA ANALYSIS

The project investigates eight major analytical questions.

### 1. Top 10 Highest-Grossing Movies

Identified the ten movies with the highest recorded box-office gross revenue.

The analysis ranked movies in descending order to identify the strongest commercial performers.

### 2. Audience Ratings vs. Critics' Ratings

Compared the top five movies according to IMDb ratings against the top five according to Metascore.

The analysis revealed that both rankings were different, showing that audience preferences do not always align with professional critics' evaluations.

### 3. Director Performance Analysis

Grouped movies by director and calculated:

- Number of movies directed.
- Average box-office gross revenue.

The five directors with the highest movie counts were identified and compared.

### 4. Primary Genre vs. Average Gross Revenue

Grouped movies according to their primary genre and calculated the average box-office gross revenue.

A horizontal bar chart was created to rank the eight highest-performing genres.

### 5. Audience Votes vs. Box-Office Revenue

Investigated whether movies receiving more audience votes tend to generate higher box-office revenue.

Correlation analysis and a scatter plot were used to examine the relationship between `No_of_Votes` and `Gross`.

### 6. Movie Runtime vs. IMDb Ratings

Grouped movie runtimes into 30-minute intervals and calculated the average IMDb rating for each interval.

A horizontal bar chart was used to compare audience ratings across different movie durations.

### 7. Genre Selection for a Production Studio

Evaluated average gross revenue across primary movie genres to identify which genre could represent an attractive investment opportunity for a production studio.

### 8. Age Certificate vs. Revenue Consistency

Grouped movies according to their age-rating certificates and calculated:

- Average gross revenue.
- Standard deviation of gross revenue.
- Number of movies in each certificate category.

Only certificate categories with at least ten movies were retained for comparison.

## 💡 KEY FINDINGS

The analysis produced the following insights:

**1. Highest-Grossing Movie**

Star Wars: Episode VII – The Force Awakens ranked first, with recorded gross revenue of **$936,662,225**.

**2. Audience vs. Critics' Ratings**

The top five IMDb-rated movies were not identical to the top five Metascore-rated movies, highlighting differences between audience preferences and professional critical opinions.

**3. Director Performance**

Alfred Hitchcock recorded the highest number of movies in the dataset, with 14 movies.

Steven Spielberg followed with 13 movies and recorded an average gross revenue of approximately $190.63 million.

**4. Genre Performance**

Family emerged as the highest-performing primary genre based on average gross revenue.

| Primary Genre | Average Gross Revenue |
|---|---:|
| Family | $219.56M |
| Action | $116.38M |
| Animation | $104.56M |
| Adventure | $73.25M |
| Horror | $66.90M |
| Biography | $53.98M |
| Drama | $31.32M |
| Crime | $29.72M |

**5. Audience Engagement and Revenue**

The correlation between audience votes and gross revenue was approximately **0.6021**, indicating a moderate positive relationship.

This suggests that movies with higher audience engagement tend to record higher box-office revenue.

**6. Runtime and Audience Ratings**

The 30–60-minute and 300–330-minute runtime categories recorded the highest average IMDb rating of 8.20.

However, these results should be interpreted carefully because some runtime categories may contain relatively few movies.

**7. Production Studio Recommendation**

Based on the average gross revenue comparison, Family was identified as the strongest primary genre for further investment consideration.

**8. Certificate Consistency**

Passed had the lowest standard deviation in gross revenue among the certificate categories included in the analysis, followed by Approved.

This indicates comparatively lower revenue variability in those categories, although their sample sizes were smaller.

## 🏢 BUSINESS RECOMMENDATIONS

Based on the findings, the following recommendations can be considered by movie production studios:

- **Genre Investment:** Family movies could be considered for further investment research because they recorded the highest average gross revenue.
- **Director Selection:** Studios can examine directors' previous production records and commercial performance when evaluating potential collaborations.
- **Audience Engagement:** Audience voting activity can provide useful information about movie popularity and its relationship with commercial performance.
- **Movie Duration:** Production studios should evaluate audience ratings across different runtime categories when planning movie duration.
- **Revenue Risk:** Standard deviation can help studios understand the variability of box-office revenue across different certificate categories.

These findings should be considered alongside production budgets, marketing costs, inflation, and distribution expenses before making actual investment decisions.

## 🛠️ TOOLS AND TECHNOLOGIES

The following tools and Python libraries were used throughout the project:

| Tool | Application |
|---|---|
| Python | Programming and data analysis |
| Pandas | Data cleaning and manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Jupyter Notebook | Interactive analysis and documentation |

### Python Libraries

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

## 📁 PROJECT STRUCTURE

```text
IMDb-Movie-Analysis/
│
├── CASPTON PROJECT REPORT_2.ipynb
│
├── imdb_top_1000.csv
│
└── README.md
```

## ⚙️ HOW TO RUN THE PROJECT

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

### 2. Navigate to the Project Folder

```bash
cd YOUR-REPOSITORY
```

### 3. Install the Required Libraries

```bash
pip install pandas numpy matplotlib jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Run the Notebook

Open `CASPTON PROJECT REPORT_2.ipynb` and execute the cells sequentially.

Ensure that `imdb_top_1000.csv` is available in the project directory.

## ⚠️ LIMITATIONS

- The dataset represents only the selected IMDb Top 1000 movies and does not cover the entire movie industry.
- Missing Gross and Meta_score values were replaced with zero, which can affect statistical calculations.
- Gross revenue does not account for production budgets, inflation, or marketing expenses.
- Correlation does not establish causation.
- Some runtime categories contain relatively few observations, which may affect the reliability of their average ratings.
- The analysis uses the first listed genre rather than considering every genre associated with a movie.

## 🚀 CONCLUSION

This project demonstrates how exploratory data analysis can be used to extract meaningful insights from movie industry data.

Through data cleaning, statistical analysis, grouping, correlation, and visualization, the project explored the relationship between movie genres, directors, audience engagement, runtime, ratings, and box-office revenue.

The findings identified Family as the highest-performing primary genre by average gross revenue within the dataset, while also highlighting a moderate positive relationship between audience votes and box-office earnings.

Overall, this project demonstrates practical skills in Python-based data analysis, data preprocessing, exploratory data analysis, data visualization, and business-oriented interpretation.

