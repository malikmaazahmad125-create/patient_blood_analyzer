import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

pd.set_option("display.float_format", "{:.2f}".format)


# ==========================================
# PATIENT BLOOD TEST DATA
# ==========================================

patient = {
    "Name": "Ali",
    "Age": 25,
    "Blood_Group": "A+",
    "Hemoglobin": 14.2,
    "Glucose": 95,
    "Cholesterol": 180
}

print("\nPATIENT BLOOD TEST DATA")
print("." * 35)
print(patient)


# ==========================================
# FUNCTION + CONDITIONS
# ==========================================

def check_patient(patient):

    print("\nPATIENT TEST ANALYSIS")
    print("." * 30)

    if patient["Hemoglobin"] < 12:
        print("Hemoglobin: LOW")
    elif patient["Hemoglobin"] > 17:
        print("Hemoglobin: HIGH")
    else:
        print("Hemoglobin: NORMAL")

    if patient["Glucose"] < 70:
        print("Glucose: LOW")
    elif patient["Glucose"] > 100:
        print("Glucose: HIGH")
    else:
        print("Glucose: NORMAL")

    if patient["Cholesterol"] > 200:
        print("Cholesterol: HIGH")
    else:
        print("Cholesterol: LOW")


check_patient(patient)


# ==========================================
# NUMPY STATISTICS
# ==========================================

hemoglobin = np.array([14.2, 11.8, 13.6, 15.1])
glucose = np.array([95, 110, 88, 102])
cholesterol = np.array([180, 220, 170, 190])

print("\nNUMPY STATISTICS")
print("." * 35)

print("Average Hemoglobin:", np.mean(hemoglobin))
print("Maximum Hemoglobin:", np.max(hemoglobin))
print("Minimum Hemoglobin:", np.min(hemoglobin))

print("Average Glucose:", np.mean(glucose))
print("Maximum Glucose:", np.max(glucose))
print("Minimum Glucose:", np.min(glucose))

print("Average Cholesterol:", np.mean(cholesterol))
print("Maximum Cholesterol:", np.max(cholesterol))
print("Minimum Cholesterol:", np.min(cholesterol))


# ==========================================
# PERCENTILE ANALYSIS
# ==========================================

print("\nPERCENTILE ANALYSIS")
print("." * 35)

print("Hemoglobin 25th Percentile:",
      np.percentile(hemoglobin, 25))

print("Hemoglobin 50th Percentile:",
      np.percentile(hemoglobin, 50))

print("Hemoglobin 75th Percentile:",
      np.percentile(hemoglobin, 75))

print("Glucose 25th Percentile:",
      np.percentile(glucose, 25))

print("Glucose 50th Percentile:",
      np.percentile(glucose, 50))

print("Glucose 75th Percentile:",
      np.percentile(glucose, 75))

print("Cholesterol 25th Percentile:",
      np.percentile(cholesterol, 25))

print("Cholesterol 50th Percentile:",
      np.percentile(cholesterol, 50))

print("Cholesterol 75th Percentile:",
      np.percentile(cholesterol, 75))


# ==========================================
# PATIENT BLOOD TEST DATAFRAME
# ==========================================

data = pd.DataFrame({
    "Name": ["Ali", "Ahmad", "Sara", "Ayesha"],
    "Age": [25, 32, 28, 35],
    "Blood_Group": ["A+", "B+", "O+", "A+"],
    "Hemoglobin": [14.2, 11.8, 13.6, 15.1],
    "Glucose": [95, 110, 88, 102],
    "Cholesterol": [180, 220, 170, 190]
})

print("\nPATIENT BLOOD TEST DATAFRAME")
print("." * 35)
print(data)


# ==========================================
# FILTERED DATAFRAME
# ==========================================

print("\nFILTERED DATAFRAME")
print("." * 35)

high_glucose = data[data["Glucose"] > 100]

print("\n1. HIGH GLUCOSE PATIENTS:")
print(high_glucose)

low_hemoglobin = data[data["Hemoglobin"] < 12]

print("\n2. LOW HEMOGLOBIN PATIENTS:")
print(low_hemoglobin)

high_cholesterol = data[data["Cholesterol"] > 200]

print("\n3. HIGH CHOLESTEROL PATIENTS:")
print(high_cholesterol)


# ==========================================
# GROUPBY ANALYSIS
# ==========================================

group_analysis = data.groupby("Blood_Group")[
    ["Hemoglobin", "Glucose"]
].mean()

print("\nGROUP ANALYSIS")
print("." * 35)
print(group_analysis)


# ==========================================
# STATISTICS SUMMARY
# ==========================================

print("\nSTATISTICS SUMMARY IS GIVEN BELOW:")
print("." * 35)
print(data.describe())


# ==========================================
# VISUALIZATION 1
# PATIENT GLUCOSE LEVELS
# ==========================================

x = data["Name"]
y = data["Glucose"]

plt.figure(figsize=(8, 5))

plt.bar(
    x,
    y,
    color=["black", "burlywood", "seagreen", "darkblue"]
)

plt.title("PATIENTS GLUCOSE LEVELS")
plt.xlabel("Patient Names")
plt.ylabel("Glucose Levels")

plt.show()


# ==========================================
# VISUALIZATION 2
# PATIENT HEMOGLOBIN LEVELS
# ==========================================

x = data["Name"]
y = data["Hemoglobin"]

plt.figure(figsize=(8, 5))

plt.bar(
    x,
    y,
    color=["black", "burlywood", "seagreen", "darkblue"]
)

plt.title("PATIENTS HEMOGLOBIN LEVELS")
plt.xlabel("Patient Names")
plt.ylabel("Hemoglobin Levels")

plt.show()


# ==========================================
# VISUALIZATION 3
# BLOOD GROUP DISTRIBUTION
# ==========================================

blood_counts = data["Blood_Group"].value_counts()

plt.figure(figsize=(8, 5))

plt.bar(
    blood_counts.index,
    blood_counts.values,
    color=["black", "seagreen", "darkblue"]
)

plt.title("PATIENT BLOOD GROUP DISTRIBUTION")
plt.xlabel("Blood Group")
plt.ylabel("Number of Patients")

plt.show()


# ==========================================
# VISUALIZATION 4
# PATIENT CHOLESTEROL LEVELS
# ==========================================

x = data["Name"]
y = data["Cholesterol"]

plt.figure(figsize=(8, 5))

plt.bar(
    x,
    y,
    color=["black", "burlywood", "seagreen", "darkblue"]
)

plt.title("PATIENTS CHOLESTEROL LEVELS")
plt.xlabel("Patient Names")
plt.ylabel("Cholesterol Levels")

plt.show()
