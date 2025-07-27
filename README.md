# 🚖 NYC Yellow Taxi Data Analytics with PySpark

This project focuses on performing big data analysis on real-world taxi trip data from New York City using PySpark. The objective is to preprocess, transform, and analyze this data to extract actionable insights through a series of PySpark DataFrame operations.

---

## 📁 Dataset Details

* **Source:** NYC Taxi & Limousine Commission
* **File Used:** `yellow_tripdata_2020-01.csv`
* **Size:** \~295 MB
* **Description:** The dataset includes trip-level details like fare amounts, surcharges, tip amounts, pickup/dropoff locations, payment types, and vendor information.

---

## 🧰 Technologies & Tools Used

* Python
* Apache Spark (PySpark)
* Jupyter Notebook
* Parquet Format (for optimized storage and query performance)

---

## 🔄 Data Processing Pipeline

1. **Data Ingestion**

   * Loaded the CSV file into a Spark DataFrame.
2. **Data Cleaning**

   * Converted string-based timestamps to proper `timestamp` types.
   * Casted numerical fields like fare, tip, distance, etc., to appropriate types.
   * Removed or handled any invalid/missing values.
3. **Data Transformation**

   * Calculated new metrics like revenue and earnings.
   * Simulated streaming behavior for time-based queries.
   * Grouped, aggregated, and sorted data for various use cases.
4. **Parquet Conversion**

   * Saved the cleaned dataset as a Parquet file to enable efficient access for future querying.

---

## 🔍 Analytical Tasks Performed

| Query  | Description                                                                                                  |
| ------ | ------------------------------------------------------------------------------------------------------------ |
| **Q1** | Added a new column `Revenue` as the sum of fare, tips, taxes, tolls, and surcharges.                         |
| **Q2** | Aggregated total passengers grouped by pickup location zones.                                                |
| **Q3** | Computed average fare and total income grouped by vendor ID.                                                 |
| **Q4** | Calculated a moving (rolling) count of transactions per payment type.                                        |
| **Q5** | Identified top 2 vendors with highest earnings on a specific date, along with total distance and passengers. |
| **Q6** | Found the most frequently traveled route (pickup to drop-off) based on passenger volume.                     |
| **Q7** | Fetched top pickup zones with maximum passenger count in the last simulated 5–10 seconds window.             |

---

## 📝 How to Run

1. Install required libraries:

   ```bash
   pip install pyspark
   ```

2. Clone the repository and open the Jupyter notebook:

   ```bash
   git clone <your-repo-link>
   cd <repo-folder>
   jupyter notebook
   ```

3. Run each cell step-by-step in the notebook. Update file paths if needed.

---

## ✅ Outcomes

* Efficiently processed real-world NYC Taxi data using distributed computing with Spark.
* Extracted business-relevant insights from large-scale trip data.
* Demonstrated ability to perform batch and near-real-time analytics using PySpark.
* Output stored as a Parquet file for fast and optimized querying.

---

## 📌 Future Enhancements

* Integrate with Databricks for cloud-based execution.
* Extend streaming simulations using Spark Structured Streaming.
* Build interactive dashboards on top of analytical results using tools like Plotly or Tableau.

---

