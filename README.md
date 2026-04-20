# 🎓 Student Habits & Academic Performance Analysis

> An end-to-end data analysis project exploring how student lifestyle habits impact exam scores — powered by SQL, Python, Excel, and Power BI.

---

## 📁 Project Structure

```
├── student_habits_performance.csv       # Raw dataset (1,000 students, 16 features)
├── Main_Data_Student_Habits_Performance.csv  # Cleaned/transformed dataset
├── sql_student_habits_performance.sql   # SQL aggregation & segmentation queries
├── student_habits_performance_Bi_P.pbix # Power BI dashboard
└── README.md
```

---

## 📊 Dataset Overview

| Feature | Description |
|---|---|
| `study_hours_per_day` | Daily hours dedicated to studying |
| `sleep_hours` | Nightly sleep duration |
| `attendance_percentage` | Class attendance rate |
| `social_media_hours` | Daily social media usage |
| `netflix_hours` | Daily streaming consumption |
| `exercise_frequency` | Weekly exercise sessions |
| `mental_health_rating` | Self-reported mental health (1–10) |
| `diet_quality` | Poor / Fair / Good |
| `part_time_job` | Yes / No |
| `extracurricular_participation` | Yes / No |
| `parental_education_level` | None / High School / Bachelor / Master |
| `exam_score` | Final exam score (target variable) |

- **1,000 students** | **16 variables** | Ages 17–24

---

## 🔍 Key Insights

### 1. Study Hours is the Dominant Driver
Study hours per day has a **0.83 correlation** with exam score — by far the strongest predictor in the dataset. Top performers (score ≥ 90) averaged **5.6 hrs/day** of study vs. **1.6 hrs/day** for bottom performers (score < 50). No other single factor comes close to this impact.

### 2. Mental Health Matters More Than Sleep
Mental health rating (self-reported, 1–10) correlates at **0.32** with exam score — the second strongest predictor. Sleep hours correlate at only **0.12**, suggesting that *quality of wellbeing* outweighs raw sleep quantity when it comes to academic performance.

### 3. Social Media & Netflix Are the Silent Killers
Both show **negative correlations** with exam score:
- Social media: **−0.17**
- Netflix: **−0.17**

Not catastrophic in isolation, but combined with low study hours, they consistently appear in the profiles of low-performing students.

### 4. Attendance Has Surprisingly Low Direct Impact
Attendance correlates at only **0.09** with exam score. Top scorers averaged **86.8% attendance** while bottom scorers averaged **83.3%** — nearly identical. This suggests attendance alone doesn't drive performance without the study habit to back it up.

### 5. Parental Education Shows No Clear Advantage
Students with parents holding a **Master's degree** actually averaged slightly *lower* scores (68.1) than those with **Bachelor-educated parents** (70.3) or **High School-educated parents** (69.6). Parental education level is not a reliable predictor of student performance in this dataset.

### 6. Part-Time Jobs Have Minimal Effect
Students with part-time jobs scored **68.7** on average vs. **69.8** for those without — a negligible difference. Having a job doesn't significantly hurt academic performance.

### 7. Extracurricular Participation is Neutral
Participation vs. non-participation: **69.6 vs. 69.6**. Virtually no difference. Extracurricular activities neither help nor hurt exam scores on average.

### 8. Gender Has No Performance Gap
Female: **69.7** | Male: **69.4** | Other: **70.7** — the dataset shows no meaningful gender-based performance gap.

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|---|---|
| **MySQL** | Data segmentation, group-by aggregations, CASE bucketing |
| **Excel / Power Query** | Data cleaning, Star Schema modeling, Pivot Tables |
| **Power BI** | Interactive dashboard with slicers and drill-through |
| **Python (pandas)** | Correlation analysis, descriptive statistics |

---

## 📐 SQL Approach

The SQL query segments students into behavioral groups using `CASE` statements across 4 dimensions:

- **Exercise frequency**: 0–2 / 2–4 / >4 sessions/week
- **Attendance**: 0–66% / 66–76% / 76–86% / >86%
- **Study hours**: 0–2 / 2–4 / 4–6 / >6 hrs/day
- **Sleep hours**: 0–5 / 5–8 / >8 hrs/night

Then aggregates avg exam score, student count, and all numeric KPIs per group — enabling multi-dimensional habit profiling.

---

## 📈 Power BI Dashboard

The `.pbix` file includes:
- KPI cards: Avg Exam Score, Avg Study Hours, Avg Sleep, Avg Attendance
- Score distribution histogram
- Correlation breakdown by habit category
- Slicers: Gender, Diet Quality, Parental Education, Part-Time Job, Extracurricular

---

## 💡 Conclusion

The data tells a clear story: **study time and mental health are what separate top students from the rest**. Structural factors like gender, parental education, and extracurricular involvement have little to no effect. The biggest risks to performance are low study hours combined with high passive screen time (social media + Netflix).

---

## 👤 Author

**Ahmed Haytham**  
Business Information Systems | Helwan University  
Data Analysis Track — Digital Egypt Pioneers Initiative (DEPI)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com)
[![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black)](https://github.com)
