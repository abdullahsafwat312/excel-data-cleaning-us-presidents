# 🇺🇸 US Presidents Dataset: Data Cleaning & Standardization

## 📌 Project Overview
This project focuses on cleaning, parsing, and standardizing an unformatted raw dataset containing historical information about US Presidents, their prior positions, political parties, vice presidents, salaries, and metadata using **Microsoft Excel**.

---

## 🛠️ Tools & Techniques Used
* **Primary Tool:** Microsoft Excel
* **Excel Functions:** `PROPER()`, `TRIM()`, `CLEAN()`, `SUBSTITUTE()`
* **Data Processing Tools:** Text-to-Columns, Find & Replace, Custom Delimiters
* **Formatting:** Number/Currency Formatting, Data Alignment, Date Standardization (`MM/DD/YYYY`)

---

## 🔍 Data Quality Issues Identified (Before State)
* **Inconsistent Text Formatting:** Names contained irregular capitalization (e.g., `john tyyler`, `JAMES MONROE`).
* **Merged Fields:** Prior political roles were concatenated directly into the political party column (e.g., `Commander-in-Chief of the Nonpartisan`, `1st Vice President of the Uni Federalist`).
* **Encoding & Artifact Errors:** Text columns contained special character corruptions (e.g., `â€“`, `froi`).
* **Unformatted Numbers:** Salaries were stored as plain integers without currency symbols or commas.
* **Typographical Errors:** Misspellings in historical names and positions.

---

## ⚙️ Cleaning Methodology & Steps Applied

### 1. Text Standardization & Casing
* Applied `=PROPER()` to normalize capitalization across all president, vice president, and party names.
* Wrapped columns in `=TRIM()` and `=CLEAN()` to eradicate extra whitespace and non-printable characters.

### 2. Data Parsing & Column Separation
* Used **Text to Columns** to isolate prior political titles into a separate dedicated column (`prior`) from the core `party` affiliation column.

### 3. Artifact & Typo Correction
* Utilized **Find & Replace** / `=SUBSTITUTE()` to eliminate corrupted encoding symbols (`â€“`).
* Corrected misspelled entries across official names and titles.

### 4. Data Type Formatting
* Converted raw numbers in the `salary` column to standard Currency (`$#,##0.00`).
* Aligned date formats across `date updated` and `date created` into standard `MM/DD/YYYY`.

---

## 📄 Dataset Access

The complete workbook is available in a single file:

* 📊 **[Data Cleaning Excel .xlsx](<Data%20Cleaning%20Excel%20.xlsx>)**

### Worksheets Included:
1. **Raw Data:** The original uncleaned dataset with formatting errors and merged fields.
2. **Cleaned Data:** The final, standardized, and structured dataset ready for analysis.
