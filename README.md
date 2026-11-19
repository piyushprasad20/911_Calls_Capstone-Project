# 911_Calls_Capstone-Project


Exploratory data analysis (EDA) of emergency 911 call records in Python using `numpy`, `pandas`, `matplotlib`, and `seaborn`.

## Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Key Analyses & Visualizations](#key-analyses--visualizations)
- [Setup & Installation](#setup--installation)
- [Usage](#usage)
- [Notes](#notes)

---

## Overview
A 911 call center—also known as a Public Safety Answering Point (PSAP)—is a facility where trained telecommunicators answer emergency calls, gather critical information, and dispatch police, fire, or medical responders.
These centers operate 24/7 and use systems like computer‑aided dispatch (CAD) and radio networks to coordinate emergency services.

---

## Project Structure

```text
911_Calls_Capstone-Project/
├── 911_Calls_Data_Capstone_Project.ipynb   # Main analysis and visualization notebook
└── README.md                               # Project documentation
```

---

## Dataset

This capstone workflow typically uses a CSV dataset of 911 call records (commonly `911.csv`) containing fields such as:

- `lat` / `lng` — Latitude and longitude of the call
- `desc` — Description of the emergency call
- `zip` — Postal/ZIP code
- `title` — Incident title (often prefixed with the call category, such as `EMS: ...`, `Fire: ...`, or `Traffic: ...`)
- `timeStamp` — Date and time of the call (`YYYY-MM-DD HH:MM:SS`)
- `twp` — Township
- `addr` — Street address
- `e` — Dummy indicator variable

> **Note:** Update the file path in `911_Calls_Data_Capstone_Project.ipynb` if your dataset is stored in a subfolder or loaded from an external URL.

---

## Key Analyses & Visualizations

Typical exploratory steps covered in a 911 Calls capstone notebook include:

- **Top Zip Codes & Townships:** Identifying the highest-frequency ZIP codes and townships (`value_counts()`).
- **Emergency Reasons (`Reason` feature):** Extracting primary categories (`EMS`, `Fire`, `Traffic`) from the `title` column and comparing counts across categories.
- **Temporal Breakdown:** Parsing `timeStamp` into `Hour`, `Day of Week`, and `Month` features.
- **Count & Heat Visualizations:**
  - Call counts by day of week and month grouped by emergency reason (`EMS`, `Fire`, `Traffic`).
  - Heatmaps and clustermaps showing call volume across days of the week, hours of the day, and months.

---

## Setup & Installation

1. **Clone the repository:**

   ```bash
   git clone [https://github.com/piyushprasad20/911_Calls_Capstone-Project.git](https://github.com/piyushprasad20/911_Calls_Capstone-Project.git)
   cd 911_Calls_Capstone-Project
   ```

2. **Install required Python libraries:**

   ```bash
   pip install numpy pandas matplotlib seaborn jupyter
   ```

---

## Usage

1. Place your 911 dataset CSV in the expected working directory (or update the `pd.read_csv(...)` path in the notebook).
2. Launch Jupyter or open the notebook in VS Code / Google Colab:

   ```bash
   jupyter notebook 911_Calls_Data_Capstone_Project.ipynb
   ```

3. Run the cells sequentially from top to bottom to inspect data summaries, engineered features, and plots.

---

## Notes

- If you add custom findings, summary statistics, or additional feature engineering steps to `911_Calls_Data_Capstone_Project.ipynb`, update the **Key Analyses & Visualizations** and **Dataset** sections above so the documentation stays aligned with your notebook.
