# Student Performance Analysis and Grouping

## Project Overview
This project analyzes student performance data to categorize students into groups based on their exam scores and preparation course completion. It also visualizes and compares the distribution between female and male students.

**Objective:** Understand patterns in student performance, identify high and low performers, and visualize differences between genders.

**Dataset:** Real student performance data including exam scores, demographic information, and prep course completion.

---

## Data Description
The dataset contains the following columns:

| Column | Description |
|--------|-------------|
| `gender` | Student gender (female/male) |
| `race/ethnicity` | Student's ethnic group |
| `parental level of education` | Parents' highest education level |
| `lunch` | Type of lunch (standard/free-reduced) |
| `test preparation course` | Whether the student completed a prep course (completed/none) |
| `math score` | Math exam score |
| `reading score` | Reading exam score |
| `writing score` | Writing exam score |

---

## Methodology

### 1. Grouping Students
Students were categorized into three performance groups based on their scores:

- **Group A (High Performers):** At least 2 scores ≥ 70  
- **Group B (Medium Performers):** At least 2 scores between 50 and 70  
- **Group C (Low Performers):** At least 2 scores ≤ 50  

**Ordering within groups:**
- Completed prep course students appear first, followed by None prep course students  
- Female students appear before male students  

---

### 2. Visualization

All plots are stored in the `plots` folder.  

1. **Female Students Distribution**  
   - Shows the percentage of female students in each group and prep course completion.  
   - File: `plots/female_grouped_distribution.png`  
   ![Female Students](plots/female_grouped_distribution.png)  

2. **Male Students Distribution**  
   - Shows the percentage of male students in each group and prep course completion.  
   - File: `plots/male_grouped_distribution.png`  
   ![Male Students](plots/male_grouped_distribution.png)  

3. **Comparison of Female vs Male Students**  
   - Stacked bar chart comparing percentages of female and male students by group and prep course.  
   - File: `plots/comparison_sorted_female_male.png`  
   ![Comparison](plots/comparison_sorted_female_male.png)  

**Colors:**  
- Completed Prep: Green shades  
- None Prep: Orange shades  

---

### 3. Insights

- **Group A:** Highest performing students, majority completed prep courses.  
- **Group B:** Medium performers, mix of completed and none prep students.  
- **Group C:** Lowest performers, identifies students who may need additional support.  
- **Gender differences:** Female students tend to have higher percentages in Completed prep within each group compared to males.  

These insights can help in targeting interventions and understanding performance patterns across genders.

---

## Tools and Libraries
- **Python 3.x**  
- **Pandas** (data manipulation)  
- **Matplotlib** (visualization)  
- **NumPy** (numerical operations)  

---

## How to Run
1. Clone this repository.  
2. Place the dataset `student_dropout_grouped_final_v2.csv` in the project folder.  
3. Run the Python script or Jupyter Notebook that generates the plots.  
4. All charts will be automatically saved in the `plots` folder.

---

## Files in this Project

| File | Description |
|------|-------------|
| `student_dropout_grouped_final_v2.csv` | The processed and grouped dataset |
| `data_exploration.ipynb` | Jupyter notebook containing all code, analysis, and plots |
| `plots/female_grouped_distribution.png` | Bar chart showing female student distribution by group and prep |
| `plots/male_grouped_distribution.png` | Bar chart showing male student distribution by group and prep |
| `plots/comparison_sorted_female_male.png` | Combined chart comparing female and male students by group and prep |

---

**Note:**  
This project sets a strong foundation for predictive modeling (machine learning) on student performance in the next steps.
