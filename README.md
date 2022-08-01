# BUDA_555
Capstone Project


1.  ES_Download.ipynb
This file is configured to connect to the elastic pods within Kubernetes. Currently, it's set up to process historical indexes, but once logstash is generating daily logs, you will be able to run the file to pull the yesterday's date.

2. ETL_Functions.ipynb
The core functions developed to convert the JSON files, assign labels to the log classifications, and generate the bar chart and word clouds.

3. ETL_Runner.ipynb 
The primary script for processing the output of ES_Download. This runner references the functions created in file #2. Iterates over ever file found in the root directory, and then saves the processed files to a dated folder path within /analyzed and /images

# TO DO

Create function to archive files that live in the root directory, once they have been processed.

Create call from ES_Download to ETL_Runner, so that the files can be processed once they are pulled from elastic.

Create process to write data to database, so Tableau can read in up to date data.
