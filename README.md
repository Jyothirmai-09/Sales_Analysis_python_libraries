# Sales_Analysis_python_libraries

## 📌 Project Introduction

This project focuses on performing **Sales Data Analysis** using **Python and the Pandas library** within Jupyter Notebook. The dataset contains information related to products, sales quantities, revenue, payment methods, cities, managers, and transaction dates.

The primary objective of this project is to understand how Python and Pandas can be used for real-world business data analysis, including data cleaning, transformation, aggregation, statistical analysis, and extracting actionable business insights from structured sales datasets.

Various data analysis techniques were implemented throughout the project, including:

* Data Cleaning
* Removing Duplicate Records
* Revenue Analysis
* Product Performance Analysis
* Payment Method Analysis
* Statistical Analysis
* Date-Time Analysis
* Data Visualization
* Exploratory Data Analysis (EDA)

This project provides practical exposure to business analytics workflows and demonstrates how data analysts leverage Python to evaluate sales performance and support data-driven decision-making.

---

# 📂 Dataset Information

The dataset contains transactional sales records collected across multiple products, cities, and payment methods.

### Dataset Features

| Column Name    | Description         |
| -------------- | ------------------- |
| Product        | Product Name        |
| Quantity       | Quantity Sold       |
| Revenue        | Sales Revenue       |
| Payment_Method | Payment Method Used |
| City           | Sales Location      |
| Manager        | Sales Manager       |
| Date           | Transaction Date    |

Each record represents a unique sales transaction.

---

# 🛠️ Tools & Technologies Used

## 🐍 Python

Python was used as the primary programming language for:

* Data Analysis
* Data Cleaning
* Statistical Analysis
* Data Visualization

---

## 📊 Pandas

Pandas was used for:

* Data Manipulation
* Data Cleaning
* Revenue Analysis
* Statistical Analysis
* GroupBy Operations
* Filtering & Aggregation

---

## 📈 Matplotlib

Used for:

* Revenue Trend Visualization
* Product Analysis Charts
* Sales Performance Graphs

---

## 📓 Jupyter Notebook

Used for:

* Interactive Coding
* Data Exploration
* Visualization
* Analytical Reporting

---

# 🧹 Data Cleaning & Preprocessing

Several preprocessing techniques were performed before analysis.

### Checking Dataset Information

```python
data.info()
```

### Removing Extra Spaces

```python
data['Product'] = data['Product'].str.strip().str.replace(r'\s+', ' ', regex=True)
```

### Identifying Duplicate Records

```python
data.duplicated()
```

### Removing Duplicate Records

```python
data.drop_duplicates(inplace=True)
```

### Date Conversion

```python
data['Date'] = pd.to_datetime(data['Date'])
```

### Creating Month Column

```python
data['Month'] = data['Date'].dt.month
```

---

# 📚 Pandas Functions Used

## Data Exploration

```python
info()
head()
loc[]
reset_index()
```

## Data Cleaning

```python
duplicated()
drop_duplicates()
str.strip()
str.replace()
```

## Data Analysis

```python
groupby()
mean()
std()
var()
agg()
value_counts()
```

## Date-Time Analysis

```python
pd.to_datetime()
dt.month
```

## Visualization

```python
plot(kind='bar')
plot()
```

---

# 📊 Business Questions Solved

## 1️⃣ Preferred Payment Method Analysis

### Objective

Identify the most commonly used payment method.

### Code

```python
data['Payment_Method'].value_counts()
```

### Insight

Determined customer payment preferences and most frequently used payment options.

---

## 2️⃣ Most Selling Product Analysis

### Objective

Find the best-selling products based on quantity and revenue.

### Code

```python
data.groupby('Product')['Quantity'].sum()

data.groupby('Product')['Revenue'].sum()
```

### Insight

Identified products contributing the highest sales volume and revenue.

---

## 3️⃣ City & Manager Revenue Analysis

### Objective

Determine which cities and managers generated the highest revenue.

### Code

