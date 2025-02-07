# Hypothesis Testing with Men's and Women's Soccer Matches

## Project Description

This project analyzes historical soccer data to determine whether women's international matches have higher goal counts than men's matches. Using Python, I will enhance my statistical testing skills while exploring global soccer patterns.

## 1. Understanding the Dataset

Both datasets—Men's and Women's soccer match data—contain similar columns, which include match information, teams, scores, and tournament types.

### Men's Dataset Overview:
- **Number of Entries:** 44,353 matches.
- **Columns:**
    - `Unnamed: 0`: An index column (may not be relevant for analysis).
    - `date`: The date the match was played (YYYY-MM-DD).
    - `home_team`, `away_team`: The teams playing the match.
    - `home_score`, `away_score`: Goals scored by each team.
    - `tournament`: The type of tournament (e.g., Friendly, FIFA World Cup, etc.).
- **Data Types:**
    - `home_score`, `away_score`: Integers.
    - `date`, `home_team`, `away_team`, `tournament`: Strings.
- **Memory Usage:** ~2.4 MB.

### Women's Dataset Overview:
- **Number of Entries:** 4,884 matches.
- **Columns:** Similar structure to the men's dataset.

## 2. Exploratory Data Analysis (EDA)

### Inspecting the Data:
- Checking dataset structure, data types, and missing values.
- Displaying the first few rows for a quick overview.

### Summary Statistics:
- Calculating mean, median, standard deviation, minimum, and maximum for goal counts.
- Women's matches show higher average goals and greater variability than men's matches.

### Distribution Analysis:
- Analyzing the distribution of matches over time.
- Plotting histograms of total goals per match to check for skewness and outliers.

### Top Participating Teams:
- Identifying teams with the most matches in each dataset.
- Women's soccer has fewer matches and dominant teams contributing to high-scoring games.

## 3. Main Process

### Filtering and Transforming Data:
- Converting `date` to datetime format for filtering.
- Filtering matches played after 2002 and from FIFA World Cup tournaments.
- Adding a `group` column to distinguish between men's and women's matches.
- Creating `goals_scored` column (sum of `home_score` and `away_score`).

### Statistical Summary:
- Women's matches have a higher average (2.98 vs. 2.51 for men's) and median (3 vs. 2 goals).
- Greater variability in women's matches (std = 2.02 vs. 1.65 for men).
- Higher goal count max in women’s matches (13 vs. 8 in men’s matches).

### Statistical Testing
- **Hypothesis:** Women's matches have a higher mean goal count than men's.
- **Test Used:** Wilcoxon-Mann-Whitney (Mann-Whitney U Test).
- **Results:**
    - P-value = 0.0051 (less than 0.01 significance level).
    - **Null hypothesis rejected** → Women’s matches have statistically higher goal counts.
    - **Effect size:** Small but significant, with women's matches more likely to have higher scores about 56% of the time.

## Conclusion
The statistical analysis provides evidence that women’s international soccer matches tend to have higher goal counts than men’s. While the effect size is small, the results are statistically significant, suggesting a meaningful difference in scoring trends between men’s and women’s soccer at the international level.

