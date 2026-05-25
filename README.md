## Sales \& Revenue Performance Dashboard

## 

## Power BI Data Analytics Project



##### Project Overview



This project focuses on analyzing sales performance and revenue trends using Power BI based on an E-commerce (Ecom Express) dataset.

The goal is to transform raw transactional data into meaningful business insights through data modeling, DAX measures, and interactive dashboards.



The dashboard enables stakeholders to:



* Monitor overall sales performance



* Identify top-performing products and regions



* Understand customer distribution



* Analyze revenue loss due to order cancellations



* Make informed, data-driven decisions



##### Project Objectives



* Analyze sales and revenue trends



* Identify top-performing products and categories



* Understand customer distribution across states



* Measure the impact of order cancellations



* Deliver interactive and user-friendly dashboards



##### Dataset Overview



The project uses three core datasets:



1️⃣ Customers Table



* CustomerID



* Full Name



* Phone



* City



* State



* OS (Android / iOS)



* Phone Brand



2️⃣ Products Table



* ProductID



* Product Name



* Category



* Price



* Rating



* Number of Ratings



3️⃣ Orders Table



* OrderID



* CustomerID



* ProductID



* Quantity



* Date \& Time of Purchase



* Delivery Status



##### Data Cleaning \& Transformation



* Combined first name and last name → Full Name



* Standardized city names



* Classified OS type (Apple → iOS, Others → Android)



* Converted product price to fixed decimal format



##### Data Modeling



* Star Schema design



* Fact Table: Orders



* Dimension Tables: Customers, Products



Benefits:



* Improved performance



* Accurate filtering



* Better analytical clarity



##### DAX Measures Used

Sales = SUMX(Orders, Orders\[Quantity] \* RELATED(Products\[Price]))



Lost\_rev\_cancellation =

CALCULATE(\[Sales], Orders\[Delivery Status] = "Cancelled")



Revenue = \[Sales] - \[Lost\_rev\_cancellation]



Cancellation Rate =

DIVIDE(

&nbsp;   CALCULATE(COUNTROWS(Orders), Orders\[Delivery Status] = "Cancelled"),

&nbsp;   COUNTROWS(Orders)

)

#### 

##### Dashboard Features



KPI Cards:



* Total Sales



* Revenue



* Lost Revenue



* Cancellation Rate



**Revenue analysis by:**



* State



* Category



* Product



* Monthly revenue trend



* Category-based slicers



* Interactive filtering and drill-down



##### **Key Insights**



* Laptop and Mobile categories generate the highest revenue



* Top-performing states: Maharashtra, Gujarat, Rajasthan



* Cancellation rate (~30%) significantly affects revenue



* Revenue shows seasonal trends



* High-value products generate more revenue despite fewer orders



##### **Future Enhancements**



* Predictive analytics (Sales Forecasting)



* Customer Lifetime Value (CLV) analysis



* Integration with real-time or streaming data




## 📸 Dashboard Preview
![Dashboard Screenshot](<img width="1297" height="727" alt="Screenshot 2026-05-25 155426" src="https://github.com/user-attachments/assets/55e58123-cf9f-4c97-aacb-101bd5137eed" />
)