```python
data.groupby('City')['Revenue'].sum().sort_values(ascending=False)

data.groupby('Manager')['Revenue'].sum().sort_values(ascending=False)
```

### Insight

Highlighted top-performing locations and sales managers.

---

## 4️⃣ Date-wise Revenue Analysis

### Objective

Analyze daily revenue performance.

### Code

```python
data.groupby('Date')['Revenue'].sum()
```

### Insight

Provided visibility into daily sales trends and revenue fluctuations.

---

## 5️⃣ Average Revenue Analysis

### Objective

Calculate overall average revenue.

### Code

```python
data['Revenue'].mean()
```

### Insight

Helped evaluate overall business performance.

---

## 6️⃣ November & December Revenue Analysis

### Objective

Analyze seasonal revenue performance.

### Code

```python
data.groupby('Month')['Revenue'].mean()
```

### Insight

Compared monthly revenue and identified seasonal sales patterns.

---

## 7️⃣ Standard Deviation Analysis

### Objective

Measure variability in revenue and quantity sold.

### Code

```python
data['Revenue'].std()

data['Quantity'].std()
```

### Insight

Provided an understanding of data spread and consistency.

---

## 8️⃣ Variance Analysis

### Objective

Measure sales fluctuations.

### Code

```python
data['Revenue'].var()

data['Quantity'].var()
```

### Insight

Helped understand the degree of variation within sales data.

---

## 9️⃣ Revenue Trend Analysis

### Objective

Analyze whether revenue increased or decreased over time.

### Code

```python
data.groupby('Date')['Revenue'].sum().plot()
```

### Insight

Visualized sales growth trends and business performance over time.

---

## 🔟 Product-wise Average Analysis

### Objective

Calculate average quantity sold and average revenue per product.

### Code

```python
data.groupby('Product')[['Quantity','Revenue']].agg({
    'Quantity':'mean',
    'Revenue':'mean'
})
```

### Insight

Provided deeper understanding of product-level sales performance.

---

# 📈 Visualizations Created

### 📊 Bar Chart

* Product-wise Sales Analysis
* Payment Method Analysis

### 📈 Line Chart

* Revenue Trend Analysis

### 📉 Comparative Analysis

* City Revenue Performance
* Manager Revenue Performance

---

# 🔑 Key Insights

✔️ Pandas simplifies large-scale sales data analysis.

✔️ GroupBy operations help uncover product and revenue trends.

✔️ Statistical analysis provides deeper understanding of business performance.

✔️ Date-Time analysis helps identify monthly and seasonal trends.

✔️ Revenue visualization helps track business growth patterns.

✔️ Data-driven insights can support better business decisions.

---

# 📁 Project Structure

```text
Sales-Data-Analysis/
│
├── Sales_Data_Analysis.ipynb
├── Sales_Data.csv
├── README.md
```

---

# 🎯 Skills Demonstrated

### Data Analysis

* Data Cleaning
* Data Wrangling
* Exploratory Data Analysis (EDA)

### Python Libraries

* Pandas
* Matplotlib

### Business Analytics

* Revenue Analysis
* Product Performance Analysis
* Statistical Analysis
* Trend Analysis

### Visualization

* Bar Charts
* Line Charts
* Sales Trend Analysis

---

# 🏁 Conclusion

This project demonstrates how Python and Pandas can be effectively used for real-world sales data analysis. Through data cleaning, duplicate removal, statistical analysis, grouping operations, date-time analysis, and visualization, meaningful business insights were successfully extracted from sales transaction data.

The project strengthened practical skills in:

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Data Manipulation using Pandas
* Statistical Analysis
* Revenue Analysis
* Business Insight Generation
* Data Visualization
* Python-based Analytics

Overall, this project serves as a strong foundation for learning Data Analysis and Business Intelligence using Python.

---

## 👩‍💻 Author

**Jyothirmai Seepana**

### Aspiring Data Analyst

**Skills:**

* SQL
* Excel
* Power BI
* Python
* Data Visualization
* Business Intelligence
