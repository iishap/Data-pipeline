# OLake + Apache Iceberg Data Pipeline Task

## Task Overview

The objective was to:
- Set up a local PostgreSQL database
- Create a sample table and load it with sample data
- Use OLake's `discover` and `sync` commands to move data to Apache Iceberg (via Rest Catalog)
- Query synced data using Apache Spark SQL

---

## Setup Steps

### 1. PostgreSQL Setup
- Used Docker to spin up PostgreSQL instance.
- Created a sample table named `orders` and inserted 20 dummy records.

### 2. OLake Configuration
- Followed OLake documentation to configure source and destination JSON files.
- Ran `discover` to fetch schema and `sync` to migrate data to Iceberg.

### 3. Apache Iceberg & Spark
- Set up Apache Spark locally.
- Used Spark SQL CLI to connect to the Rest Catalog and run queries on the synced data.

---

## -> Video Walkthrough  
[Click here to watch the video](https://drive.google.com/file/d/1k-5jsTnIyWNpy31-kgMnNWgV_yyK_4Cs/view?usp=sharing)

---

## Screenshots

1. Sample `orders` table in PostgreSQL  
   ![orders-table](https://drive.google.com/uc?export=view&id=1xFEuIP5jUAe04CWFoE98VDX_es9DISsV)

2. OLake Discover and Sync Commands Output  
   ![olake-output](https://drive.google.com/uc?export=view&id=1d7aCYIKpROXedJ33r_foFa828K1y6Nn2)

3. Spark SQL Query Output  
   ![spark-sql](https://drive.google.com/uc?export=view&id=1MHoh-IioZi4VLpbHF0GC9M2iFTNR4xSF)


---

## ⚠️ Challenges Faced

- The **documentation for connecting Apache Iceberg via OLake’s Rest Catalog** was **not very clear**. There were several configuration nuances that weren’t explicitly mentioned.
- Faced issues in getting Spark to recognize Iceberg tables initially resolved by cross-referencing with Iceberg and Spark docs.

---

## Suggestions for Improvement

- **Enhance OLake’s documentation** for Iceberg integration with a dedicated section, full examples, and troubleshooting tips.
- Adding a sample project repo or video guide would reduce onboarding friction for new users.

---

## ✅ Conclusion

Despite initial challenges, the task was successfully completed. All steps from schema discovery to Iceberg querying were implemented and demonstrated in the attached video.

