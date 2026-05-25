# 📊 Python Automated Transaction Report Generator

## 🧩 Business Problem
Financial transaction systems generate large volumes of raw data that must be analyzed at a merchant level for:<br>
• Risk monitoring<br>
• Fraud detection<br>
• Compliance reporting<br>
• Operational insights

Manually splitting and formatting these reports is: <br>
• ⏱️ Time-consuming<br>
• ❌ Error-prone<br>
• 📉 Not scalable for high-volume datasets<br>

This project automates the entire reporting pipeline.

## 🚀 Solution Overview
This project streamlines the transformation of raw transaction data into **structured, merchant-wise Excel reports** with professional formatting.

It eliminates manual effort by:<br>
• Splitting data by merchant<br>
• Generating individual Excel reports<br>
• Applying financial-grade formatting<br>
• Producing analysis-ready outputs for stakeholders

## ⚙️ Key Features
• Automatic CSV ingestion using pandas<br>
• Merchant-wise segmentation of transactions<br>
• Individual Excel report generation per merchant<br>
• Professional formatting using openpyxl:<br>
&nbsp;&nbsp;&nbsp;&nbsp;◦ Bold header rows<br>
&nbsp;&nbsp;&nbsp;&nbsp;◦ Center alignment<br>
&nbsp;&nbsp;&nbsp;&nbsp;◦ Cell borders<br>
&nbsp;&nbsp;&nbsp;&nbsp;◦ Date-time formatting<br>
• Auto-adjust column widths for readability<br>
• Scalable structure for large datasets

## 🏗️ System Architecture
The pipeline follows a simple 4-stage process:<br>
**1. Data Ingestion**<br>
&nbsp;&nbsp;&nbsp;&nbsp;Load raw transaction CSV into pandas DataFrame<br>
**2. Data Segmentation**<br>
&nbsp;&nbsp;&nbsp;&nbsp;Split dataset based on unique `MERCHANT` values<br>
**3. Report Generation**<br>
&nbsp;&nbsp;&nbsp;&nbsp;Export each merchant dataset into Excel format<br>
**4. Formatting Layer**<br>
&nbsp;&nbsp;&nbsp;&nbsp;Apply Excel styling using `openpyxl` for readability and presentation

## 📂 Project Structure
```
Python-Automated-Transaction-Report-Generator/
│
├── TRANSACTIONS.csv                 # Input dataset
├── script.py                       # Main automation script
├── destination_folder/             # Generated merchant reports
│   ├── SUSPICIOUS_TRANSACTIONS_REPORT - Merchant_1.xlsx
│   ├── SUSPICIOUS_TRANSACTIONS_REPORT - Merchant_2.xlsx
│   └── ...
└── README.md
```

## 📷 Output Preview
## 📊 Merchant-wise Transaction Report

Below are a few sample generated reports:<br>

Merchant_1
![Image_1](images/01_image.png)

Merchant_2
![Image_2](images/02_image.png)

## 🔍 Formatting Detail View

Zoomed-in view showing formatting applied using `openpyxl`:<br>
• Bold headers<br>
• Center alignment<br>
• Borders applied<br>
• Clean financial layout<br>

![Image_3](images/03_image.png)

## 📊 Impact
• **Report generation time** – What took hours manually now completes in seconds, a reduction of over 99%<br>
• **Scalability** – The manual process struggled with large volumes; the automated solution handles growth seamlessly<br>
• **Error rate** – Human errors like typos, missed rows, and formatting mistakes have been virtually eliminated<br>
• **Consistency** – Outputs are now fully standardized, with uniform formatting, borders, alignment, and column widths across every file

## 🧠 Code Highlights
• **Merchant-wise Splitting Logic**
```
source_dataframe['MERCHANT'].unique()
```

• **Data Filtering**
```
filtered_data = source_dataframe[source_dataframe['MERCHANT'] == merchant_name]
```

• **Excel Export**
```
filtered_data.to_excel(output_file_path, index = False)
```

• **Formatting Layer**
&nbsp;&nbsp;&nbsp;&nbsp;◦ Borders applied using `openpyxl.styles.Border`
&nbsp;&nbsp;&nbsp;&nbsp;◦ Alignment using `openpyxl.styles.Alignment`
&nbsp;&nbsp;&nbsp;&nbsp;◦ Date formatting applied for datetime objects
&nbsp;&nbsp;&nbsp;&nbsp;◦ Auto column width optimization for readability

## 📌 Use Cases
This automation is useful for:<br>
• 🛡️ Fraud & risk monitoring teams<br>
• 💳 Payment transaction analysis<br>
• 📊 Merchant-level reporting systems<br>
• 📑 Compliance & audit workflows<br>
• 📈 Operational analytics dashboards<br>

## 🎯 Key Learnings
• Automating financial reporting workflows using Python<br>
• Working with pandas for data segmentation<br>
• Advanced Excel formatting using openpyxl<br>
• File system automation and dynamic report generation<br>
• Designing scalable data processing pipelines<br>

View notebook with detailed steps here: [Automated Transaction Report Generator](PYTHON_AUTOMATED_TRANSACTION_REPORT_GENERATOR.ipynb)
