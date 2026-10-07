# Amazon Prime Video Catalogue – Exploratory Data Analysis

## Project Overview

This project presents an Exploratory Data Analysis (EDA) of an Amazon Prime Video catalogue dataset.

The objective is to understand the composition and characteristics of the catalogue and identify insights that can support content planning, audience targeting, catalogue diversification, and talent-related decisions.

The analysis covers content types, genres, release trends, production countries, age certifications, ratings, audience voting, runtime, and relationships between different content metrics.

---

## Business Problem

In the competitive streaming industry, platforms need to continuously understand their content catalogue to support effective content planning and audience targeting.

This analysis aims to answer questions such as:

- Which genres are most represented in the catalogue?
- What is the distribution of Movies and TV Shows?
- How are Movies and TV Shows distributed across major genres?
- Which production countries are represented?
- How are IMDb ratings distributed across different content types and countries?
- How has the catalogue changed across different release years?
- What age certifications are most represented?
- How does runtime differ between Movies and TV Shows?
- What relationships exist between IMDb and TMDB metrics?
- Which titles are highly rated based on sufficient audience votes?
- What patterns can be observed in audience voting and ratings?

---

## Dataset

The project uses two datasets:

### 1. Titles Dataset

The Titles dataset contains **9,871 records and 15 columns**.

Important attributes include:

- Title
- Content Type
- Release Year
- Runtime
- Seasons
- Genres
- Production Countries
- Age Certification
- IMDb Score
- IMDb Votes
- TMDB Score
- TMDB Popularity

### 2. Credits Dataset

The Credits dataset contains **124,235 records and 5 columns**.

Important attributes include:

- Title ID
- Person ID
- Name
- Role
- Character

The Credits dataset is used to analyse actors, directors, and their association with different titles and genres.

---

## Tools & Technologies

The analysis was performed using:

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Google Colab**
- **Jupyter Notebook**

---

## Data Preparation

Before performing the analysis, the datasets were inspected and cleaned.

The preparation process included:

- Checking dataset structure and data types
- Identifying and removing duplicate records
- Analysing missing values
- Handling missing categorical values
- Handling missing numerical values
- Creating an IMDb missing-information feature
- Preparing analysis-specific dataframes
- Converting relevant numerical fields into appropriate formats

Duplicate records identified included:

- **3 duplicates** in the Titles dataset
- **56 duplicates** in the Credits dataset

For categorical fields, meaningful placeholders were used where appropriate, such as:

- `Unknown` for missing age certifications
- `Not Applicable` for movie seasons

For numerical variables such as IMDb Score, IMDb Votes, TMDB Popularity, and TMDB Score, missing values were handled using group-based median imputation.

---

## Exploratory Data Analysis

The analysis follows a structured EDA approach:

### Univariate Analysis

The first stage focuses on understanding individual variables.

Examples include:

- Genre Distribution
- Movies vs TV Shows
- Age Certification Distribution
- Release Year Analysis
- Production Country Distribution

### Bivariate Analysis

The second stage examines relationships between two variables.

Examples include:

- Movies vs TV Shows across Genres
- IMDb Ratings across Production Countries
- Runtime of Movies vs TV Shows
- Average IMDb Score by IMDb Vote Range

### Multivariate Analysis

The final stage examines relationships between multiple numerical variables.

Examples include:

- Correlation Heatmap
- Pair Plot

This progression helps move from understanding individual characteristics to identifying deeper relationships within the dataset.

---

## Key Visualizations

The project contains **20 visualizations**, covering areas such as:

1. Genre Distribution
2. Movies vs TV Shows
3. Average Cast Size Across Major Genres
4. Movie vs TV Show Proportions Across Major Genres
5. Top Actors & Directors by Genre
6. Production Countries
7. IMDb Rating Range Across Production Countries
8. Talent Density Across Production Volume Levels
9. Movie & TV Show Releases by Year
10. Releases by Five-Year Period
11. Growth of Highly Rated Content
12. IMDb Rating Distribution: Movies vs TV Shows
13. Genre Evolution Over Time
14. IMDb Rating Concentration by Content Type
15. Top-Rated Titles
16. Correlation Heatmap
17. Pair Plot
18. Age Certification Distribution
19. Runtime Distribution of Movies vs TV Shows
20. Average IMDb Score by IMDb Vote Range

---

## Key Business Insights

The analysis provides insights that can support several areas of content planning and catalogue management.

### Genre & Content Mix

Genre analysis helps identify heavily represented genres and understand how Movies and TV Shows are distributed across different genres. This can support discussions around catalogue balance and diversification.

### Geographic Representation

Production-country analysis provides an overview of the geographic diversity of the catalogue and can support discussions around regional and international content expansion.

### Audience Segmentation

Age certification analysis helps understand how content is distributed across different audience age groups and may highlight opportunities to strengthen specific audience segments.

### Content Ratings

IMDb analysis provides insights into rating distributions, highly rated titles, and the relationship between ratings and audience voting.

### Talent Analysis

Actor and director analysis can help identify talent frequently associated with specific genres or highly rated titles, supporting future content and talent planning.

### Runtime

Runtime analysis provides insight into differences in content length between Movies and TV Shows, which can support content-format planning.

---

## Business Limitations

The dataset does not contain direct Amazon-specific business metrics such as:

- Viewing hours
- Watch time
- Revenue
- Subscriber retention
- Customer engagement
- Actual Amazon Prime Video viewing data

Therefore, IMDb and TMDB metrics should be treated as external indicators rather than direct measures of Amazon Prime Video performance.

Similarly, a genre being highly represented in the catalogue does not necessarily mean that it is the most popular or commercially successful genre.

The findings should therefore be considered supporting evidence for business decisions rather than direct measures of business performance.

---

## Conclusion

This project provides a structured analysis of **9,871 Amazon Prime Video catalogue titles and 124,235 credit records** through 20 visualizations.

The analysis provides insights into:

- Genre representation
- Content type distribution
- Production countries
- Age certifications
- Release trends
- IMDb ratings
- Audience voting
- Runtime
- Talent
- Relationships between content metrics

These findings can support areas such as genre diversification, regional content planning, audience targeting, and talent selection.

---

## Future Improvements

The analysis can be extended through:

- Deeper statistical analysis
- Predictive modelling
- Audience segmentation
- Content recommendation analysis
- Interactive dashboard development
- Integration with actual viewing and engagement data
- Analysis of revenue, watch time, and subscriber behaviour

These improvements could help move the project from descriptive analysis toward more advanced and actionable business decision-making.

---

## Project Structure

```text
Amazon-Prime-Video-EDA/
│
├── Project_2.ipynb
├── README.md
└── datasets/
    ├── titles.csv
    └── credits.csv
