# Netflix Dataset Visualization Guide

This guide summarizes the key insights and recommended visualizations for the Netflix dataset. It is intended for building exploratory analysis in Python or dashboards in Power BI.

---

## 1. Distribution of Content

**Goal:** See the balance between movies and TV shows.

* **Graph:** Countplot / Bar Chart
* **X-axis:** `Type_Of_Entertainment`
* **Y-axis:** Count
* **Insights:** Understand proportion of movies vs TV shows on the platform.

---

## 2. Films Added Over Time

**Goal:** Identify trends in adding content.

* **Graph 1:** Line chart

  * **X-axis:** `Year_Added`
  * **Y-axis:** Count of films
* **Graph 2:** Line chart with hue `Type_Of_Entertainment`

  * Shows trends of movies vs TV shows added per year.

---

## 3. Film Duration Analysis

**Goal:** Explore how long content is and compare TV shows vs movies.

* **Graph 1:** Histogram / Distribution plot

  * `Duration_Number`
* **Graph 2:** Boxplot

  * `Duration_Number` vs `Is_TV_Show`
  * **Insight:** TV shows tend to be shorter than movies.

---

## 4. Genre Insights

**Goal:** See which genres are most represented.

* **Graph 1:** Treemap

  * Size → number of films
  * Color → Genre
* **Graph 2:** Bar chart

  * Top 10 genres by number of films
* **Graph 3 (optional):** Count of films per genre over time (stacked bar with `Year_Added`)

---

## 5. Director & Country Analysis

**Goal:** Identify prolific directors and key content-producing countries.

* **Graph 1:** Horizontal bar chart

  * Top 10 directors by number of films (`Director` vs count)
* **Graph 2:** Horizontal bar chart

  * Top countries by number of films (`Country` vs count)

---

## 6. Ratings Analysis

**Goal:** Understand distribution of content ratings.

* **Graph:** Countplot / Bar chart

  * `Film_Rating` on X-axis, count on Y-axis
* Optional: stacked by `Type_Of_Entertainment` to compare movies vs TV shows

---

## 7. Correlation Insights

**Goal:** See numeric relationships.

* **Graph:** Heatmap (`sns.heatmap`) of numeric columns:

  * `Duration_Number`, `Film_Releasing_Year`, `Year_Added`, `Month_Added`, `Is_TV_Show`
* **Insight:** Quickly shows that TV shows are shorter than movies, slight trends over years, etc.

---

## 8. Scatter Plots / Trend Analysis

**Goal:** Explore relationships and trends.

* **Graph 1:** Scatter plot of `Film_Releasing_Year` vs `Duration_Number`

  * Optional color: `Is_TV_Show`
* **Graph 2:** Scatter of `Year_Added` vs `Duration_Number`

  * Can detect trends in content length over time

---

## Optional Advanced Analysis

* **Actor Analysis:** Split `Casts` into rows → top actors by appearances (bar chart)
* **Multi-genre films:** Analyze number of genres per film and see distribution (histogram)
* **Genre vs Duration:** Boxplot of `Duration_Number` per genre → which genres tend to be longer

---

## Summary of Must-Have Visuals

1. Movies vs TV shows (bar chart)
2. Content added per year (line chart)
3. Duration distribution and comparison (histogram + boxplot)
4. Top genres (treemap or bar chart)
5. Top directors and countries (bar charts)
6. Ratings distribution (bar chart)
7. Numeric correlations (heatmap)

These visuals provide actionable insights on content distribution, trends, and durations.
