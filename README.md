# milestone2_project

## Netflix Movies and TV Shows Data Analysis using PySpark

### 1. Dataset Description

This project analyzes the Netflix Movies and TV Shows dataset using PySpark.

The dataset contains information about Netflix movies and TV shows, including:
- Show ID
- Type
- Title
- Director
- Cast
- Country
- Date Added
- Release Year
- Rating
- Duration
- Genre
- Description

Dataset source:
https://www.kaggle.com/datasets/shivamb/netflix-shows

### 2. Project Steps

The following steps were performed:

1. Loaded the Netflix CSV dataset using PySpark.
2. Checked the schema and structure of the DataFrame.
3. Renamed columns where required.
4. Added a Data_Source column.
5. Converted and cleaned required columns.
6. Created a Content_Age column to classify content as New or Old.
7. Filtered movies and TV shows for analysis.
8. Identified and handled null values.
9. Checked for duplicate records.
10. Saved the processed DataFrame in Parquet format.
11. Performed analysis using grouping and counting.
12. Analyzed Netflix content by genre and country.

### 3. Data Loading

The dataset was loaded using PySpark CSV reader with:
- Header enabled
- Schema inference enabled
- Multi-line records enabled
- Escape characters handled
- PERMISSIVE mode used to handle malformed records

### 4. Data Cleaning and Transformation

The following transformations were performed:

- Renamed `listed_in` to `genre`.
- Renamed `date_added` to `added_date`.
- Converted appropriate columns to suitable data types.
- Added `Data_Source` with the value `Netflix`.
- Created `Content_Age` based on release year.
- Filtered movies and TV shows where required.
- Handled missing values using meaningful values such as `Unknown` where appropriate.

### 5. Null Value Handling

Null values were identified using PySpark.

For columns where missing values could be replaced meaningfully, values such as `Unknown` were used.

Rows with invalid or unusable information were removed where appropriate.

### 6. Duplicate Removal

Duplicate records were checked and removed where required to improve data quality.

### 7. Data Analysis

The processed Netflix dataset was analyzed using PySpark.

Examples of analysis performed:

- Count of content by genre
- Count of content by country
- Movie and TV show analysis
- Content release year analysis
- Other grouped analysis using PySpark

### 8. Output

The processed DataFrame was written in Parquet format for efficient storage and further analysis.

### 9. Screenshots

Screenshots of important outputs are included in the `screenshots` folder.

They include:
- Dataset schema
- Data loading
- Transformations
- Null value handling
- Analysis results
- Genre analysis
- Country analysis
- Other important outputs

### 10. Challenges and Solutions

Some challenges were encountered while processing the dataset, including:

- Invalid data types in some columns
- Missing values
- Multi-line records in the CSV file
- Date parsing issues
- Storage path and volume issues

These were resolved by using appropriate PySpark functions, data cleaning techniques, permissive CSV reading, and suitable Databricks volume paths.

### 11. Technologies Used

- Python
- PySpark
- Apache Spark
- Databricks
- GitHub
- Parquet
