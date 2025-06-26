<img width="1321" alt="image" src="https://github.com/user-attachments/assets/56c0a5be-1c1b-482a-bbfe-21884b4913b4" />


## Project Overview

This project contains two PySpark-based notebooks demonstrating scalable data transformation and feature engineering in real-world scenarios.  
The first notebook explores financial time series using Spark SQL and DataFrame APIs.  
The second performs distributed feature engineering on a clinical dataset retrieved from PostgreSQL, including missing value analysis and imputation using Spark ML.

## Objectives

- Apply PySpark DataFrame and SQL operations for time series exploration  
- Analyze, clean, and impute missing values from a clinical dataset using distributed computing  
- Leverage Spark ML for statistical preprocessing  
- Integrate data from PostgreSQL using JDBC  
- Demonstrate best practices for working with large-scale or streaming-ready data sources  

## Tools and Technologies

- PySpark (Spark SQL, Spark ML)  
- PostgreSQL (via JDBC)  
- pandas (for comparison/reference)  
- Python 3.x  
- Apache Spark 3.x

## Project Structure

feature-engineering-and-spark-dataframe-operations/  
├── spark_dataframe_operations_appl_stock.ipynb        – Apple stock data exploration using Spark SQL and DataFrame API  
├── feature_engineering_diabetes_dataset.ipynb         – Feature engineering and imputation on clinical data using PySpark and PostgreSQL  
├── README.md                                          – Project documentation  

## Notebook 1: Apple Stock Dataframe Operations

**Title**: Exploratory Data Analysis and SQL Queries with PySpark  
**Description**:  
- Reads Apple stock price data into Spark DataFrame  
- Demonstrates:
  - Column operations, filtering, sorting  
  - New feature creation  
  - Comparisons using both SQL and DataFrame APIs  
- Focus: PySpark syntax fluency, performance benchmarking

<img width="1296" alt="image" src="https://github.com/user-attachments/assets/9cc3587a-6b91-44f9-9bb5-5f3a4225c82d" />

## Notebook 2: Diabetes Dataset Feature Engineering

**Title**: Feature Engineering on Clinical Data Using PySpark and PostgreSQL  
**Description**:  
- Loads a diabetes dataset from a PostgreSQL database using Spark JDBC  
- Performs:
  - Null count analysis  
  - Threshold-based row dropping  
  - Median imputation using `pyspark.ml.feature.Imputer`  
  - Min/Max range analysis using Spark aggregation  
- Focus: Scalable preprocessing and integration with relational sources

## How to Run

1. Ensure Apache Spark and PySpark are installed and properly configured  
2. PostgreSQL must be running with the database and table accessible  
3. Update connection details in the `load_data_from_postgres()` function  
4. Launch notebooks via Jupyter or a Spark-compatible notebook environment  

To install dependencies:
pip install pyspark pandas

To run Spark locally (example):
Ensure Java 8+ and Spark are installed, then:
export PYSPARK_PYTHON=python3  
pyspark --master local[*]

## Requirements

- PySpark  
- pandas  
- PostgreSQL (for JDBC source)  
- Java (for running Spark)  
- JDBC driver: postgresql-42.7.1.jar

## License

This project is licensed under the MIT License. See the LICENSE file for details.
