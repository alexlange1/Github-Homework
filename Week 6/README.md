# Data Analysis: Netflix and Titanic Datasets

This project dives into an in-depth analysis of two datasets: Netflix and Titanic. Using Python and libraries like Pandas, Seaborn, and Matplotlib, key insights were extracted through a series of exploratory tasks. Below is a summary of the objectives, methodologies, and outcomes for each analysis.

---

## Table of Contents
1. Overview  
2. Dataset Details  
3. Netflix Analysis  
   - Task 1: Handling Missing Ratings  
   - Task 2: Counting 2021 Films by Country  
   - Task 3: Movies from 2020 with Complete Data  
   - Task 4: Identifying the Year with Most Releases  
   - Task 5: Average Releases Since 2010  
4. Titanic Analysis  
   - Task 1: Survival Percentage by Gender  
   - Task 2: Survival by Gender and Passenger Class  
5. Instructions for Use  
6. Key Takeaways  
7. Future Enhancements  

---

## 1. Overview

This project aims to utilize Python's data manipulation and visualization tools to uncover insights from the Netflix and Titanic datasets. The exercises focus on enhancing familiarity with data cleaning, transformation, and visualization techniques while interpreting real-world data.

---

## 2. Dataset Details

### Netflix Dataset
The Netflix dataset includes the following attributes:

- **Title**: Name of the movie or TV show.  
- **Type**: Specifies if it is a Movie or TV Show.  
- **Release Year**: Year the title was released.  
- **Country**: Country of production.  
- **Rating**: Maturity rating of the title.  

### Titanic Dataset
The Titanic dataset contains details about passengers, including:

- **Gender**: Male or Female.  
- **Passenger Class**: Travel class (1st, 2nd, 3rd).  
- **Survival Status**: Whether the passenger survived or not.  

---

## 3. Netflix Analysis

### **Task 1: Handling Missing Ratings**
**Objective**: Count the number of missing values in the `rating` column.  
**Method**:  
- Use `isnull()` and `sum()` to count missing entries.  
**Output**: Total missing ratings: **4**

---

### **Task 2: Counting 2021 Films by Country**
**Objective**: Determine how many movies were released in 2021 for a specific country (e.g., Spain).  
**Method**:  
- Filter the dataset for `type='Movie'` and `release_year=2021`.  
- Group results by the `country` column.  
**Output**: Total movies from Spain in 2021: **6**

---

### **Task 3: Movies from 2020 with Complete Data**
**Objective**: Count the number of movies released in 2020 with no missing values.  
**Method**:  
- Filter for `type='Movie'` and `release_year=2020`.  
- Use `dropna()` to remove incomplete records.  
**Output**: Number of complete movies: **409**

---

### **Task 4: Identifying the Year with Most Releases**
**Objective**: Find the year with