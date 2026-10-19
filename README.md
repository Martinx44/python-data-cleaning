# Movie Industry Data Analysis Using Python

## Project Overview

This project explores a movie industry dataset using Python to investigate relationships between movie budgets, gross earnings, audience ratings, vote counts, genres, and production companies.

The objective is to identify patterns in movie financial performance, examine relationships between numerical variables, and investigate which production companies have accumulated the highest total gross earnings in the dataset.

The project applies exploratory data analysis (EDA), statistical correlation, data quality assessment, and data visualization to extract insights from historical movie data.

### Objectives

- Inspect the structure and quality of the movie dataset.
- Identify missing values and examine data types.
- Investigate potential duplicate records.
- Explore the relationship between movie budgets and gross earnings.
- Examine correlations between numerical movie attributes.
- Identify production companies with the highest aggregate gross earnings.
- Visualize distributions, relationships, and potential outliers.
- Explore categorical variables and their relationships with movie performance.

### Tools and Technologies

- Programming language: Python
- Data manipulation: pandas, NumPy
- Data visualization: Matplotlib, Seaborn
- Statistical analysis: Pearson correlation and regression plots
- Environment: Jupyter Notebook
- Data source: CSV file

### Dataset Description

The project uses a movie dataset containing 7,669 records and 15 original columns in the displayed output, covering movies released across several decades.

The dataset includes the following fields:

Column| Description
"name"| Movie title
"rating"| Movie content classification
"genre"| Movie genre
"year"| Recorded release year
"released"| Release date and country information
"score"| Movie rating score
"votes"| Number of recorded votes
"director"| Movie director
"writer"| Movie writer
"star"| Principal star associated with the movie
"country"| Country associated with the movie
"budget"| Recorded movie production budget
"gross"| Recorded gross earnings
"company"| Production company
"runtime"| Movie runtime

Note: The dataset contains missing values, and the precise currency and accounting basis for the financial fields should be verified before making comparisons across countries or years.

### Project Workflow

1. Data Loading and Preparation

Imported the dataset into a pandas DataFrame and inspected the first few records to understand its structure and contents.

Libraries used include pandas, NumPy, Matplotlib, and Seaborn.

Techniques: "pd.read_csv()", ".head()", DataFrame inspection.

2. Missing-Value Analysis

Calculated the percentage of missing values in each column.

The initial inspection identified approximately:

Column| Missing values
"rating"| 1%
"budget"| 28%
"gross"| 2%

The remaining columns displayed approximately 0% missing values when percentages were rounded to whole numbers.

The missing budget values are particularly relevant because they affect the number of movies available for budget-versus-revenue analysis.

3. Data Type Inspection

Examined column data types to distinguish numerical variables from text-based and categorical fields.

The numerical variables included "year", "score", "votes", "budget", "gross", and "runtime". Several descriptive fields, including movie titles, genres, directors, and production companies, were stored as objects.

This inspection established which variables could be used directly in numerical analysis and which required additional preprocessing.

4. Duplicate-Record Inspection

Applied pandas "drop_duplicates()" to examine duplicate records.

The displayed result still contained the full dataset, so the notebook should explicitly compare row counts before and after duplicate removal to determine whether any records were actually removed.

Technique: "DataFrame.drop_duplicates()".

5. Sorting Movies by Gross Earnings

Sorted the dataset by "gross" in descending order to identify movies with the highest recorded gross earnings.

The displayed results placed Avatar, Avengers: Endgame, and Titanic among the highest-grossing movies in the dataset.

Techniques: "sort_values()", descending sort order.

6. Outlier Analysis

Used a box plot to examine the distribution of movie gross earnings and identify potential extreme values.

Because gross earnings are highly unevenly distributed, a small number of blockbuster movies can dominate the scale of the visualization.

A scatter plot was also used to explore the relationship between movie budgets and gross earnings.

Techniques: Seaborn box plots, Matplotlib scatter plots.

7. Correlation Analysis

Calculated a Pearson correlation matrix for the numerical variables and visualized the results using a heatmap.

The displayed correlation results showed several notable relationships:

Variable pair| Pearson correlation| Interpretation
Budget and gross earnings| 0.740| Strong positive linear association
Votes and gross earnings| 0.631| Moderate-to-strong positive association
Budget and votes| 0.442| Moderate positive association
Score and votes| 0.409| Moderate positive association
Score and gross earnings| 0.186| Weak positive linear association

