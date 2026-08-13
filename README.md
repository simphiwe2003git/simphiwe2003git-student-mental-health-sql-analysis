

## Project Overview

This project explores the relationship between the length of stay in a foreign country and the mental health outcomes of international university students. Using SQL, the analysis investigates whether the duration of stay is associated with depression, social connectedness, and acculturative stress among international students.

The project was completed as part of a DataCamp SQL project and demonstrates practical SQL skills including filtering, aggregation, grouping, sorting, and data analysis.


## Business Problem

International students often experience challenges when adapting to a new country. Universities and researchers need data-driven insights into how the length of stay may influence students' mental health to better design support programmes and interventions.

This project analyzes survey data to identify patterns between the duration of stay and three important psychological assessment scores.


## Project Objectives

The objective of this analysis was to:

- Filter the dataset to include only international students.
- Group students according to their length of stay.
- Calculate the average depression score (PHQ-9).
- Calculate the average social connectedness score (SCS).
- Calculate the average acculturative stress score (ASISS).
- Count the number of international students in each stay category.
- Present the results in descending order of length of stay.


## Dataset

The dataset contains survey responses collected from university students and includes demographic information together with standardized mental health assessment scores.

The analysis specifically focuses on:

- International students (`inter_dom = 'Inter'`)
- Length of stay (`stay`)
- PHQ-9 Depression Score (`todep`)
- Social Connectedness Scale (`tosc`)
- Acculturative Stress Scale (`toas`)

Dataset location:

data/student_mental_health.csv

## Technologies Used

- SQL
- PostgreSQL
- DataCamp Workspace
- Git
- GitHub

## SQL Concepts Demonstrated

This project demonstrates:

- SELECT
- WHERE
- COUNT()
- AVG()
- ROUND()
- GROUP BY
- ORDER BY
- Aliasing
- Aggregate Functions

## Final SQL Query

`sql
SELECT
    stay,
    COUNT(inter_dom) AS count_int,
    ROUND(AVG(todep), 2) AS average_phq,
    ROUND(AVG(tosc), 2) AS average_scs,
    ROUND(AVG(toas), 2) AS average_as
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC;


## Results

The analysis produced a table containing:

- Length of stay
- Number of international students
- Average depression score
- Average social connectedness score
- Average acculturative stress score

The results suggest that the duration of stay may be associated with differences in mental health outcomes among international students.

## Repository Structure

```
student-mental-health-sql-analysis/
│
├── README.md
├── data/
│   └── student_mental_health.csv
├── sql/
│   └── analysis.sql
├── images/
│   ├── sql_query.png
│   └── results_table.png
```

---

## How to Run

1. Download the dataset from the `data` folder.
2. Import the CSV into your SQL environment.
3. Execute the SQL query found in `sql/analysis.sql`.
4. Compare your output with the results shown in the repository.


## Future Improvements

Possible future enhancements include:

- Data visualization using Power BI or Tableau
- Statistical hypothesis testing
- Correlation analysis
- Predictive modelling using Python
- Interactive dashboards


## Author

**Simphiwe Mkhwanazi**

IT Honours Student | Data Analytics | Cloud Computing | Software Development
