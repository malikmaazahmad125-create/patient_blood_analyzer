## **📌 Project Overview**

**Patient Blood Test Analyzer** is a Python-based **Computational Biology and Biological Data Analysis project** developed to analyze structured patient blood-test data.

The project demonstrates a complete analytical workflow starting from patient data collection and progressing through **Python dictionaries, functions, conditional analysis, NumPy calculations, percentile analysis, Pandas DataFrames, filtering, GroupBy analysis, statistical summaries, and Matplotlib visualizations**.

The analyzer works with important patient parameters including:

- 🧑 **Patient Name**
- 🎂 **Age**
- 🩸 **Blood Group**
- 🧬 **Hemoglobin**
- 🧪 **Glucose**
- 🧪 **Cholesterol**

The purpose of this project is to demonstrate how programming and data-analysis techniques can be applied to structured biological datasets.

---

## **🎯 Project Objectives**

The project is designed to:

- **Store patient information** using Python Dictionaries
- **Build reusable analysis** using Functions
- **Apply If / Elif / Else conditions**
- **Perform numerical calculations** using NumPy
- **Calculate Percentiles**
- **Create structured Pandas DataFrames**
- **Filter patients** using biological measurements
- **Perform GroupBy analysis**
- **Generate descriptive statistical summaries**
- **Create meaningful data visualizations**
- **Develop practical Computational Biology skills**

---

## **🧰 Technologies & Libraries**

| **Technology** | **Purpose** |
|---|---|
| 🐍 **Python** | Core programming and analysis |
| 🔢 **NumPy** | Numerical and statistical calculations |
| 🐼 **Pandas** | Data manipulation and DataFrame analysis |
| 📊 **Matplotlib** | Data visualization |
| 📓 **Jupyter Notebook** | Interactive development and visualization |

---

## **🔬 Patient Data Parameters**

| **Parameter** | **Description** |
|---|---|
| **Name** | Patient identification |
| **Age** | Patient age |
| **Blood_Group** | Patient blood-group category |
| **Hemoglobin** | Hemoglobin measurement |
| **Glucose** | Blood glucose measurement |
| **Cholesterol** | Cholesterol measurement |

---

## **⚙️ Core Features**

### **🗂️ Patient Data Using Dictionary**

Patient information is initially represented using a Python dictionary containing key-value pairs.

