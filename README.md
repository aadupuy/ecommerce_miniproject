E-Commerce mini project (Ad / Recommendation focus)

Goal: predict whether a user will purchase an item (or recommend top items) using an e-commerce dataset.

Dataset: Online Retail Dataset from Kaggle
- 500k+ transactions
- Fields: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

More details on each field:
- InvoiceNo: 25,900 unique values ; either numeric (completed transaction), starting with C (canceled transation) or A (adjusted transaction)

Data Cleaning:
- Remove canceled or adjusted transactions (InvoiceNo being non-numeric, starting with C or A)