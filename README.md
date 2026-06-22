# Sales_Analysis_python_libraries

## 📌 Project Introduction

This project presents an end-to-end sales data analysis workflow using Python and Pandas. The dataset contains transactional sales records including product information, revenue, payment methods, sales locations, managers, and transaction dates.

The objective of this project is to transform raw sales data into actionable business insights through data cleaning, exploratory data analysis (EDA), statistical analysis, and visualization techniques. By leveraging Python's data analysis capabilities, the project identifies sales patterns, evaluates product performance, analyzes customer payment preferences, and uncovers revenue trends across different dimensions of the business.

Key areas covered in this project include:

* Data Cleaning & Preprocessing
* Revenue Analysis
* Product Performance Analysis
* Payment Method Analysis
* Statistical Analysis
* Sales Trend Analysis
* Exploratory Data Analysis (EDA)
* Business Insight Generation
* Data Visualization

This project demonstrates practical data analytics skills commonly used by Data Analysts to support business decision-making and performance evaluation.


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

This project demonstrates the application of Python and Pandas in solving real-world business analytics problems using sales transaction data. Through data cleaning, aggregation, statistical analysis, and visualization, meaningful insights were extracted to evaluate sales performance, identify high-performing products, understand customer behavior, and monitor revenue trends.

Key outcomes of the project include:

✔️ Identification of top-performing products and revenue contributors

✔️ Analysis of customer payment preferences

✔️ Evaluation of city-wise and manager-wise sales performance

✔️ Discovery of revenue trends and seasonal patterns

✔️ Application of statistical techniques to understand data variability

✔️ Creation of visualizations to support business decision-making

Through this project, practical experience was gained in data preparation, exploratory data analysis, statistical analysis, and business reporting using Python and Pandas. The project serves as a strong demonstration of foundational data analytics skills applicable to real-world business environments.


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