```python
patient = {
    "Name": "Ali",
    "Age": 25,
    "Blood_Group": "A+",
    "Hemoglobin": 14.2,
    "Glucose": 95,
    "Cholesterol": 180
}

🔬 **Patient Data Parameters**

Parameter

Description

Name

Patient identification

Age

Patient age

Blood_Group

Patient blood-group category

Hemoglobin

Hemoglobin measurement

Glucose

Blood glucose measurement

Cholesterol

Cholesterol measurement

⚙️ **Core Features**

🗂️ **Patient Data Using Dictionary**

Patient information is initially represented using a Python dictionary containing key-value pairs.

patient = {
    "Name": "Ali",
    "Age": 25,
    "Blood_Group": "A+",
    "Hemoglobin": 14.2,
    "Glucose": 95,
    "Cholesterol": 180
}

This provides the initial structure for individual patient-level analysis.

⚙️ **Functions & Conditional Analysis**

A custom function is used to analyze individual patient test values.

Conditional statements classify measurements into:

LOW
NORMAL
HIGH

The project applies conditional logic to:

Hemoglobin
Glucose
Cholesterol

This demonstrates how computational rules can be applied to biological measurements.

🔢 **NumPy Numerical Analysis**

Numerical measurements are converted into NumPy arrays for efficient mathematical analysis.

hemoglobin = np.array([14.2, 11.8, 13.6, 15.1])
glucose = np.array([95, 110, 88, 102])

**The project calculates:**

Mean
Maximum
Minimum

This provides a numerical overview of the patient dataset.

📐 **Percentile Analysis**

The project calculates the:

25th Percentile
50th Percentile
75th Percentile

for Hemoglobin and Glucose.

Percentile analysis helps describe the distribution and relative position of measurements within the dataset.

🐼**Pandas DataFrame**

The patient information is converted into a structured Pandas DataFrame.

Name	Age	Blood Group	Hemoglobin	Glucose	Cholesterol
Ali	25	A+	14.2	95	180
Ahmad	32	B+	11.8	110	220
Sara	28	O+	13.6	88	170
Ayesha	35	A+	15.1	102	190

The DataFrame provides a convenient structure for filtering, grouping, statistical analysis, and visualization.

🔎 $$**Data Filtering**

The project uses Pandas Boolean filtering to identify specific patient groups.

🧪 High Glucose Patients
data[data["Glucose"] > 100]

Identifies patients whose glucose value is above the selected threshold.

🩸 Low Hemoglobin Patients
data[data["Hemoglobin"] < 12]

Identifies patients whose hemoglobin value is below the selected threshold.

🧪#**High Cholesterol Patients**
data[data["Cholesterol"] > 200]

Identifies patients whose cholesterol value is above the selected threshold.

🧬 ##**GroupBy Analysis**

The project performs blood-group-based analysis using Pandas groupby().

data.groupby("Blood_Group")[["Hemoglobin", "Glucose"]].mean()

Patients are grouped according to their Blood Group, and the average Hemoglobin and Glucose values are calculated for each group.

Blood Group	Average Hemoglobin	Average Glucose
A+	14.65	98.50
B+	11.80	110.00
O+	13.60	88.00

This demonstrates how categorical biological variables can be used to organize and compare numerical measurements.

📊 ##**Statistical Summary**

The project uses:

data.describe()

to generate a descriptive statistical summary.

The summary contains:

Count
Mean
Standard Deviation
Minimum
25%
50%
75%
Maximum

This provides a compact overview of the numerical characteristics of the patient dataset.

📈 Data Visualization

##**The project uses Matplotlib to convert numerical patient information into visual representations.**

🧪 Glucose Level Visualization
x = data["Name"]
y = data["Glucose"]

plt.bar(x, y, color=["black", "burlywood", "seagreen", "darkblue"])

plt.title("PATIENTS GLUCOSE LEVELS")
plt.xlabel("Patient Names")
plt.ylabel("Glucose Levels")

plt.show()

##**This bar chart compares glucose levels between individual patients.**

🩸 Hemoglobin Level Visualization
x = data["Name"]
y = data["Hemoglobin"]

plt.bar(x, y, color=["black", "burlywood", "seagreen", "darkblue"])

plt.title("PATIENTS HEMOGLOBIN LEVELS")
plt.xlabel("Patient Names")
plt.ylabel("Hemoglobin Levels")

plt.show()

##**This visualization compares Hemoglobin levels across patients.**

🧬 Blood Group Distribution
blood_counts = data["Blood_Group"].value_counts()

plt.bar(
    blood_counts.index,
    blood_counts.values,
    color=["black", "seagreen", "darkblue"]
)

plt.title("PATIENT BLOOD GROUP DISTRIBUTION")
plt.xlabel("Blood Group")
plt.ylabel("Number of Patients")

plt.show()

This visualization represents the number of patients belonging to each blood group.

🧪 Cholesterol Level Visualization
x = data["Name"]
y = data["Cholesterol"]

plt.bar(x, y, color=["black", "burlywood", "seagreen", "darkblue"])

plt.title("PATIENTS CHOLESTEROL LEVELS")
plt.xlabel("Patient Names")
plt.ylabel("Cholesterol Levels")

plt.show()

This bar chart compares cholesterol measurements between patients.

🔄 ##**Complete Analysis Workflow**
Patient Information
        ↓
Python Dictionary
        ↓
Functions & Conditions
        ↓
NumPy Arrays
        ↓
Numerical Statistics
        ↓
Percentile Analysis
        ↓
Pandas DataFrame
        ↓
Data Filtering
        ↓
Blood Group GroupBy
        ↓
Statistical Summary
        ↓
Matplotlib Visualization
        ↓
Biological Data Interpretation
🧠 ##**Concepts Demonstrated**
Concept	Implementation
Python Dictionaries	Patient data storage
Functions	Patient analysis
Conditional Logic	LOW / NORMAL / HIGH classification
NumPy Arrays	Numerical data
NumPy Statistics	Mean, maximum, minimum
Percentiles	Distribution analysis
Pandas DataFrame	Structured patient data
Boolean Filtering	Patient selection
GroupBy	Blood-group analysis
Descriptive Statistics	Dataset summary
Matplotlib	Graphical visualization
Bar Charts	Patient comparison
💡Analytical Insights

The project demonstrates how computational analysis can identify patterns such as:

Patients with relatively higher glucose values
Patients with lower hemoglobin values
Patients with elevated cholesterol values
Average Hemoglobin values across blood groups
Average Glucose values across blood groups
Patient blood-group distribution
Differences between individual patient measurements

The project therefore demonstrates the transition from raw biological measurements → structured data → computational analysis → visualization → interpretable insights.

⚠️ ##**Disclaimer:** This project is intended for educational and computational analysis purposes. The thresholds and classifications used in the project should not be considered medical diagnosis or clinical advice.

🚀 ##**Future Improvements**

##**The project can be further enhanced with:**

📂 CSV file integration
📊 Excel data integration
👥 Larger patient datasets
🧪 Additional blood-test parameters
📈 Correlation analysis
🔥 Heatmap visualization
📉 Distribution plots
📊 Interactive dashboards
🧮 Advanced statistical analysis
🤖 Machine Learning classification
💾 Automated patient reports
🧬 Large-scale biological datasets
▶️ How to Run
1. Clone the Repository
git clone <your-repository-url>
2. Install Required Libraries
pip install -r requirements.txt
3. Run the Project
python patient_blood_analyzer.py
4. Jupyter Notebook

##**The project can also be executed in Jupyter Notebook to interactively view:**

Patient DataFrames
Statistical outputs
Filtering results
GroupBy results
Matplotlib visualizations

Run cells using:

Shift + Enter
##**📁 Project Structure**
Patient-Blood-Test-Analyzer/
│
├── patient_blood_analyzer.py
├── patient_blood_analyzer.png
├── README.md
└── requirements.txt
📦 Requirements

##**Create a requirements.txt file:**

numpy
pandas
matplotlib

Install all dependencies using:

pip install -r requirements.txt
🌱 ##**Learning Outcomes**

This project provides practical experience in:

Python Programming → NumPy → Pandas → Data Filtering → GroupBy → Statistics → Visualization → Computational Biology

It builds a foundation for developing more advanced Computational Biology, Biological Data Science, and Machine Learning projects.

⭐## **Project Highlights**
Category	Details
🧬 Domain	Computational Biology
🐍 Language	Python
🩸 Dataset	Patient Blood-Test Data
🔢 Numerical Analysis	NumPy
🐼 Data Analysis	Pandas
🔎 Filtering	Boolean Conditions
🧬 Group Analysis	Blood Group GroupBy
📊 Statistics	Mean, Percentiles, Describe
📈 Visualization	Matplotlib Bar Charts
📓 Environment	Jupyter Notebook
👨‍💻 ## **Author**
Muhammad Maaz
🧬 Coding With Maazi

Computational Biology • Python • Data Analysis • Biological Data Science

## **🏁 Conclusion**

Patient Blood Test Analyzer demonstrates a complete computational workflow for analyzing structured biological patient data.

Starting from a Python dictionary, the project progresses through functions, conditional statements, NumPy calculations, percentile analysis, Pandas DataFrames, filtering, GroupBy analysis, descriptive statistics, and Matplotlib visualizations.

The project demonstrates how fundamental programming and data-analysis techniques can transform raw patient measurements into structured, interpretable, and visually meaningful computational results.

🧬 Patient Data → Computational Analysis → Statistical Results → Visualization → Biological Insights
🚀 ### **🚀 Coding With Maazi**

Keep Learning • Keep Coding • Keep Building 🧬
