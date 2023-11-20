# Time Series Data Standardization

This project focuses on harmonizing time series data collected from various sensors with differing sampling rates and temporal discretization. Specifically, it showcases the process using datasets from the PDI13215 (pressure sensor) and FI12110 (flow sensor), spanning observations over several months. The project serves as an exemplary model of the approach's adaptability, extending its use to harmonize and standardize datasets from diverse sensors.

## Tasks

### 1. Adaptive Temporal Data Transformation

- **Normalize Data Structure:**
  - Transform disparate raw data into a standardized format: Timestamp, PDI13215 Sensor Value, FI12110 Sensor Value.
  - Address discrepancies in timestamps and missing values via interpolation, ensuring a consistent N-minute interval (e.g., 10-minute intervals: 9:00, 9:10, 9:20, etc.). Data points more frequent than the interval will be filtered out.

### 2. Data Cleaning and Export

- **Data Cleansing:**
  - Remove rows containing empty or NULL values.

- **Export Format:**
  - Save the processed data into a .csv file encoded in UTF-8, using a comma (,) as a delimiter.
  - Timestamp format: YYYY-MM-DD HH:MI:SS
  - Format the output file similar to the provided template, establishing a foundation for subsequent machine learning training and analysis.

### Data Format Template

1. **Point Name:** PDI13215, FI12110
2. **Description:** Value for PDI13215, Value for FI12110
3. **Extended Name:**
4. **Extended Description:**
5. **Units:** PSI, M3/h
6. **TIMESTAMP:** PDI13215_SENSOR_VALUE, FI12110_SENSOR_VALUE

This project offers a model for handling challenges specific to PDI13215 and FI12110 data. It's designed to be easily adapted for addressing similar issues in data collected from various sensors.
