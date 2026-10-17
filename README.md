# 🛒 E-Commerce Sales Performance Analysis

## 📌 Project Overview

This project analyzes e-commerce sales data for a sample retail company, **SwiftCart Retail**. The objective is to understand product category performance, customer satisfaction, and product pricing using Python.

The analysis calculates total sales, identifies the highest-revenue product category, evaluates customer ratings, filters highly rated records, and visualizes sales and price distributions.

The project demonstrates practical data analysis and visualization techniques that can support data-driven inventory planning.

## 🎯 Objectives

- Calculate total sales using product price and quantity.
- Compare sales across product categories.
- Identify the category with the highest total sales.
- Calculate the average customer rating.
- Identify products or order records with ratings greater than 4.
- Visualize category-wise sales using a bar chart.
- Analyze product prices using a histogram.
- Understand how data analysis can support inventory optimization.

## 🛠️ Technologies Used

- **Python** — programming language
- **Pandas** — data manipulation and analysis
- **Matplotlib** — data visualization
- **Jupyter Notebook** — interactive development environment
- **Google Colab** — cloud-based notebook execution

## 📂 Project Structure

```text
ecommerce-sales-performance-analysis/
│
├── README.md
├── ecommerce_sales_analysis.ipynb
└── ecommerce_sales_dataset.csv
```

**Note:** The CSV file is required to run the notebook. Upload it if you have permission to share the dataset. It was referenced in the notebook but was not included as a separate uploaded file.

## 📊 Dataset Description

The notebook expects a CSV file named `ecommerce_sales_dataset.csv` with the following columns:

| Column | Description |
|---|---|
| `Order_ID` | Identifier for an order |
| `Product_Category` | Category of the product |
| `Price` | Price of the product |
| `Quantity` | Quantity purchased |
| `Customer_Rating` | Customer rating for the record |

The notebook creates an additional column, `Total_Sales`, by multiplying `Price` by `Quantity`.

## 🔍 Analysis Performed

### 1. Total Sales Calculation

Calculates sales for each record using:

```python
df["Total_Sales"] = df["Price"] * df["Quantity"]
```

This column is then used to calculate total sales for each product category.

### 2. Category-wise Sales Analysis

Groups the data by product category, sums total sales, and sorts the categories from highest to lowest sales.

The recorded notebook output identifies **Home** as the highest-revenue category.

### 3. Customer Satisfaction Analysis

Calculates the mean of the `Customer_Rating` column to understand the overall rating in the dataset.

### 4. High-Rated Products or Orders

Filters records where the customer rating is greater than 4 and sorts them by rating and total sales.

### 5. Sales Performance Visualization

Creates a bar chart comparing total sales across product categories. The chart includes a title, axis labels, sales-value labels, and grid lines for readability.

### 6. Pricing Analysis

Examines product prices using summary statistics such as minimum, maximum, mean, and median, and creates a histogram to visualize the price distribution.

## 📈 Key Findings

Based on the outputs currently saved in the notebook:

- **Highest-sales category:** Home
- **Home category total sales:** 71,874
- **Electronics category total sales:** 38,910
- **Clothing category total sales:** 24,963
- **Books category total sales:** 7,576
- **Average customer rating:** 3.86 out of 5
- **Records with ratings above 4:** 10
- **Minimum product price:** 331
- **Maximum product price:** 3,890
- **Average product price:** 2,334.05
- **Median product price:** 2,288.50

These findings reflect the saved notebook output and should be verified by running the notebook against the intended dataset.

## 💡 Business Insights

- The Home category contributes the highest recorded sales and may deserve attention during inventory planning.
- The Electronics category is the second-highest sales category in the saved results.
- The average rating provides a general indication of customer feedback, while individual ratings help identify highly rated records.
- The price histogram helps show which price ranges are more common.
- Inventory decisions should consider demand, profit margins, stock levels, and customer feedback in addition to sales totals.

## ⚙️ Installation and Requirements

Install Python and the required libraries:

```bash
pip install pandas matplotlib jupyter
```

## ▶️ How to Run the Project

### Option 1: Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload `ecommerce_sales_analysis.ipynb`.
3. Upload `ecommerce_sales_dataset.csv` to the Colab session.
4. Run the notebook cells in order.

### Option 2: Run Locally

1. Download or clone the repository.
2. Install the required libraries.
3. Place the CSV file in the same folder as the notebook.
4. Open a terminal in that folder and run:

```bash
jupyter notebook
```

5. Open the notebook and run its cells in order.

**Important:** The original notebook uses the Google Colab path `/content/ecommerce_sales_dataset.csv`. When running locally, change the dataset path to:

```python
df = pd.read_csv("ecommerce_sales_dataset.csv")
```

## 🎓 Learning Outcomes

Through this project, I practiced:

- Loading CSV data with Pandas
- Creating calculated columns
- Grouping and aggregating data
- Sorting and filtering records
- Calculating descriptive statistics
- Analyzing customer ratings
- Creating bar charts and histograms
- Interpreting data for business decision-making

## 🚀 Future Enhancements

- Add profit-margin and revenue-trend analysis.
- Compare sales and ratings across categories.
- Include monthly or quarterly sales trends if dates are available.
- Build an interactive dashboard using Streamlit or Power BI.
- Add data cleaning and missing-value checks.
- Provide inventory recommendations using additional stock and demand data.

## 👩‍💻 Author

**Poorvi N S**

B.Tech — Artificial Intelligence and Machine Learning

## 📄 License

This project is intended for educational and learning purposes. Add a license file if you wish to define the terms under which others may reuse your work.
