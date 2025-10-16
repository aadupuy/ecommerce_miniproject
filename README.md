E-Commerce mini project (Ad / Recommendation focus)

Goal: predict whether a user will purchase an item (or recommend top items) using an e-commerce dataset.

Dataset: Online Retail Dataset from Kaggle
- 500k+ transactions
- Fields: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

More details on each field:
- InvoiceNo: 25,900 unique values ; either numeric (completed transaction), starting with C (canceled transation) or A (adjusted transaction)

Data Cleaning:
- Remove canceled or adjusted transactions (InvoiceNo being non-numeric, starting with C or A)
- Converted InvoiceDate to datetime format and computed TotalPrice = Quantity * UnitPrice

Exploratory Data Analysis (EDA)
- Looked at number of unique users, number of purchases per user/item
- Visualized top10 selling items
- Visualized purchase trends over time: spike around November / December
- Looked at quantity distributions: most products are bought in small quantities per transaction (<~10), meaning that most customers buy only a few units per transaction, but few transactions involve very large quantities

Looked for seasonality or patterns by month / week / day
- Number of transaction or revenue per month show a spike around November / December: holiday season

Feature Engineering
- Defined user features: total purchases per user, average basket size per user, recency (number of days since last purchase) per user
- Defined item features: total quantity sold per item, average price per item, item popularity (number of unique buyers)
- Defined user-item interaction features: purchase frequency (how many times a user bought the same item), last purchase gap (number of days between a user buys the same item)
- Encoded categorical features (strings to integers): StockCode, Country (we do not need to encode Description since an item can already be identified by its StockCode)

