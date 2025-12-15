# Dashboard-Analysis-for-Hospitals-in-Saudi-Arabia-


## 📄 Project Overview
This project leverages **Data Mining** techniques and **Business Intelligence** (Power BI) to analyze hospital admission records in Riyadh, Saudi Arabia. [cite_start]Covering data from **January 2022 to September 2024**, the analysis processes approximately **23,000 hourly observations** to uncover trends in patient demographics, clinical conditions, and operational efficiency[cite: 362].

The repository is divided into two core components:
1.  **Data Mining & Preprocessing (Python):** A Jupyter Notebook for cleaning, transforming, and exploring the raw data.
2.  **Dashboard Analysis (Power BI):** A summary of the interactive dashboard designed to support decision-making for hospital management, medical departments, and supply chain operations.


## 🛠️ Part 1: Data Mining & Preprocessing (Python)
**File:** `datamining_project.ipynb`

This notebook handles the end-to-end data pipeline, ensuring the raw dataset is clean and structured for downstream analysis.

### ⚙️ Technologies Used
* **Python Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly.express`

### 🔄 Workflow & Key Steps
1.  **Data Loading & Inspection:**
    * [cite_start]Imported the raw dataset: `Hospital_Dataset_2020_2024.csv`[cite: 1].
    * Performed initial schema validation and data type checking.
2.  **Data Cleaning:**
    * [cite_start]**Null Handling:** Identified and managed missing values in columns like `readmission_count` and `severity_level`[cite: 2].
    * [cite_start]**Outlier Removal:** Applied the **Interquartile Range (IQR)** method to filter anomalies in `admission_count`, ensuring statistical robustness[cite: 373].
3.  **Feature Engineering:**
    * Converted `admission_date` to DateTime objects.
    * [cite_start]Extracted temporal features: `admission_hour`, `admission_day`, `admission_month`, and created a boolean flag `admission_is_weekend` to analyze weekly patterns[cite: 374].
4.  **Data Transformation:**
    * [cite_start]**Standardization:** Normalized string data (e.g., Hospital Names, Condition Types) to lowercase and removed whitespace to eliminate duplicates[cite: 375].
    * [cite_start]**Categorization:** Grouped rare medical conditions under an "Other" category to reduce noise and improve visualization clarity[cite: 376].
5.  **Exploratory Data Analysis (EDA):**
    * [cite_start]Visualized total admissions by **Hospital**, **Day of Week**, **Condition Type**, and **Patient Age Group** using Plotly for interactive exploration[cite: 1, 6].
6.  **Export:**
    * [cite_start]The processed dataset was saved as `Hospital_Cleaned_Data.csv` for Power BI integration[cite: 379].

---

## 📊 Part 2: Power BI Dashboard Summary
**Document:** `Dashboard Analysis for Hospitals in Saudi Arabia.docx`

The Power BI dashboard transforms the processed data into actionable insights, utilizing interactive cards, slicers, and charts to answer critical business questions.

### 🎯 Dashboard Components
* **KPI Cards:** Display aggregate metrics such as Total Admissions, Readmissions, Emergency Visits, and Average Length of Stay.
* **Interactive Filters (Slicers):** Allow users to drill down by **Hospital**, **Year**, **Condition Type**, and **Severity Level**.
* **Visualizations:**
    * **Temporal Analysis:** Admission trends by hour, day, and season.
    * **Clinical Breakdown:** Admissions by diagnosis code and severity.
    * [cite_start]**Demographics:** Patient distribution by age and gender[cite: 307].

### 💡 Key Business Insights
| Domain | Question Answered | Insight Derived |
| :--- | :--- | :--- |
| **Top Management** | Which hospitals have the highest volume? | [cite_start]**Riyadh National**, **Dammam Central**, and **Jeddah National** are the top three facilities, with a variance of 200-300 cases between them[cite: 336, 337]. |
| **Medical Dept** | What are the most common conditions? | **Asthma** is the leading cause of admission, followed by **COPD**. The majority of cases are classified as **Moderate** severity. |
| **Operations** | When is the peak demand? | **Thursdays** typically see the highest admission volumes. Emergency visits peak in **Q2**, particularly around **9:00 AM**. |
| **Supply Chain** | What drives medication consumption? | Patients diagnosed with **Asthma (ICD Code J45)** and those in the **18-45 age group** with moderate severity show the highest daily medication usage. |
| **Quality** | Who has the highest readmission rates? | Male patients, who constitute ~60% of the total patient population, exhibit higher readmission rates than females. |

---

## 🚀 How to Run
1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    ```
2.  **Run the Code:**
    * Ensure `Hospital_Dataset_2020_2024.csv` is in the directory.
    * Open `datamining_project.ipynb` in Jupyter Notebook or Google Colab and run all cells to generate the cleaned dataset.
3.  **View the Analysis:**
    * Refer to `Dashboard Analysis for Hospitals in Saudi Arabia.docx` for the full analytical report.
    * (Optional) Import `Hospital_Cleaned_Data.csv` into Power BI to recreate the dashboard visuals.
