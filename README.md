# <h1>Interactive Power BI Dashboards: Sales, Products, and Customers Analysis</h1>

## <h2>Project Overview</h2>
<p>This project showcases three dynamic and minimalistic Power BI dashboards that provide insights into Sales, Products, and Customer behavior. The goal is to present a comprehensive analysis of key business metrics, enabling easy exploration and data-driven decisions through an intuitive interface.</p>

## <h2>Key Features</h2>
<h3>The project includes **three dashboards** that focus on different aspects of the data:</h3>
1. **Sales Dashboard**:
   - Total Sales and Total Quantity Sold (Card): Visualize total revenue and total sold quantity.
   - Total Sales by Month (Line Chart): Tracks sales records every month.
   - Total Sales by Category (Stacked Column Chart): Track sales trends by different categories.
   - Total Sales by Supplier (Line and Stacked Column Chart): Highlight the sales by different suppliers.

2. **Products Dashboard**:
   - Product Qauntity by Category (Clustered Bar Chart): Monitor current stock levels for each product category.
   - Average Product Price by Category (Clustered Column Chart): Monitors the average price of products by category.
   - Average Discount Percentage by Category(Stacked Column Chart): Highlights the average dicount on product categories.

3. **Customers Dashboard**:
   - Customer Demographics (Pie Chart): Understand the gender breakdown of customers.
   - Customer Locations (Map): Geographical visualization of customer distribution.
   - Customer Age Distribution (Line Chart): Analyze customer ages and their distribution.
   - Repeat Customers (KPI): Track repeat customers for loyalty analysis.

## <h2>Data Sources</h2>
The data is generated through PostgreSQL and then exported into excel files for data cleaning and preprocessing.
This project uses the following Excel files:
- **Sales Data**: Contains details on sales transactions.
- **Inventory Data**: Holds product stock levels and supplier information.
- **Promotions Data**: Tracks product promotions, including discounts and dates.
- **Products Data**: Includes product names, categories, and prices.
- **Customer Data**: Contains customer details like age, gender, location, and sign-up dates.

## <h2>DAX Calculations</h2>
The project includes several **DAX (Data Analysis Expressions)** measures for enhanced data insights:
- **Total Sales**:
    ```DAX
    Total Sales = SUM(Sales[total price])
    ```
- **Average Sales**:
    ```DAX
    Average Sales = AVERAGE(Sales[total price])
    ```
- **Repeat Customers**:
    ```DAX
    Repeat Customers = COUNTROWS(FILTER(Sales, CALCULATE(COUNT(Sales[saleid]), ALLEXCEPT(Sales, Sales[customerid])) > 1))
    ```

## <h2>Interactivity & Filters</h2>
To enhance user experience, each dashboard is equipped with slicers for dynamic filtering:
- **Sales Dashboard**: Filter by Location and payment mode.
- **Products Dashboard**: Filter by product category.
- **Customers Dashboard**: Filter by customer location and Demographics(Gender).


## <h2>How to Run the Project</h2>
1. Clone or download this repository.
2. Open **Power BI Desktop**.
3. Open the `.pbix` file included in this repository.
4. Explore the dashboards using the slicers and filters to gain insights.

## <h2>Screenshots</h2>
Include screenshots of the dashboards to give a visual preview of the project:
- [Home Page](https://github.com/dev-thememegod/Retail-Sales-Data-Analysis/blob/main/dash%201.png)
- [Sales Dashboard Screenshot](https://github.com/dev-thememegod/Retail-Sales-Data-Analysis/blob/main/dash%202.png)
- [Products Dashboard Screenshot](https://github.com/dev-thememegod/Retail-Sales-Data-Analysis/blob/main/dash%204.png)
- [Customers Dashboard Screenshot](https://github.com/dev-thememegod/Retail-Sales-Data-Analysis/blob/main/dash%203.png)

## **Contributing**
Feel free to contribute by forking the repository and making enhancements. Pull requests are welcome for new features or improvements.

## <h2>License</h2>
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
