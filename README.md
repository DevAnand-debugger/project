## Operations on Dataset using Python (Pandas)

**Name:** Dev Anand
**Title:** Operations on Dataset in Python

---

# 📌 Introduction

In modern computing, large amounts of information are stored in **datasets**. A dataset is a structured collection of data that can be analyzed, modified, and processed to extract useful insights.

Python provides powerful libraries for handling datasets. One of the most widely used libraries is **Pandas**.

Pandas helps in:

* Data loading
* Data cleaning
* Data manipulation
* Statistical analysis
* Data exploration

Datasets are commonly stored in formats such as:

* CSV (Comma Separated Values)
* Excel
* SQL Databases
* JSON

---

# 🔹 What is Pandas?

**Pandas** is a Python library used for **data analysis and data manipulation**.

It provides two main data structures:

### 1️⃣ Series

A one-dimensional labeled array.

Example:

```
Roll Numbers of students
```

### 2️⃣ DataFrame

A **two-dimensional table** consisting of rows and columns.

Example:

| Roll No | Gender | Department | CGPA |
| ------- | ------ | ---------- | ---- |
| 101     | Female | Computer   | 8.2  |

DataFrames are the most commonly used structure in data science.

---

# 🔹 Dataset Creation

A dataset can be created using a **Python dictionary** and then converted into a DataFrame.

Example dataset contains:

* Roll Number
* Gender
* Department
* CGPA

### Steps:

1. Import Pandas
2. Create dictionary
3. Convert dictionary to DataFrame

```
import pandas as pd

data = {
"Roll_No":[101,102,103,104,105],
"Gender":["Female","Male","Female","Male","Female"],
"Department":["Computer","IT","ENTC","Mechanical","Computer"],
"CGPA":[8.2,7.5,9.1,6.8,8.7]
}


df = pd.DataFrame(data)
```

This creates a table-like dataset.

---

# 🔹 Saving Dataset to CSV File

Datasets are often stored as **CSV files**.

```
df.to_csv("students.csv",index=False)
```

Explanation:

* `to_csv()` saves DataFrame to file
* `index=False` removes the extra index column

---

# 🔹 Adding a New Column

A new column can be added easily.

```
df["year"]=["First","Second","First","Second","First"]
```

This adds the **year of study** for each student.

---

# 🔹 Dataset Dimensions

### Shape

```
df.shape
```

Returns:

```
(rows , columns)
```

Example:

```
(5 , 5)
```

---

### Size

```
df.size
```

Total number of elements in dataset.

Formula:

```
rows × columns
```

---

# 🔹 Dataset Information

### Info

```
df.info()
```

Provides:

* Column names
* Data types
* Non-null values
* Memory usage

---

# 🔹 Statistical Summary

```
df.describe()
```

Provides statistics such as:

* Mean
* Standard deviation
* Minimum value
* Maximum value
* Quartiles

---

# 🔹 Accessing Data from Dataset

### Access a Column

```
df["Department"]
```

Returns all values of department column.

---

### Access a Specific Row

```
df.loc[2]
```

Returns information of **row index 2** (PRN 103).

---

# 🔹 Data Types of Columns

```
df.dtypes
```

Shows the datatype of each column such as:

* Integer
* Float
* Object (string)

---

# 🔹 Statistical Operations

Statistical operations help analyze numeric data.

---

## Mean (Average)

```
df["CGPA"].mean()
```

Mean = Sum of values / Number of values

Used for academic performance analysis.

---

## Median

```
df["Roll_No"].median()
```

Median = Middle value in sorted dataset.

Useful when dataset contains outliers.

---

## Mode

```
df["CGPA"].mode()
```

Mode = Most frequent value in dataset.

---

# 🔹 Adding Grade Column

```
df["Grade"]=["A","B","A","C","D"]
```

This adds a grade for each student based on performance.

---

# 🔹 Removing a Column

```
df.drop("Gender",axis=1,inplace=True)
```

Explanation:

* `axis=1` refers to column
* `inplace=True` updates dataset permanently

---

# 🔹 Finding Maximum CGPA

```
df["CGPA"].max()
```

Used to identify **top performing student**.

---

# 🔹 Querying Specific Data

Example: CGPA of PRN 105

```
df[df["Roll_No"]==105]["CGPA"]
```

Explanation:

* Condition filters row
* Then CGPA column is selected

---

# 🔹 Loading External Dataset

Datasets can also be loaded from CSV files.

Example:

```
df=pd.read_csv("/content/Cars93.csv")
```

This loads the dataset into a DataFrame.

---

# 🔹 Viewing Dataset

### First 5 rows

```
df.head()
```

### Last 5 rows

```
df.tail()
```

These functions help quickly inspect data.

---

# 🔹 Dataset Properties

### Shape

Shows number of rows and columns.

### Size

Total number of elements.

### Data Types

Shows datatype of each column.

### Info

Provides structural information.

---

# 🎯 Learning Outcomes

After completing this experiment, students learn:

* How to create datasets
* How to load datasets
* DataFrame manipulation
* Data exploration techniques
* Statistical analysis
* Column operations
* Data filtering

These concepts are fundamental in:

* Data Science
* Machine Learning
* Artificial Intelligence
* Business Analytics

---

# 📚 Applications of Dataset Operations

Dataset operations are widely used in:

* Student result analysis
* Banking data analysis
* Business intelligence
* Healthcare records
* Stock market analysis
* Scientific research
* Machine learning models

---

# ✅ Conclusion

Datasets are the **foundation of modern data analysis**.

Using Pandas, datasets can be:

* Created
* Modified
* Analyzed
* Filtered
* Visualized

This experiment demonstrates how Python simplifies **data handling and statistical analysis**, which is essential for modern computing fields.

---

## ✍ Author

**Dev Anand**
B.Tech ENTC – Symbiosis Institute of Technology, Pune

---

