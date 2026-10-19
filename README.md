# movies-python-data-cleaning
Movie Data Analysis 🎬
This project is all about diving into a dataset of movies to see how different factors like budget, ratings, and more relate to a movie's success. We use Python libraries like Pandas, NumPy, Matplotlib, and Seaborn for the analysis.

#What's Inside
Dataset: Info on movies like title, rating, genre, budget, gross revenue, and more.
Analysis: We explore correlations, check out data distributions, spot outliers, and see how different features relate.
Visuals: Plenty of plots and charts to make the data easier to digest.

#Getting Started
Clone the repo:

#bash
Copy code
git clone https://github.com/yourusername/moviedata-analysis.git
Install the necessary Python packages:

#bash
Copy code
pip install -r requirements.txt
Run the analysis by opening the Jupyter notebook or running the Python script:

bash
Copy code
jupyter notebook MovieDataAnalysis.ipynb
or

bash
Copy code
python MovieDataAnalysis.py
Key Takeaways
Budget vs. Gross: There's a strong link between how much is spent on a movie and how much it earns.
Ratings and Genres: Certain ratings and genres tend to have higher gross revenue.
Top Movies: We also look at which companies are behind the big earners.
Contributing
Got ideas or found something off? Feel free to open an issue or submit a pull request.




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







