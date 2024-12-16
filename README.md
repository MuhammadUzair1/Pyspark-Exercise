# PySpark Exercise and Sample Data Generator

## Overview

This repository contains work implemented in PySpark, focusing on solving data-intensive problems and optimizing computation to leverage the full power of your machine. The project includes:

1. A Python script (`data_generator.py`) to generate sample data containing **75 million rows** across multiple CSV files.
2. Solutions to Spark exercises, designed to maximize computational efficiency.
3. Instructions for running PySpark on Windows, including necessary prerequisites and environment setup.

---

## Features

### 1. **Data Generation**

The `data_generator.py` script generates sample CSV files containing 75 million rows. This data serves as a large dataset for testing and working with Spark applications.

#### Key Features:

- Generates large-scale, realistic datasets.
- Saves the data in CSV format for easy integration with Spark.
- Configurable row counts and schema design to customize test data.

---

### 2. **Spark Exercises**

The repository includes solutions to Spark exercises that demonstrate:

- Efficient data ingestion and transformations.
- Handling and processing large datasets with optimal resource utilization.
- Real-world scenarios that apply advanced PySpark techniques like window functions, aggregations, and joins.

#### Optimization Techniques Used:

- Partitioning and caching to manage memory effectively.
- Leveraging Spark's lazy evaluation to minimize unnecessary computations.
- Optimized filtering and column pruning to reduce data processing overhead.

---

## Prerequisites

To execute Spark on a Windows machine, ensure the following tools and configurations are in place:

### 1. **Java Installation**

- Install Java version **8** or higher.
- Define the `JAVA_HOME` path in your system's environment variables.

### 2. **Spark Installation**

- Download and install Apache Spark from the [official website](https://spark.apache.org/downloads.html).

### 3. **Winutils Setup**

- Download the `winutils.exe` file for your version of Hadoop.
- Place the `winutils.exe` file in a folder (e.g., `C:\hadoop\bin`).
- Add this folder to your system's `PATH` environment variable.

### 4. **Environment Variables**

Define the following variables in your system:

- `JAVA_HOME`: Path to the Java installation directory.
- `SPARK_HOME`: Path to the Spark installation directory.
- Add `%SPARK_HOME%\bin` to the `PATH` variable.

---

## Usage

### 1. **Generate Sample Data**

Run the `data_generator.py` script to generate large-scale CSV files:

```bash
python data_generator.py
```

The script will create CSV files in the specified output directory, containing a total of **75 million rows**.

### 2. **Run PySpark Application**

Use the PySpark shell or execute a Python script with Spark:

```bash
spark-submit your_script.py
```

Ensure that all required dependencies are installed and paths are configured before execution.

---

## Example Exercises and Solutions

This project includes solutions to the following Spark exercises:

1. **Data Cleaning and Transformation**

   - Handling missing values.
   - Optimizing schema to reduce memory footprint.

2. **Aggregations and Grouping**

   - Computing aggregates efficiently using `groupBy` and `agg` functions.
   - Leveraging window functions for advanced analytics.

3. **Joins and Filtering**

   - Efficiently joining large datasets.
   - Filtering data early in the pipeline to reduce unnecessary computation.

4. **Performance Optimization**
   - Partitioning large datasets to improve parallel processing.
   - Using `persist` and `cache` where appropriate.

---

## Performance Considerations

To maximize computation power and achieve optimal performance:

- Use **repartitioning** to balance the workload across available cores.
- Utilize **broadcast joins** for small lookup tables.
- Profile the Spark job using the UI to identify and resolve bottlenecks.
- Ensure sufficient memory and disk space for intermediate data.

---

## Troubleshooting

### Common Errors and Fixes:

1. **Java Not Found**

   - Ensure Java is installed and `JAVA_HOME` is correctly set in the environment variables.

2. **Winutils Missing**

   - Download the correct `winutils.exe` and place it in the specified folder (e.g., `C:\hadoop\bin`).

3. **Out of Memory Errors**

   - Increase the driver and executor memory using Spark configurations:
     ```bash
     --driver-memory 4G --executor-memory 8G
     ```

4. **Environment Variables Not Set**
   - Double-check the paths for `JAVA_HOME`, `SPARK_HOME`, and `HADOOP_HOME`.

---

## Conclusion

This project demonstrates the use of PySpark for processing and analyzing large-scale datasets efficiently. By leveraging optimized data generation, configuration, and processing techniques, it provides a comprehensive workflow for working with Spark on a Windows system.

---

## License

This project is licensed under the MIT License.
