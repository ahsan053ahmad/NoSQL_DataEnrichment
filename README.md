
#  NoSQL_DataEnrichment – MongoDB, JSON Processing, and Data Cleaning in Python

This repository contains the submission for Lab 7 of the Data Engineering course, focused on working with **NoSQL databases**, **JSON enrichment**, and **data cleaning techniques**. The assignment leverages MongoDB for data storage and querying, while Python (with `pandas` and `json`) is used for extracting, transforming, and enriching the dataset.

---

###  Business Problem

In modern data environments, especially when dealing with semi-structured or external data sources, JSON is a common format. The task was to load JSON data, validate and clean it, and then enrich it using multiple lookup strategies—eventually storing and retrieving the results in/from MongoDB.

---

###  Project Objectives

- Load external JSON datasets into Python using `json` and `pandas`
- Perform nested structure extraction and flattening
- Identify and handle missing or corrupted records
- Enrich base records using auxiliary data files (e.g., mapping files for resolution)
- Insert cleaned and enriched records into MongoDB collections
- Run MongoDB queries to validate inserts and retrieve summaries

---

### Solution Approach

1. **JSON File Processing**
   - Loaded a sample nested JSON file representing base records
   - Flattened and normalized nested attributes into tabular format using `json_normalize`

2. **Data Cleaning**
   - Dropped records with missing or null values in critical fields
   - Removed duplicates and inconsistent entries

3. **Data Enrichment**
   - Used mapping files (e.g., `job_map.json`) to enhance base records
   - Merged mappings with original records using `pandas.merge` based on key fields

4. **MongoDB Integration**
   - Connected to a local MongoDB instance using `pymongo`
   - Inserted enriched records into collections
   - Queried MongoDB using basic aggregation and match filters to validate results

---

### Business Value

- **Data Quality Assurance**: Cleaning routines enhance data reliability for downstream tasks
- **NoSQL Proficiency**: Demonstrates real-world application of MongoDB for semi-structured data
- **Scalable Data Handling**: Efficient parsing and transformation of JSON prepares data for analytics pipelines
- **Reusability**: The code can be adapted for future ETL/ELT jobs involving JSON APIs or log streams

---

### Challenges Encountered

- JSON records contained variable structures and inconsistent nesting
- MongoDB schema design required careful mapping to flattened data
- Edge cases in merging enrichment files (e.g., missing keys) had to be handled gracefully

---


