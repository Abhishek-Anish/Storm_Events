Please note that the files are long due to the inclusion of detailed outputs for each record along with its corresponding predictions, ensuring thorough documentation and analysis traceability.

==============================================================================================================================

CLIMATIC IMPACT AND WFO EFFIECIENCY ON USA STORM DYNAMICS - 2023


This project focuses on analyzing storm event data within a Databricks environment. 
The provided materials include a IPYNB script for loading, visualizing, analyzing and predicting storm event data, 
accompanied by the necessary data file and an HTML version of the notebook for easy viewing.

The zip file includes the following files:
1. READ ME file named as "READ_ME"

2. Workingsystem.ipynb: ipynb file containing the script for the analysis.

3. Workingsystem.html: HTML export of the .ipynb file for viewing in a web browser.

4. StormEvents_details-ftp_v1.0_d2023_c20240317.zip: StormEvents_details-ftp_v1.0_d2023_c20240317.csv named CSV file of the dataset is inside this zipped file.


PREREQUISITES:
Access to a Databricks workspace.

USAGE: 
-Open the databricks workspace and log into your databricks account

-Databricks Setup: Create a new or ensure you have a running Databricks cluster with the databricks runtime version set to 14.3 LTS ML (Scala 2.12, Spark 3.5.0) 

-Data File Upload: Download the dataset from the zipped folder named "StormEvents_details-ftp_v1.0_d2023_c20240317.zip". Upload the StormEvents_details-ftp_v1.0_d2023_c20240317.csv file to your Databricks FileStore.
 The steps inlcude creating a table, setting inferSchema to true and checking first row as headers.  

-Once the table is created, Import the notebook by creating a new notebook and then File > Import Notebook and upload the 'Workingsystem.ipynb' notebook to your workspace

-Ensure that the notebook is attached to a running Databricks cluster (14.3 LTS ML) 

-Run the notebook and execute cell by cell to do the analysis. 

- Ensure that the code syntax (which is available in the notebook) to create the "storm_data" dataframe is the one given below: 

 storm_data = spark.read.format("csv").option("header", "true").load("dbfs:/FileStore/tables/StormEvents_details_ftp_v1_0_d2023_c20240317.csv", inferSchema=True)

- Command 47 (cross validation) will take around 25 minutes to run. 
