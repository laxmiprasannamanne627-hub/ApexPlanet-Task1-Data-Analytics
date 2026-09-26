# ApexPlanet Data Analytics Internship – Task 1

## Data Cleaning and Preparation

This project was completed as part of the **ApexPlanet Data Analytics Internship**.

The objective of this task was to understand the given sales dataset, identify data quality issues, perform data cleaning and transformation using Python and Pandas, and prepare a final dataset suitable for analysis.

---

## 📌 Project Overview

Data cleaning is an important step in the data analytics process because the quality of the data directly affects the accuracy of analysis and business insights.

In this project, the provided sales dataset was examined for:

* Missing values
* Duplicate records
* Inconsistent text formatting
* Invalid numeric values
* Date formatting issues
* Potential outliers
* Sales calculation consistency

The cleaned dataset was then exported as an analysis-ready Excel file.

---

## 🎯 Objectives

The main objectives of this task were to:

1. Understand the structure of the dataset.
2. Create a data dictionary describing each variable.
3. Identify missing values and duplicates.
4. Check data consistency and validity.
5. Standardize date and text formats.
6. Handle missing values appropriately.
7. Identify potential outliers using the IQR method.
8. Validate the `Total_Sales` values.
9. Prepare and export the final analysis-ready dataset.

---

## 📊 Dataset

The dataset contains sales transaction information with:

* **1,000 rows**
* **12 columns**

### Dataset Columns

| Column          | Description                      |
| --------------- | -------------------------------- |
| `Order_ID`      | Unique identifier for an order   |
| `Order_Date`    | Date when the order was placed   |
| `Customer_ID`   | Unique identifier for a customer |
| `Customer_Name` | Name of the customer             |
| `Age`           | Age of the customer              |
| `Gender`        | Gender of the customer           |
| `City`          | City of the customer             |
| `Product`       | Product purchased                |
| `Category`      | Category of the product          |
| `Quantity`      | Number of units purchased        |
| `Unit_Price`    | Price of one unit                |
| `Total_Sales`   | Total value of the transaction   |

---

## 🔍 Data Quality Issues Identified

During the initial data profiling, the following issues were identified:

### Missing Values

* `Age` contained **20 missing values**.
* `City` contained **13 missing values**.

### Date Formatting

* `Order_Date` was initially stored as a text/object field.
* It was converted into a proper datetime format for analysis.

### Text Formatting

Text-based columns were checked and standardized by removing unnecessary leading and trailing spaces.

### Duplicate Records

The dataset was checked for duplicate records.

### Numeric Validation

Numeric columns such as `Age`, `Quantity`, `Unit_Price`, and `Total_Sales` were checked for invalid values.

### Outlier Detection

Potential outliers were identified using the **Interquartile Range (IQR)** method.

Outliers were not automatically deleted because unusually large transactions can represent valid business transactions.

---

## 🧹 Data Cleaning Process

The following cleaning and transformation steps were performed:

### 1. Missing Age Values

Missing values in the `Age` column were replaced using the **median age** of the dataset.

### 2. Missing City Values

Missing values in the `City` column were replaced with:

`Unknown`

This preserves the records while clearly indicating that the city information was unavailable.

### 3. Date Conversion

The `Order_Date` column was converted into a proper datetime format using Pandas.

### 4. Text Standardization

The following text columns were standardized by removing unnecessary spaces:

* `Order_ID`
* `Customer_ID`
* `Customer_Name`
* `Gender`
* `City`
* `Product`
* `Category`

### 5. Duplicate Checking

Duplicate records were checked to ensure that the dataset did not contain unintended repeated records.

### 6. Numeric Validation

Numeric fields were checked for valid values and appropriate data types.

### 7. Sales Validation

The relationship between `Quantity`, `Unit_Price`, and `Total_Sales` was validated using:

```text
Calculated Sales = Quantity × Unit Price
```

The calculated values were compared with the original `Total_Sales` values.

### 8. Outlier Detection

The IQR method was used to identify potential outliers in:

* `Age`
* `Quantity`
* `Unit_Price`
* `Total_Sales`

Potential outliers were retained because they may represent legitimate transactions.

---

## 📖 Data Dictionary

A separate data dictionary has been created containing:

* Column name
* Data type
* Meaning of the variable
* Business relevance

This helps users understand how each field can be used for future analysis.

---

## 📁 Files in This Repository

### 1. Data Cleaning Notebook

`ApexPlanet_Task1_Data_Cleaning.ipynb`

Contains the complete Python/Pandas workflow used for:

* Data loading
* Data profiling
* Missing-value analysis
* Duplicate checking
* Data validation
* Data cleaning
* Outlier detection
* Final validation
* Dataset export

### 2. Cleaned Dataset

`ApexPlanet_Task1_Cleaned_Dataset.xlsx`

The final cleaned and analysis-ready dataset.

### 3. Data Dictionary

`ApexPlanet_Task1_Data_Dictionary.xlsx`

Documents the meaning, data type, and business relevance of each dataset variable.

---

## 🛠️ Tools & Technologies

* **Python**
* **Pandas**
* **Google Colab**
* **Microsoft Excel**
* **GitHub**

---

## 📈 Final Result

The dataset was successfully cleaned and prepared for further data analysis.

The final dataset contains:

* **1,000 records**
* **12 original data columns**
* Missing values handled
* Dates standardized
* Text formatting standardized
* Duplicate and numeric validity checks completed
* Sales values validated
* Potential outliers identified
* Analysis-ready Excel file created

---

## 🚀 Future Scope

The cleaned dataset can be used for further analytics such as:

* Sales trend analysis
* Product performance analysis
* Category-wise sales analysis
* Customer analysis
* City-wise sales analysis
* Demographic analysis
* Dashboard development
* Business insights and reporting

---

## 👩‍💻 Author

**Laxmi Prasanna Manne**

B.Tech – Computer Science and Engineering (AI & ML)

Aspiring **Data Analyst**

---

## 📌 Internship

**ApexPlanet Data Analytics Internship**

**Task 1 – Data Cleaning and Preparation**
