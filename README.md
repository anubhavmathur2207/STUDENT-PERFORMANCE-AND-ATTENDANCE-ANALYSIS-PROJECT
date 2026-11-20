# Student Performance and Attendance Analysis

## 1. Project Overview

The **Student Performance and Attendance Analysis** project is a Python-based data analysis project that analyzes the academic performance and attendance records of 2,500 students.

The project uses **Python, Pandas, NumPy, and CSV files** to generate student data, perform calculations, analyze academic results, and display useful information.

It helps understand how data analysis can be used to evaluate student performance, attendance, and branch-wise academic results.

The dataset is generated automatically using Python, so there is no need to enter 2,500 student records manually.

---

## 2. Project Objectives

The main objectives of this project are:

- Generate a dataset containing 2,500 student records.
- Store student information in a CSV file.
- Calculate average, highest, and lowest marks.
- Analyze student attendance.
- Identify passed and failed students.
- Check attendance eligibility.
- Find the top 10 performing students.
- Identify students with attendance below 75%.
- Compare academic performance across different branches.
- Categorize students according to their marks.
- Export the final analysis into a CSV file.

---

## 3. Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Pandas | Data handling and analysis |
| NumPy | Numerical calculations and data generation |
| CSV | Storing student records |

### Libraries Used

**1. Pandas**

Pandas is used to create DataFrames, read CSV files, filter records, group students by branch, and perform data analysis.

**2. NumPy**

NumPy is used to generate random student data, calculate numerical values, and apply conditions using functions such as `np.where()` and `np.select()`.

**3. CSV**

CSV stands for Comma-Separated Values. It is used to store student information in a tabular format.

---

## 4. Dataset Information

The project automatically generates a dataset containing **2,500 student records**.

Each student record contains the following information:

| Column | Description |
|---|---|
| Roll_No | Unique roll number of each student |
| Name | Generated student name |
| Branch | Student's engineering branch |
| Marks | Marks obtained by the student |
| Attendance | Attendance percentage |

### Branches Included

- CSE – Computer Science and Engineering
- ECE – Electronics and Communication Engineering
- IT – Information Technology
- ME – Mechanical Engineering
- CE – Civil Engineering

### Data Generation

The project uses NumPy to generate sample data:

- Roll numbers start from 1001.
- Student names are generated automatically.
- Branches are selected randomly.
- Marks are generated between 20 and 100.
- Attendance is generated between 40% and 100%.

A random seed of 42 is used so that the generated dataset remains reproducible when the code is run again.

**Note:** This project uses randomly generated sample data, not actual college student records.

---

## 5. Project Features and Working

### 1. Automatic Dataset Generation

The program generates records for 2,500 students using NumPy and stores them in a Pandas DataFrame.

### 2. CSV File Creation

The generated dataset is saved as:

`students.csv`

The CSV file contains all the original student records.

### 3. Dataset Information

The program displays:

- Total number of students.
- Total number of columns.
- Number of different branches.

### 4. Student Record Display

The `head()` function displays the first 10 student records.

This helps us understand the structure of the dataset.

### 5. Performance Analysis

The program calculates:

- Average marks.
- Highest marks.
- Lowest marks.

NumPy functions such as `np.mean()`, `np.max()`, and `np.min()` are used.

### 6. Attendance Analysis

The program calculates:

- Average attendance.
- Highest attendance.
- Lowest attendance.

This helps evaluate the overall attendance level of students.

### 7. Pass and Fail Analysis

Students scoring 40 or more marks are classified as **Pass**.

Students scoring below 40 marks are classified as **Fail**.

The program also calculates the overall pass percentage.

### 8. Attendance Eligibility

Students with attendance of 75% or more are classified as **Eligible**.

Students with attendance below 75% are classified as **Short Attendance**.

This is an assumed project rule and may differ from actual college policies.

### 9. Top 10 Performers

The program identifies the 10 students with the highest marks using:

`df.nlargest(10, "Marks")`

It displays their roll numbers, names, branches, and marks.

### 10. Low Attendance Analysis

The program filters students whose attendance is below 75%.

It displays the total number of such students and shows the first 10 matching records.

### 11. Branch-Wise Performance Analysis

The program groups students according to their branches using `groupby()`.

For each branch, it calculates:

- Total number of students.
- Average marks.
- Average attendance.

This makes it easier to compare the performance of different branches.

### 12. Performance Categories

Students are divided into five categories based on their marks:

