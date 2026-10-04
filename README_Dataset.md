# Dataset Academic Graph P5

Files:
- students.csv: 48 rows
- programs.csv: 3 rows
- courses.csv: 10 rows
- enrollments.csv: 122 rows (TAKES relationships)
- lecturers.csv: 4 rows
- teachings.csv: 10 rows (TEACHES relationships)

Expected graph counts after import:
- Student: 48
- Program: 3
- Course: 10
- Lecturer: 4
- TAKES: 122
- STUDIES_IN: 48
- TEACHES: 10

Main graph model:
- (:Student)-[:STUDIES_IN]->(:Program)
- (:Student)-[:TAKES {semester, grade, attendance}]->(:Course)
- (:Lecturer)-[:TEACHES]->(:Course)
