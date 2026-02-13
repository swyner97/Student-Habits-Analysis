# Student Habits vs Performance Analysis

**Author:** Sarah Wyner  
**Course:** DAT 301 - Project 2  
**Date:** October 1, 2025

## 📋 Table of Contents

- [Overview](#overview)
- [Research Question](#research-question)
- [Dataset](#dataset)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Analysis Components](#analysis-components)
- [Key Findings](#key-findings)
- [Visualizations](#visualizations)
- [Recommendations](#recommendations)
- [Future Work](#future-work)
- [License](#license)

## Overview

This project examines the relationship between student habits, lifestyle choices, and academic performance. By analyzing data from 1,000 undergraduate students aged 18-24, we identify key factors that influence exam scores and provide actionable insights for both students and educators.

## Research Question

**What factors influence student academic performance?**

This analysis explores various dimensions including:
- Study habits and time management
- Sleep patterns
- Exercise frequency
- Mental health status
- Attendance rates
- Screen time usage (social media and streaming)

## Dataset

**Source:** [Kaggle - Student Habits vs Academic Performance](https://www.kaggle.com/datasets/jayaantanaath/student-habits-vs-academic-performance)

**Specifications:**
- **Size:** 1,000 student records
- **Variables:** 16 original variables + 7 engineered features
- **Target Variable:** Exam Score (0-100)
- **Demographics:** Undergraduate students aged 18-24

### Original Variables
- `study_hours_per_day`
- `social_media_hours`
- `netflix_hours`
- `attendance_percentage`
- `sleep_hours`
- `exercise_frequency`
- `mental_health_rating`
- `exam_score`
- And more...

### Engineered Features
- `study_hours_category` - Categorized study time (Low/Medium/High/Very High)
- `attendance_category` - Categorized attendance (Low/Medium/Optimal)
- `sleep_group` - Sleep duration groups
- `exercise_group` - Exercise frequency groups
- `mental_health_group` - Mental health rating categories
- `total_screen_time` - Combined social media and streaming hours
- `performance_level` - Exam score categories (Below Average/Average/Good/Excellent)

## Features

### New Additions for Project 2 (Python Version)
1. **Correlation Analysis** - Comprehensive correlation matrix with heatmap visualization
2. **Multi-Factor Regression** - Statistical analysis of multiple predictors
3. **Interactive Filtering** - Performance-level based data exploration
4. **Advanced Statistical Tests** - Additional hypothesis testing
5. **Predictive Modeling** - Exploration of predictive capabilities

## 🔧 Requirements

```python
pandas >= 1.3.0
numpy >= 1.20.0
matplotlib >= 3.4.0
seaborn >= 0.11.0
scipy >= 1.7.0
```

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/swyner97/Student-Habits-Analysis/
cd Student-Habits-Analysis
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Ensure your data file is in the correct location:
```
project_root/
├── data/
│   └── student_habits_performance.csv
├── project2.ipynb
└── README.md
```

## Usage

### Running the Jupyter Notebook

1. Launch Jupyter Notebook:
```bash
jupyter notebook
```

2. Open `project2.ipynb`

3. Run all cells sequentially (Cell → Run All)

### Running as Python Script

If you prefer to run as a script:
```bash
python project2.py
```

### Expected Outputs

The analysis will generate:
- 7 high-resolution PNG visualizations
- Statistical analysis results printed to console
- Summary of key findings and recommendations

## Project Structure

```
project_root/
├── data/
│   └── student_habits_performance.csv
├── project2.ipynb                    # Main Jupyter notebook
├── project2.html                      # HTML export of notebook
├── project2.pdf                       # PDF export of analysis
├── README.md                          # This file
├── requirements.txt                   # Python dependencies
└── plots/                            # Generated visualizations
    ├── plot1_study_hours.png
    ├── plot2_attendance.png
    ├── plot3_screen_time.png
    ├── plot4_sleep.png
    ├── plot5_correlation.png
    ├── plot6_mental_health.png
    └── plot7_multi_factor.png
```

## 🔬 Analysis Components

### 1. Data Cleaning and Feature Engineering
- Created categorical variables for better grouping
- Handled missing values
- Generated derived features (e.g., total screen time)

### 2. Exploratory Data Analysis (EDA)
- **Study Hours Impact:** Clear positive correlation with exam scores
- **Attendance Analysis:** Optimal attendance (≥90%) shows benefits
- **Sleep Duration:** 7-8 hours appears optimal
- **Exercise Frequency:** Active students (4+ sessions/week) perform better
- **Mental Health:** Strong correlation with academic performance

### 3. Statistical Analysis
- Correlation matrix computation
- Group comparisons (mean, std, count)
- Screen time analysis for high vs. low performers

### 4. Data Visualization
Seven comprehensive visualizations:
1. Study hours vs. exam performance (scatter with trend line)
2. Attendance level impact (box plots)
3. Screen time breakdown (2D scatter with color-coded scores)
4. Sleep duration analysis (box plots)
5. Correlation heatmap (all numeric variables)
6. Mental health vs. scores (scatter with trend line)
7. Multi-factor summary (4-panel comparative visualization)

## Key Findings

### Top Correlations with Exam Score:
1. **Study Hours per Day:** 0.825 (very strong positive)
2. **Mental Health Rating:** 0.322 (moderate positive)
3. **Exercise Frequency:** 0.160 (weak positive)
4. **Sleep Hours:** 0.122 (weak positive)
5. **Attendance Percentage:** 0.090 (very weak positive)
6. **Social Media Hours:** -0.167 (weak negative)
7. **Netflix Hours:** -0.172 (weak negative)

### Performance by Category:

#### Study Hours
- **Very High (6+ hrs):** 97.8 average score
- **High (4-6 hrs):** 82.1 average score
- **Medium (2-4 hrs):** 66.0 average score
- **Low (0-2 hrs):** 47.5 average score

#### Mental Health
- **Good (8-10):** 76.4 average score
- **Fair (4-7):** 69.3 average score
- **Poor (1-3):** 63.4 average score
- **Difference:** 13.0 points between good and poor

#### Screen Time Patterns
- **High Performers (≥80):** 2.20 hrs social media, 1.61 hrs Netflix
- **Low Performers (<60):** 2.74 hrs social media, 2.05 hrs Netflix

## Recommendations

### For Students:
 **Study 4-6 hours daily** for optimal results  
 **Maintain 90%+ attendance** (critical for success)  
 **Prioritize mental health** - seek support when needed  
 **Get 7-8 hours of sleep** consistently  
 **Exercise 4+ times per week**  
 **Limit social media to <2 hours/day**  

### For Educators:
 **Emphasize attendance importance** in course policies  
 **Provide mental health resources** and support systems  
 **Promote healthy lifestyle habits** through wellness programs  
 **Monitor screen time impacts** on student performance  
 **Create supportive study environments** that encourage optimal study hours  

## Future Work

Potential extensions of this analysis:

1. **Predictive Modeling**
   - Build regression models to predict exam scores
   - Compare different algorithms (Linear, Random Forest, XGBoost)
   - Feature importance analysis

2. **Time Series Analysis**
   - Track habit changes over semester
   - Identify critical intervention points

3. **Clustering Analysis**
   - Identify student personas based on habits
   - Create targeted intervention strategies

4. **Causal Inference**
   - Establish causal relationships (not just correlations)
   - Control for confounding variables

5. **Interactive Dashboard**
   - Build Streamlit or Dash application
   - Allow real-time data exploration
   - Enable "what-if" scenario modeling

##  Contact

**Sarah Wyner**  
- Email: swyner97@gmail.com
- LinkedIn: https://www.linkedin.com/in/sarah-wyner
- GitHub: https://github.com/swyner97

## Acknowledgments

- Dataset provided by Kaggle user jayaantanaath
- Course: DAT 301 - Data Analysis
- Inspiration: Understanding factors that drive student success

---

**Note:** This analysis is for educational purposes as part of DAT 301 coursework. Results should be interpreted in the context of the specific dataset and may not generalize to all student populations.
