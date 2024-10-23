# Secure and Scalable ETL Pipeline on Google Cloud Platform

## Executive Summary
This project demonstrates the creation of a secure and scalable ETL pipeline capable of handling sensitive employee data using Google Cloud Platform tools such as Cloud Data Fusion, Airflow, BigQuery, and Cloud Storage. The pipeline automates data extraction, transformation, and loading while ensuring data security through techniques such as data masking.

## Project Objectives:
- **Build a scalable ETL pipeline** using GCP’s Cloud Data Fusion and Airflow.
- **Ensure data security** by implementing robust data masking techniques.
- **Optimize resource usage** to minimize costs on GCP.
- **Visualize transformed data** using Data Studio.

## Technology Stack:
- **Google Cloud Platform**: Cloud Data Fusion, Airflow (Cloud Composer), BigQuery, Cloud Storage
- **Python**: For custom data manipulation and scripting.
- **Data Studio**: For data visualization and reporting.

## Project Implementation:
### Step-by-Step Walkthrough:
1. **Data Extraction and Ingestion**:
   - **Dataset**: Synthetic employee data (generated using the Faker library) uploaded to Cloud Storage.
   - **Storage**: Data stored in the Google Cloud Storage bucket `my-etl-data-bucket`.
   
2. **Data Transformation**:
   - **Pipeline Creation**: Built in Cloud Data Fusion (`datafusion-dev` instance).
   - **Data Masking**: Applied built-in functions to mask sensitive fields like SSN and salary.
   - **Transformed Data Storage**: Transformed data stored in BigQuery's `employee_data.transformed_employee_data` table.
   
3. **Data Loading**:
   - **BigQuery Integration**: The transformed data is loaded into BigQuery for further analysis.
   
4. **Data Visualization**:
   - **Dashboard**: Built in Data Studio, connected to the `transformed_employee_data` table in BigQuery, visualizing various aspects of the data.
   
5. **Pipeline Orchestration**:
   - **Airflow Configuration**: Managed via Cloud Composer to schedule the ETL pipeline with defined tasks and dependencies.

## Challenges and Solutions:
- **Data Schema Mismatches**: Resolved during the transformation phase in Cloud Data Fusion.
- **Pipeline Optimization**: Adjusted pipeline settings to improve efficiency and reduce execution times.
- **Permission Management**: Configured IAM roles (BigQuery Data Editor, Cloud Composer Worker) for secure access control.

## Results:
The ETL pipeline was successfully implemented, securely handling employee data, optimizing cloud resources, and visualizing the processed data using Google Data Studio.

# Data Visualization:
Explore the visualized data on the secure ETL pipeline via the following Data Studio dashboard:
- [Data Studio Dashboard Link](...)

## Future Improvements:
- Expand the pipeline to handle real-time streaming data.
- Integrate additional GCP services like Pub/Sub for real-time event processing.

## Tools Used:
- **Cloud Data Fusion**: ETL pipeline design and orchestration.
- **BigQuery**: Data warehousing and querying.
- **Cloud Composer**: Orchestrating the ETL workflow with Airflow.
- **Data Studio**: Visualization of transformed data.

## Acknowledgments:
- **Data Source**: Synthetic employee dataset generated using Python's Faker library.
