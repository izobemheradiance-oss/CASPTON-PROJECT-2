# CASPTON-PROJECT-2
# IMDb Top 1000 Movies – Exploratory Data Analysis

## Project Overview

This project focuses on performing Exploratory Data Analysis (EDA) on the IMDb Top 1000 Movies dataset using Python.

The aim is to analyze movie performance, audience preferences, box office revenue, movie genres, directors, ratings, and runtime to generate useful insights that can help a movie production studio make data-driven decisions.

The analysis explores different factors that may influence a movie's commercial success and audience reception.

## Project Objectives

The main objectives of this project are to:

- Identify the top 10 highest-grossing movies.
- Compare the top 5 movies based on IMDb audience ratings and Metascore critic ratings.
- Identify the five directors with the highest number of movies in the dataset.
- Calculate the average box office revenue for the top directors.
- Determine which primary movie genre generates the highest average gross revenue.
- Examine the relationship between audience votes and box office revenue.
- Investigate the relationship between movie runtime and IMDb ratings.
- Identify the most suitable movie genre and runtime for a production studio.
- Analyze box office revenue across different age certificates.

## Tools and Technologies

The following tools and Python libraries were used:

- **Python** – Programming language used for the analysis.
- **Pandas** – Data cleaning, manipulation, and analysis.
- **NumPy** – Numerical operations.
- **Matplotlib** – Data visualization.
- **Jupyter Notebook** – Development environment for performing the analysis.

## Dataset

The project uses the IMDb Top 1000 Movies dataset (`imdb_top_1000.csv`).

Some of the important columns include:

- `Series_Title` – Movie title.
- `Released_Year` – Year the movie was released.
- `Certificate` – Movie age classification.
- `Runtime` – Duration of the movie.
- `Genre` – Movie genre.
- `IMDB_Rating` – Audience rating.
- `Director` – Movie director.
- `Meta_score` – Critic rating.
- `No_of_Votes` – Number of audience votes.
- `Gross` – Box office revenue.

## Data Cleaning and Preparation

Before conducting the analysis, the following preprocessing steps were performed:

1. Imported the dataset using Pandas.
2. Examined the dataset structure and data types.
3. Removed commas from the Gross column and converted it into a numeric format.
4. Replaced missing Gross values with 0.
5. Replaced missing Meta_score values with 0.
6. Replaced missing Certificate values with "NON".
7. Converted Runtime from text to integer values.
8. Created a new column called `Primary_Genre` by extracting the first genre listed for each movie.

## Exploratory Data Analysis

The project answers several business and analytical questions through data analysis and visualization.

### 1. Highest-Grossing Movies
Identified the top 10 movies with the highest box office revenue.

### 2. Audience vs. Critics Ratings
Compared the top five movies ranked by IMDb ratings against the top five movies ranked by Metascore.

### 3. Director Performance
Identified the five directors with the highest number of movies in the dataset and calculated their average gross revenue.

### 4. Genre Performance
Analyzed average gross revenue across primary genres and visualized the top eight genres using a horizontal bar chart.

### 5. Audience Votes vs. Box Office Revenue
Used correlation analysis and a scatter plot to investigate the relationship between the number of audience votes and movie revenue.

The analysis found a moderate positive correlation of approximately **0.63**.

### 6. Runtime vs. IMDb Ratings
Grouped movie runtimes into 30-minute intervals and compared their average IMDb ratings using a horizontal bar chart.

### 7. Studio Recommendations
Used the results of the genre and runtime analysis to recommend a suitable movie genre and runtime for a production studio.

### 8. Age Certificate vs. Box Office Revenue
Compared average gross revenue and revenue variability across movie certificates.

## Key Findings

- The top five movies based on IMDb ratings are not identical to the top five based on Metascore.
- Audience votes and box office revenue have a moderate positive correlation of approximately 0.63.
- The Family genre was identified as the genre with the highest average gross revenue in the analysis.
- Runtime was grouped into 30-minute intervals to investigate its relationship with audience ratings.
- Box office performance was also examined across different age certificates.

## Conclusion

This project demonstrates how Python and data analysis techniques can be used to explore movie industry data, identify patterns, and generate insights for business decision-making.

By analyzing movie ratings, revenue, genres, directors, runtime, and audience engagement, the project provides useful information that can support a movie studio in making more informed production decisions.

---