These results suggest that movies with larger recorded budgets tend to have higher gross earnings in this dataset. Movies with more votes also tend to have higher gross earnings.

However, correlation does not establish causation. These relationships may be influenced by release year, distribution reach, franchise popularity, genre, and other factors.

8. Regression and Relationship Visualization

Created regression plots to examine the relationships between:

- Movie budget and gross earnings.
- Movie score and gross earnings.

These visualizations help assess the direction and general strength of relationships between variables.

9. Production Company Revenue Analysis

Grouped movies by production company and summed their recorded gross earnings to identify the companies with the highest aggregate gross totals.

The top five companies in the displayed results were:

Rank| Production company| Aggregate gross earnings
1| Warner Bros.| 56.49 billion
2| Universal Pictures| 52.51 billion
3| Columbia Pictures| 43.01 billion
4| Paramount Pictures| 40.49 billion
5| Twentieth Century Fox| 40.26 billion

These figures represent the sums recorded in the dataset, not inflation-adjusted earnings or necessarily comparable lifetime totals for every company's entire film catalogue.

10. Categorical Data Encoding

Converted text-based columns into categorical codes to create a numerically encoded version of the dataset.

This was used to explore correlations across encoded columns.

However, assigning integer codes to nominal categories such as movie titles, directors, and production companies does not create meaningful numerical distances between those categories. Consequently, correlations involving arbitrary category codes should not be interpreted as substantive relationships.

For stronger statistical analysis, correlation calculations should prioritize appropriate numerical variables or use statistical methods designed for categorical data.

### Key Findings

Based on the displayed results:

- Budget and gross earnings: A Pearson correlation of approximately 0.74 indicates a strong positive linear association in the observed data.
- Audience engagement: Vote counts have a positive association with gross earnings, with a reported correlation of approximately 0.63.
- Audience scores: The relationship between movie scores and gross earnings is comparatively weak, with a reported correlation of approximately 0.19.
- Production company performance: Warner Bros. has the highest aggregate gross earnings among the companies displayed in the analysis.
- Data completeness: Budget data has a substantial missing-value rate, which should be considered when interpreting financial relationships.
- Revenue distribution: The presence of very high-grossing movies creates extreme values that can influence summary statistics and visualizations.

These are descriptive findings from the supplied notebook output and should not be interpreted as causal conclusions.

### Skills Demonstrated

- Python programming
- Exploratory data analysis
- Data quality assessment
- Missing-value analysis
- DataFrame manipulation with pandas
- Numerical analysis with NumPy
- Statistical correlation
- Data visualization with Matplotlib and Seaborn
- Regression plot interpretation
- Outlier exploration
- Grouping and aggregation
- Categorical data preprocessing

### Conclusion

This project demonstrates how Python can be used to explore a movie dataset, investigate financial performance, and visualize relationships between production budgets, audience engagement, ratings, and gross earnings.

The findings highlight the positive association between movie budgets and gross earnings, the relationship between vote counts and commercial performance, and the concentration of aggregate gross earnings among major production companies.

Further analysis could improve the project by addressing missing values, validating financial units, accounting for inflation, and investigating whether budget and other movie characteristics can predict gross earnings.

Author

### Martin Agu

Aspiring Data Analyst | Python | SQL | pandas | Exploratory Data Analysis | Data Visualization




# Zentel Network Service Ticket Analysis (Python)

## Project Overview

This project focuses on exploring and preparing telecommunications service ticket data using Python and pandas. The dataset contains customer service reports, ticket timestamps, fault categories, assigned operators, ticket statuses, and supporting reference tables.

The objective is to assess data quality, understand the structure of service operations data, and prepare the dataset for further analysis of ticket response times, issue resolution, operational performance, and service delivery.

### Project Objectives

- Load and inspect data from multiple Excel worksheets.
- Assess dataset structure, column data types, and missing values.
- Identify data quality issues that may affect analysis.
- Standardize data types, particularly ticket timestamps.
- Prepare service ticket data and reference tables for further analysis.
- Establish a foundation for investigating service response times, resolution efficiency, and ticket status patterns.

### Tools and Technologies

- Programming language: Python
- Data manipulation: pandas
- File handling: Python "pathlib"
- Data source: Microsoft Excel (".xlsx")
- Environment: Jupyter Notebook

### Dataset Description

The source workbook, "Zentel Network Service Ticket Data.xlsx", contains seven worksheets loaded into separate pandas DataFrames.