| Marks | Performance |
|---|---|
| 85–100 | Excellent |
| 70–84 | Very Good |
| 50–69 | Good |
| 40–49 | Average |
| Below 40 | Poor |

The `np.select()` function is used to assign these categories automatically.

### 13. Final Analysis Export

After completing the analysis, the program saves the final dataset with additional columns:

- Result
- Attendance_Status
- Performance

The final file is saved as:

`student_analysis.csv`

---

## 6. Project Folder Structure

After running the program, your folder will look like this:

```text
Student_Performance_Analysis/
│
├── main.py
│
├── students.csv
│
├── student_analysis.csv
│
└── README.md
```

**File descriptions:**

- `main.py` – Main Python program containing the complete project code.
- `students.csv` – Original dataset of 2,500 students.
- `student_analysis.csv` – Final dataset containing the analysis results.
- `README.md` – Project documentation.

The two CSV files are automatically generated when the Python program runs.

---

## 7. Installation and Requirements

### Step 1: Install Python

Download and install Python from:

https://www.python.org/downloads/

### Step 2: Install Required Libraries

Open Command Prompt and execute:

```bash
py -m pip install pandas numpy
```

### Step 3: Open Python IDLE

1. Open Python IDLE.
2. Create a new file.
3. Paste the project code.
4. Save the file as `main.py`.

### Step 4: Run the Project

Press **F5** or select:

`Run → Run Module`

The program will execute and generate the CSV files automatically.

---

## 8. Expected Output

When the program runs successfully, it displays:

- Project title.
- Dataset information.
- First 10 student records.
- Average, highest, and lowest marks.
- Attendance statistics.
- Pass and fail counts.
- Attendance eligibility.
- Top 10 performers.
- Low attendance records.
- Branch-wise performance.
- Performance category counts.
- Final project summary.

At the end, the program displays:

```text
PROJECT COMPLETED SUCCESSFULLY!
```

The generated CSV files can be opened using Microsoft Excel or any spreadsheet application.

---

## 9. Important Python Concepts Used

This project demonstrates the following Python concepts:

| Concept | Application |
|---|---|
| Variables | Storing values |
| Lists | Storing generated student names |
| Dictionaries | Creating the dataset |
| For Loops / List Comprehension | Generating student names |
| Functions | Using built-in library functions |
| NumPy Arrays | Generating numerical data |
| Pandas DataFrame | Managing student records |
| Conditional Statements | Classifying students |
| Filtering | Finding low attendance students |
| GroupBy | Branch-wise analysis |
| CSV Handling | Saving and reading datasets |

### Important Functions Used

```python
np.arange()
np.random.seed()
np.random.choice()
np.random.randint()
np.mean()
np.max()
np.min()
np.where()
np.select()
pd.DataFrame()
pd.read_csv()
df.to_csv()
df.head()
df.nlargest()
df.groupby()
df.value_counts()
```

---

## 10. Advantages of the Project

- Handles a large dataset of 2,500 records.
- Reduces manual calculations.
- Automatically generates student data.
- Provides quick academic performance analysis.
- Helps identify students with low attendance.
- Makes branch-wise comparison easier.
- Saves analysis results for future use.
- Demonstrates practical applications of Python and data analysis.

---

## 11. Limitations

- The dataset contains randomly generated sample records.
- It does not use a real college database.
- It does not have a graphical user interface.
- It does not automatically update student information.
- The attendance and passing criteria are predefined project assumptions.

---

## 12. Future Improvements

The project can be improved by adding:

- A graphical user interface using Tkinter.
- Charts and graphs using Matplotlib.
- A real student database.
- Student search functionality.
- Individual student reports.
- Subject-wise marks analysis.
- Automatic identification of at-risk students.

---

## 13. Conclusion

The **Student Performance and Attendance Analysis** project demonstrates how Python can be used to manage and analyze student information.

By using Pandas and NumPy, the project generates a dataset of 2,500 students and performs several useful operations, including marks analysis, attendance analysis, pass/fail classification, top performer identification, and branch-wise comparison.

This project helped develop practical knowledge of Python programming, data handling, numerical operations, and CSV file management.

It is a beginner-friendly project that demonstrates the fundamentals of data analysis using Python.

---

## 14. Author

**Project Name:** Student Performance and Attendance Analysis  
**Language:** Python  
**Libraries:** Pandas and NumPy  
**Dataset Size:** 2,500 Student Records  
**IDE:** Python IDLE  

**Developed as a Python academic project.**
