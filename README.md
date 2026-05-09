# Employee Resource Management: End-to-End Data Science Project

This repository documents a 6-phase data science journey, transforming a raw, "dirty" employee dataset into a predictive tool for organizational decision-making.

---

## 🚀 Project Roadmap
- [x] **Phase 1:** Data Immersion & Wrangling
- [x] **Phase 2:** Exploratory Data Analysis (EDA)
- [x] **Phase 3:** Interactive Dashboarding (Power BI)
- [x] **Phase 4:** Statistical Validation & Storytelling
- [x] **Phase 5:** Machine Learning & Predictive Modeling
- [ ] **Phase 6:** Final Portfolio Synthesis (Upcoming)

---

## 🛠️ Phase 1: Data Immersion & Wrangling
**Objective:** Transform raw, survey-style Excel data into a clean, analysis-ready CSV.
- **Key Actions:** - Standardized verbose headers (e.g., "Please enter your Dell Email ID" → `Dell_Email`).
  - Fixed categorical typos (Corrected "Anyalst" to "Analyst").
  - **Feature Engineering:** Created `Total_Compensation` (Salary + Bonus).
- **Deliverable:** `cleaned_employee_data.csv`

---

## 📊 Phase 2: Exploratory Data Analysis (EDA)
**Objective:** Identify patterns and distributions using Python visualizations.
- **Tools:** Matplotlib, Seaborn.
- **Key Insights:**
  - Identified salary cost centers across different Teams.
  - Visualized gender distribution across Job Levels to check for organizational balance.
  - Analyzed the correlation between attendance and bonus payouts.

---

## 📈 Phase 3: Interactive Dashboarding
**Objective:** Transition from static code to a "Single Source of Truth" for stakeholders.
- **Tools:** Power BI Desktop, DAX.
- **Features:** - Executive KPI cards for Headcount, Total Spend, and Avg Bonus.
  - Dynamic slicers for Team-based and Manager-based filtering.
  - Pay parity visuals by Job Level and Gender.

---

## 🔬 Phase 4: Statistical Validation
**Objective:** Use scientific methods to validate observations from the EDA phase.
- **Method:** Independent T-Test (comparing Bonus based on Attendance).
- **Findings:** - **P-Value:** 0.9620
  - **Conclusion:** Failed to reject the Null Hypothesis. There is no statistically significant evidence that attendance drives bonus amounts in this dataset, suggesting a shift toward performance-based incentives.

---

## 🤖 Phase 5: Predictive Modeling
**Objective:** Move from descriptive analytics to predictive foresight.
- **Model:** Linear Regression (Scikit-Learn).
- **Process:** - One-Hot Encoding for categorical variables (`Job_Level`, `Team`).
  - Train-Test split (80/20) for model validation.
- **Performance:** - Evaluation Metrics: Mean Absolute Error (MAE) and R-Squared.
  - The model effectively predicts `Salary` based on organizational features.

---

## 📖 Data Dictionary
| Column Name | Description | Data Type | 
| :--- | :--- | :--- | 
| `Employee_ID` | Unique identifier | Integer |
| `Job_Level` | Employee rank (Cleaned) | Categorical |
| `Total_Compensation` | Salary + Bonus (Engineered) | Float |
| `Attendance` | Presence status | Categorical |
| `Team` | Department/Group assignment | Categorical |

---

## 📂 Repository Structure
- `/data`: Raw and Cleaned datasets.

- ## 🏁 Phase 6: Project Synthesis & Key Learnings
**Project Conclusion:** This end-to-end project successfully navigated the journey from raw data to predictive experimentation. 

**Top 3 Takeaways:**
1. **Data Quality is King:** The most significant impact on the project was the initial wrangling phase where 18 messy columns were standardized into a clean schema.
2. **Statistics > Visuals:** While EDA showed a "visual" difference in bonuses, the T-test (P=0.96) proved it wasn't statistically significant, preventing a false business conclusion.
3. **Data Volume Matters:** The predictive model (Phase 5) highlighted that Machine Learning requires a larger volume of data to find reliable patterns in compensation.

**Final Status:** Project Completed successfully.
- `/scripts`: Python notebooks for cleaning, EDA, and ML.
- `/visuals`: Exported charts and Dashboard screenshots.
- `/docs`: Final Presentation Deck (PPT).