Worksheet| DataFrame| Purpose
Service Data| "zentel_service_data_df"| Main service ticket records
Employee| "zentel_employee_df"| Employee, designation, and manager information
Service Type| "zentel_service_type_df"| Service type reference data
Channel Type| "zentel_channel_type"| Service channel reference data
Fault Type| "zentel_fault_type_df"| Fault classification reference data
Location| "zentel_location_df"| Location reference data
Resources| "zentel_resources_df"| Resource reference data

#### Main Service Data Fields

The service dataset contains 5,998 records and 12 columns in the inspected output.

Column| Description
"Report ID"| Identifier for a service report or ticket
"Report Channel"| Channel through which the ticket was reported
"Customer Name"| Customer associated with the ticket
"State Key"| Location or state reference identifier
"Ticket Open Time"| Date and time the ticket was opened
"Ticket Resp Time"| Recorded response timestamp
"Issue Res Time"| Recorded issue-resolution timestamp
"Fault Type"| Classification of the reported fault
"Operator"| Staff member associated with the ticket
"Ticket Close Time"| Ticket closure timestamp or recorded status value
"Ticket Status"| Operational status of the ticket
"Business Status"| Business-level status of the ticket

Note: The meaning and consistency of the timestamp and status fields should be validated against the source documentation before calculating performance metrics.

## Project Workflow

1. Loading the Data

Used pandas "read_excel()" to import the seven worksheets from the Excel workbook into individual DataFrames.

Python's "pathlib" module was used to construct the file path.

Techniques: "Path", "pd.read_excel()", DataFrame creation.

2. Initial Data Inspection

Inspected the main service dataset using:

- ".head()" to preview records.
- ".shape" to examine the number of rows and columns.
- ".info()" to inspect data types and non-null counts.
- ".describe()" to obtain descriptive statistics where appropriate.

These operations provide an initial understanding of the dataset before performing data cleaning or analysis.

3. Missing-Value Assessment

Used ".isna().sum()" to identify missing values in each column.

The initial inspection identified 526 missing values in the "Fault Type" column, while the other 11 columns showed no missing values in the reported output.

These missing entries require further investigation to determine whether they represent unclassified faults, unavailable information, or another operational condition.

4. Data Type Inspection

Inspected column data types to distinguish datetime fields from text and categorical fields.

The initial output showed that:

- "Ticket Open Time", "Ticket Resp Time", and "Issue Res Time" were already represented as "datetime64[ns]".
- "Ticket Close Time" was stored as an "object" rather than a consistent datetime type.
- Several columns contained text-based identifiers and categorical values.

The next cleaning step is to validate and convert "Ticket Close Time" into a consistent datetime representation where appropriate.

5. Data Quality and Standardization

The initial inspection establishes the foundation for additional cleaning operations, including:

- Validating timestamp formats and chronological consistency.
- Checking for duplicate report identifiers.
- Inspecting categorical values for inconsistent spelling or formatting.
- Reviewing missing fault classifications.
- Validating relationships between service tickets and the employee, channel, fault, location, service type, and resource reference tables.

These steps should be completed and documented as the notebook develops.

### Potential Analytical Questions

Once data cleaning and validation are complete, the dataset can support investigations such as:

1. What is the average time between ticket opening and the recorded response?
2. How long does it take to resolve different types of service faults?
3. Which fault categories account for the highest number of tickets?
4. What proportion of tickets are completed, open, or active?
5. How does ticket volume vary by reporting channel or location?
6. How do ticket response and resolution times vary across operators?
7. Are there tickets with missing classifications or inconsistent status and timestamp combinations?

These are proposed analytical directions, not findings established by the current notebook.

### Skills Demonstrated

- Python programming
- Data ingestion from Excel
- DataFrame manipulation with pandas
- Exploratory data inspection
- Missing-value assessment
- Data type validation
- Data quality assessment
- Multi-table dataset preparation

Conclusion

This project establishes a foundation for analyzing telecommunications service operations. By loading the source workbook, inspecting the service ticket data, and identifying missing values and data type inconsistencies, the notebook begins the process of transforming raw operational data into a dataset suitable for further analysis.

The next stage is to complete data cleaning, validate the relationships between reference tables, engineer meaningful time-based metrics, and investigate service delivery performance.

Author

#### Martin Agu

Aspiring Data Analyst | Python | pandas | SQL | Data Cleaning | Exploratory Data Analysis







