# logistics-etl-scripts

## **INTRODUCTION**

A collection of Python and Google Apps Script tools designed to automate high-volume logistics data reconciliation (2,500+ daily and 75,000+ monthly orders), saving up to 10 hours of manual work weekly.

## OBJECTIVES
**The Challenge:** Last-mile delivery and middle-mile fleet reports required a lot of hours of manual effort.

**The Solution:** Scripts that handle the data preprocessing automatically and generate insights for operational analysis.

#### **TECH STACK**

- **Languages:** Python 3.x, JavaScript (Google Apps Script).
- **Libraries:** Pandas, NumPy, pytz, openpyxl, matplotlib, seaborn, zipfile, os, shutil
- **Platforms:** Google Colab, Google Sheets, Metabase (as a data source in CSV format).

## **WORKFLOW**

| Script Name | Function | Workflow | Output | Tech Stack |
| --- | --- | --- | --- | --- |
| [last_mile_delivery_report_automation_3pl.ipynb](https://github.com/adangkurnia/logistics-etl-scripts/blob/main/notebooks/last_mile_report/last_mile_delivery_report_automation_3pl.ipynb) | Automate data preprocessing to generate excel files based on 3PL name | ETL: CSV → Clean → Excel | Files with xlsx format | Python (Pandas, NumPy, pytz, OpenPyXl) |
| [last_mile_delivery_report_automation_time_slot.ipynb](https://github.com/adangkurnia/logistics-etl-scripts/blob/main/notebooks/last_mile_report/last_mile_delivery_report_automation_time_slot.ipynb) | Automate data preprocessing to generate Excel files based on time slots for next day delivery | ETL: CSV → Clean → Excel | Files with xlsx format | Python (pandas, numpy, pytz, openpyxl) |
| [01_middle_mile_fleet_data_extraction_automation.ipynb](https://github.com/adangkurnia/logistics-etl-scripts/blob/main/notebooks/middle_mile_fleet/01_middle_mile_fleet_data_extraction_automation.ipynb) | Automate data preprocessing to generate csv file | ETL: CSV → Clean → Cleaned CSV | Files with csv format | Python (pandas, numpy) |
| [02_middle_mile_utilization_preview_automation.ipynb](https://github.com/adangkurnia/logistics-etl-scripts/blob/main/notebooks/middle_mile_fleet/02_middle_mile_utilization_preview_automation.ipynb) | Automate fleet capacity dashboards in Google Colab to provide visibility into Middle Mile utilization metrics. | Cleaned CSV → Data Visualization | Dashboard Viz | Python (pandas, numpy, matplotlib, seaborn) |
| [reset_attendance.js](https://github.com/adangkurnia/logistics-etl-scripts/blob/main/app_script/reset_attendance.js) | Automate the data cleaning across multiple tabs | Google Sheets Automation | Clean cells | Apps Script |

## **HOW TO USE**
### 🐍 1. Python (Data Processing & ETL)

These scripts are designed for **Google Colab.**

1. **Open:** Upload the `.ipynb` file to [Google Colab](https://colab.research.google.com/).
2. **Input:** Download the raw `.csv` file sample provided in `/data`.
3. **Run:** Select `Runtime > Run All` from the top menu.
4. **Output:** 
    1. Last mile delivery reconciliation data: the cleaned and formatted `.xlsx` files will be generated and downloaded automatically.
    2. Fleets: the cleaned CSV file and data visualization.

### 📝 2. Google Apps Script (Macro & Spreadsheet Automation)

These scripts are designed to run directly within **Google Sheets**.

1. **Open:** Go to your Google Sheet and select `Extensions > Apps Script`.
2. **Paste:** Copy the code from the `.js` file in this repo into the editor.
3. **Authorize:** Click the **Run** button (the triangle icon). You will need to grant permission for the script to manage your spreadsheet.
4. **Action:** Use the custom menu (e.g., "Logistics Tools") that appears in your Sheet to execute the macro.

#### **KEY ACCOMPLISHMENTS**

- **Scale:** Handled 2,500+ daily orders for last mile delivery and 75k+ monthly order records middle mile fleet utilizations.
- **Time Saved:** Up to 10 hours per week.
- **Accuracy:** 100% data integrity through automated validation logic.
