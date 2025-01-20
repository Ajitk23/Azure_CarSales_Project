
![photo_2025-01-21_05-05-54](https://github.com/user-attachments/assets/df4b0635-c2d1-4437-a132-f3b2f6074a61)

# Azure_CarSales_Project
End-to-End Azure Project by using Unity Catalog
# **SalesCarsProject: A Complete Azure Data Engineering Solution**

## **Overview**
The **SalesCarsProject** demonstrates an end-to-end data pipeline solution using Azure services and Databricks, focusing on secure, scalable, and efficient data management. The project involves ingesting raw data, performing incremental loads, and transforming data into meaningful insights with a modern architecture.

---

## **Key Technologies Used**
1. **Azure Data Factory (ADF)**: For orchestrating workflows, including incremental data loading.
2. **Azure SQL Database**: For storing raw data and tracking incremental load progress.
3. **Azure Data Lake Storage Gen2**: Hierarchical storage for organizing data into Bronze, Silver, and Gold layers.
4. **Azure Databricks**: For data transformation, using Delta Lake for ACID transactions.
5. **Unity Catalog**: Secure, modern data access management, eliminating the need for traditional file mounting.
6. **Parquet File Format**: For efficient storage and querying.

---

## **Process Overview**
1. **Data Ingestion**:
   - Raw data was pulled from a source using ADF’s Copy Activity and stored in the `source_cars_data` table in Azure SQL Database.
   - A parameterized process enabled dynamic file selection.

2. **Incremental Loading**:
   - Implemented incremental data processing using water tables to track the last loaded date.
   - ADF’s Lookup, Copy Activity, and Stored Procedure Activities automated the process.

3. **Unity Catalog Integration**:
   - Used Unity Catalog in Azure Databricks for secure, role-based access to data, replacing traditional file mounting.
   - External tables were created to link the data lake with Databricks.

4. **Data Transformation**:
   - Databricks notebooks were created for data transformation:
     - Bronze layer: Raw data ingestion.
     - Silver layer: Data cleaning, enrichment, and feature creation.
   - Transformed data was stored in Parquet format in the Silver layer.

5. **Workflow Integration**:
   - Databricks notebooks were integrated into a unified workflow to automate transformations.
   - ADF Copy Activity tested incremental datasets for final validation.

---

## **Key Outcomes**
1. **Scalable Architecture**: Handled large datasets efficiently.
2. **Enhanced Security**: Unity Catalog enabled fine-grained access control.
3. **Efficient Data Processing**: Incremental loading reduced overhead.
4. **Optimized Storage**: Parquet and Delta Lake improved performance and cost-effectiveness.
5. **End-to-End Automation**: Seamless integration of ADF and Databricks workflows ensured reliability.

---

## **Conclusion**
The SalesCarsProject highlights the power of Azure and Databricks in building a robust and modern data engineering solution. By leveraging Unity Catalog, the project set a new standard for secure and scalable data management, serving as a valuable guide for aspiring data engineers.

---


