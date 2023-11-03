
# Business Insights 360

## Project Overview

AtliQ Hardware is experiencing significant growth and aims to gain a competitive edge by using Power BI for data analytics. They are adopting this technology for the first time to help make informed decisions in areas like finance, sales, marketing, and supply chain. This project is expected to provide valuable insights and answers to the company's key stakeholders across various business aspects.

To view the report, click [here](https://app.powerbi.com/view?r=eyJrIjoiY2MwNmNlMWYtNjc5YS00NGY0LTkwYzYtZmRiZjk2MWQ1ZTVkIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

## Tech stacks

- SQL
- PowerBi Desktop
- Excel
- DAX language
- DAX studio (for optimizing the report)
- Project charter file

## Advanced Power BI Proficiency

- **Project Goals:** What do you want to achieve with this project?

- **Data Sources:** Where is the data coming from, and is it good data?

- **Project Scope:** What are the boundaries of this project?

- **Timeline:** When do you need to finish this project?

- **Resources:** What do you need to get this project done?

- **Project Team:** Who's on your project team and what do they do?

- **Data Security:** How are you protecting sensitive data?

- **Integration:** Does this project connect to other systems?

- **Risks:** What could go wrong, and how will you deal with it?

- **Success Criteria:** How will you know if the project worked?

- **Feedback:** How will you listen to suggestions for improvement?

- **Documentation & Training:** Will you explain how to use the project?

- **Calculated Columns:** How do you add new data columns?

- **Measures with DAX:** What's a way to calculate new numbers in your data?

- **Data Modeling:** How does the data all fit together?

- **Bookmarks for Visuals:** How can you save different views of your data?

- **Page Navigation with Buttons:** How do you move between different views?

- **Divide Function:** How to avoid dividing by zero errors in your calculations?

- **Date Table with M Language:** How to create a special date table using M language?

- **Dynamic Titles:** How to show the right titles based on what you're looking at?

- **KPI Indicators:** How to highlight what's most important in your data?

- **Conditional Formatting:** How to make data look different based on its value?

- **Data Validation:** How to make sure your data is correct?

- **Power BI Services:** How to work with your data in the cloud.

- **Publishing to Power BI Services:** How to share your work with others.

- **Personal Gateway:** How to set up your data to refresh automatically.

- **Power BI App Creation:** How to build an app for your data.

- **Collaboration & Permissions:** How to work together and control who can see what in Power BI Services.

## GitHub

- Uploading Large size files using GitHub LFS.
- Tracking the particular type of file extensions for LFS.

## Business related terms

- **Gross Price:** The initial price of a product before any deductions or expenses.

- **Pre-invoice Deductions:** Deductions made before creating the invoice.

- **Post-Invoice Deductions:** Deductions applied after the invoice is issued.

- **Net Invoice Sale:** The final amount after considering deductions and discounts.

- **Gross Margin:** The profit percentage after accounting for the cost of goods.

- **Net Sales:** The total revenue after all deductions.

- **Net Profit:** The earnings left after subtracting all costs.

- **COGC (Cost of Goods Sold):** The cost to produce the goods.

- **YTD (Year to Date):** Data accumulated from the beginning of the current year.

- **YTG (Year to Go):** Projections for the rest of the current year.

- **Direct:** Sales made directly to customers.

- **Retailer:** Sales through a middleman or store.

- **Distributors:** Sales through wholesalers or distributors.

- **Consumer:** The end-user or customer who buys the product.

## Company’s back ground

AltiQ Hardware, a rapidly growing global company, specializes in selling computers and accessories through three main channels.

- Retailers

- Direct sales

- Distributors

Despite its expansion, the company faced unexpected losses in its American store. To counter this, they've decided to build an analytics team to make data-driven decisions and remain competitive. The project kickoff session aims to clarify the project's purpose, objectives, and address any questions related to its goals and outcomes.

## In preparation for creating a dashboard, what are the essential questions that should be addressed before beginning the project?

- What is the primary goal of developing this Power BI dashboard?
- How will we measure the success of this project?
- What is the project's timeline and deadline?
- Are stakeholders expecting a preview before the official release?
- What are the stakeholders' expectations and aspirations for this project?
- What concerns or fears do the stakeholders have regarding the dashboard's development?
- Who will be the end users of this dashboard, and what will be its intended purpose?
- What are the stakeholders' expectations upon the project's completion?
- What potential challenges or issues might arise during the project?
- What data and resources are necessary to construct this dashboard?
- Have stakeholders provided input on the dashboard's design and views?

After the project kick off meetings, the data engineering team has given the data as per the request of data analytics team, let’s explore them.

## Dataset Understanding

Before diving into analysis, it's essential to have a clear understanding of the available data. Knowing what data is at your disposal is crucial.

- **Dimension Table:** This table contains static information, such as customer and product details. It provides context and reference for the analysis.

- **Fact Table:** This table holds data related to transactions. It records the actual events or transactions that occurred. Analyzing this table can help derive insights and patterns from the real data.

In our setup, we're making use of two databases **gdb041** and **gdb056**. These databases hold distinct data sets and play a role in various aspects of our work or analysis.

- **gdb041**
    - **Table Name: dim_customer**
        - **27 Distinct Markets:** These are different geographic regions or countries where customers are located. Examples include India, USA, and Spain.
        - **75 Distinct Customers:** These are individual entities or businesses that interact with the dataset.
        - **2 Types of Platforms:** Customers can be categorized into two groups based on where they conduct their business:
            - **Brick & Mortar:** These customers operate physical or offline stores.
            - **E-commerce:** These customers conduct their business online through platforms like Amazon and Flipkart.
        - **Three Channels:** These are different ways through which products or services are distributed:
            - **Retailer:** Products are sold through retail stores.
            - **Direct:** Products are sold directly to customers or businesses.
            - **Distributors:** Products are sold through intermediaries or wholesalers.
    
    - **Table Name: dim_market**
        - **27 Distinct Markets:** This table categorizes different markets, such as India, the USA, and Spain.
        - **7 Sub-zones:** The markets are further grouped into sub-zones for more specific analysis.
        - **4 Regions:** These markets are organized into four regions.
            - APAC
            - EU
            - LATAM
            - NA

    - **Table Name: dim_product**
        - **Divisions:** This table classifies products into different divisions.
            - P & A (Peripherals & Accessories)
            - PC (Personal Computers)
            - Notebook
            - Desktop
            - N & S (Networking & Storage).

        - **Categories:** There are 14 different categories, Like Internal HDD, keyboard
        - **Variants:** There are different variants available for the same product
    
    - **Table Name:  fact_forecast_monthly**
        - **Forecasting Customer Demand:** The table is utilized to predict what customers will need in advance.
        - **Benefits of Forecasting:** Higher Customer Satisfaction: Accurate forecasts lead to better customer satisfaction as products or services are available when needed.
        - **Reduced Warehousing Costs:** By forecasting demand, companies can minimize excess inventory and the associated warehousing costs.
        - **Denormalization:** The table is intentionally denormalized by the data engineering team. This means it's structured for analytical purposes and might combine data that's typically kept separate for efficient analysis.
        - **Date Representation:** All dates in the table are replaced with the start date of each respective month. This simplifies data handling and aligns data points for monthly forecasting.
        - **Column Structure:** The table contains various columns that store relevant information for the forecasting process.
        - **Forecast Quantity:** Ultimately, the table provides the crucial information of the forecasted quantity needed by customers, allowing businesses to plan and allocate resources effectively.

    
    - **Table Name:  fact_sales_monthly**
        - The "fact_sales_monthly" table records monthly sales data, similar to "fact_forecast_monthly," but with actual quantities sold instead of forecasts, enabling performance analysis.
    
- **gdb056**
    - **freight_cost:** Contains data related to travel and other costs for each market, organized by fiscal year.
    - **gross_price:** Provides details about gross prices for products, including product codes.
    - **manufacturing_cost:** Contains information on manufacturing costs for products, with product codes and associated years.
    - **Pre_invoice_deductions:** Includes data on pre-invoice deductions percentages for each customer, categorized by year.
    - **Post_invoice_deductions:** This table encompasses details on post-invoice deductions and other types of deductions.

## Importing data into PowerBi

To import MySQL database data into Power BI, provide database access details, select desired tables, and load the data for analysis.

## Data Model

 - **Data Modeling Foundation:** Data modeling is the fundamental structure on which a report is built, and all visual elements rely on it.

- **Impact of Poor Data Modeling:** Inadequate data modeling can negatively affect the overall performance and usability of the report.

- **Best Practices:** Adhering to best practices in data modeling is essential to ensure the report's effectiveness and accuracy.

- **Reference to Good Practices Blog:** There is a blog or resource that provides guidance on good data modeling practices. You can refer to this [page](https://addendanalytics.com/blog/data-modelling-best-practices/) for more information and insights.

- **Snowflake Data Modeling Method:** The project adopts the Snowflake data modeling method, which is a recognized approach to designing a structured and efficient data model for reporting and visualization.

![model_view](https://github.com/vikaskushwah312/Business-Insights-360/blob/main/Resources/model_view.png)

## Dashboard Designing Process:
**Designing Visuals:** The team will create visual elements based on received mockups and develop necessary measures.

**Home View:** The home view provides access to various sections or views. Users can navigate to specific view pages by clicking the corresponding buttons.
- **Info**
- **Finance View**
- **Sales View**
- **Marketing View**
- **Supply Chain View**
- **Executive View**
- **Support**

  ## Overall Report


https://github.com/vikaskushwah312/Business-Insights-360/assets/46120892/9e64571a-3a1d-401f-b351-eb64fc853b27

you can find the full report file here : [Report](https://app.powerbi.com/view?r=eyJrIjoiY2MwNmNlMWYtNjc5YS00NGY0LTkwYzYtZmRiZjk2MWQ1ZTVkIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

## Project Outcome
This report enables data-driven decision-making and provides answers to numerous "why" questions in various situations.

