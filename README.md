# Adidas Sales Data Analysis

This project performs an Exploratory Data Analysis (EDA) on Adidas sales data. The primary goal is to clean, preprocess, and analyze sales patterns to derive insights.

The analysis uses two main datasets: `Adidas US Sales Datasets.csv` and `AdidasSalesdata.csv`. These datasets are merged into a consolidated file, `Adidas_sales.csv`, which forms the basis for the EDA.

## Data Cleaning and Preprocessing

The `project Adidas_Sales.ipynb` notebook performs several data cleaning and preprocessing operations, including:

*   **Data Loading and Merging:** Reading `Adidas US Sales Datasets.csv` and `AdidasSalesdata.csv`, and then concatenating them into a single DataFrame.
*   **Column Renaming:** Standardizing column names by replacing spaces with underscores (e.g., 'Invoice Date' to 'Invoice_Date').
*   **Data Type Conversion:**
    *   Converting 'Invoice_Date' to a consistent 'mm-yyyy' string format after parsing it as datetime.
    *   Cleaning and converting currency and percentage strings (e.g., 'Price per Unit', 'Total_Sales', 'Operating_Profit', 'Operating_Margin', 'Units_Sold') to numeric data types (integers and floats).
*   **Feature Engineering:**
    *   Extracting 'Product_Category' (e.g., 'Street Footwear', 'Apparel') and 'Gender_Type' (e.g., 'Men', 'Women') from the 'Product' column.
*   **Data Cleansing:**
    *   Removing the original 'Product' and 'Retailer_ID' columns as they are either redundant or transformed.
    *   Removing duplicate rows from the merged dataset.
    *   Filtering out rows where key numerical columns ('Price_per_Unit', 'Units_Sold', 'Total_Sales', 'Operating_Profit') have zero values, as these might not be relevant for sales analysis.
*   **Index Resetting:** Resetting the DataFrame index after cleaning operations to ensure a clean sequence.

## Exploratory Data Analysis (EDA)

The notebook explores various aspects of the sales data through summary statistics and visualizations. Key analyses include:

*   **Understanding Data Distributions:**
    *   Distribution of units sold per transaction (Histogram with KDE).
    *   Distribution of operating margins (Distribution plot with KDE).
*   **Sales Trends and Performance:**
    *   Trend of total sales over months, broken down by sales method (Line chart).
    *   Number of transactions by sales method (Count plot).
    *   Total sales variation by region (Bar chart).
    *   Total sales variation by state and differentiated by gender type (Bar chart).
    *   Distribution of total sales among different cities (Box plot).
    *   Distribution of total sales among product categories (Bar chart).
*   **Profitability Analysis:**
    *   Distribution of operating profit among different retailers (Pie chart).
*   **Price Analysis:**
    *   Impact of price per unit on units sold for different product categories (Scatter plots).

## Technologies Used

*   **Python:** The core programming language used for the analysis.
*   **Pandas:** For data manipulation, cleaning, and aggregation.
*   **Matplotlib:** For creating static, animated, and interactive visualizations.
*   **Seaborn:** For making statistical graphics and enhancing matplotlib plots.
*   **Jupyter Notebook:** As the environment for writing and executing the analysis code.

## How to Run the Project

1.  **Prerequisites:** Ensure you have Python installed on your system. You will also need the following libraries:
    *   pandas
    *   matplotlib
    *   seaborn
    *   Jupyter Notebook or JupyterLab

    You can install these libraries using pip:
    ```bash
    pip install pandas matplotlib seaborn notebook
    ```
2.  **Data Files:** Make sure the following data files are in the root directory of the project (or update the file paths in the notebook accordingly):
    *   `Adidas US Sales Datasets.csv`
    *   `AdidasSalesdata.csv`
3.  **Run Jupyter Notebook:**
    *   Navigate to the project's root directory in your terminal or command prompt.
    *   Launch Jupyter Notebook by running: `jupyter notebook`
    *   Open the `project Adidas_Sales.ipynb` file from the Jupyter Notebook interface in your browser.
    *   You can run the notebook cells sequentially to perform the data loading, cleaning, preprocessing, and exploratory data analysis.

## Data Source

The analysis is based on two primary CSV files:
*   `Adidas US Sales Datasets.csv`
*   `AdidasSalesdata.csv`

These files are merged into `Adidas_sales.csv` during the preprocessing phase. The specific origin of these datasets is not detailed within the project notebook.

## Presentation

A PowerPoint presentation summarizing the key findings from the Exploratory Data Analysis can be found in the `Project Adidas Sales - EDA.pptx` file.
