# Medical Data Visualizer

A data analysis and visualization project built with Python as part of the [freeCodeCamp Data Analysis with Python](https://www.freecodecamp.org/learn/data-analysis-with-python/) certification.

## Project Overview

This project visualizes and analyzes medical examination data using **matplotlib**, **seaborn**, and **pandas**. The dataset contains patient information including body measurements, blood test results, and lifestyle choices, which are used to explore the relationship between cardiac disease and various health factors.

## Dataset

**File:** `medical_examination.csv`  
**Size:** 70,000 patient records

| Feature | Variable | Type |
|---|---|---|
| Age | `age` | int (days) |
| Height | `height` | int (cm) |
| Weight | `weight` | float (kg) |
| Gender | `gender` | categorical |
| Systolic blood pressure | `ap_hi` | int |
| Diastolic blood pressure | `ap_lo` | int |
| Cholesterol | `cholesterol` | 1: normal, 2: above normal, 3: well above normal |
| Glucose | `gluc` | 1: normal, 2: above normal, 3: well above normal |
| Smoking | `smoke` | binary |
| Alcohol intake | `alco` | binary |
| Physical activity | `active` | binary |
| Cardiovascular disease | `cardio` | binary |

## Visualizations

### 1. Categorical Plot (`catplot.png`)
Bar chart showing the counts of good and bad outcomes for `cholesterol`, `gluc`, `smoke`, `alco`, `active`, and `overweight` variables, split by patients with and without cardiovascular disease (`cardio = 0` and `cardio = 1`).

### 2. Heat Map (`heatmap.png`)
Correlation matrix showing relationships between all variables in the cleaned dataset. Notable correlations:
- `weight` & `overweight`: **0.7** (strongest)
- `cholesterol` & `gluc`: **0.4**
- `cardio` & `cholesterol`: **0.3**
- `smoke` & `alco`: **0.3**

## Key Findings

- Overall cardiovascular disease prevalence: **50%** (34,979 cases)
- **62.2%** of patients are classified as overweight
- Elevated cholesterol found in **25.2%** of the population
- Average blood pressure: **129/97 mmHg**

## Files

```
Medical Data Visualizer/
├── medical_examination.csv   # Dataset
├── medical_data_visualizer.py # Main solution file
├── main.py                   # Run and test script
├── test_module.py            # Unit tests
├── catplot.png               # Generated categorical plot
├── heatmap.png               # Generated heat map
└── README.md
```

## How to Run

### Prerequisites
```bash
pip install pandas matplotlib seaborn numpy
```

### Run
```bash
python main.py
```

This will:
1. Generate `catplot.png` and `heatmap.png`
2. Run all unit tests and display results in the terminal

## Technologies Used

- **Python 3**
- **Pandas** — data manipulation and analysis
- **Matplotlib** — figure and plot rendering
- **Seaborn** — statistical data visualization
- **NumPy** — numerical operations

## Certificate

This project is part of the **Data Analysis with Python** certification on [freeCodeCamp](https://www.freecodecamp.org/).
