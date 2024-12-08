# Annotation File Analysis and Processing

## Overview
This project focuses on analyzing annotation files by organizing, counting, and filtering based on specific criteria. The aim is to explore the dataset in depth by grouping annotations by month, examining specific timeframes, and deriving key statistical insights.

---

## Tasks Summary
The project is divided into three key tasks:

1. Count annotations by month and year, and identify the month with the highest number of annotations.
2. Create a dictionary that groups annotations by month and save the results in JSON and Pickle formats.
3. Filter and display annotations from the second half of 2024 in chronological order.

---

## Task 1: Count Annotations by Month and Year

### **Objective**
Analyze the number of annotations grouped by month and year, and identify the month with the most annotations.

### **Steps**
1. **Import Required Libraries**: Use `os`, `glob`, `re`, and `datetime` for file handling and metadata extraction.
2. **Extract Metadata**: Apply regex to extract the `year` and `month` from annotation filenames.
3. **Group by Month**: Use a nested dictionary to count annotations for each month.
4. **Identify Peak Month**: Utilize the `max()` function to determine the month with the highest number of annotations.
5. **Display Results**: Generate a structured report summarizing:
   - Total files processed.
   - Monthly annotation counts.
   - The peak month.

### **Outcome**
A detailed report showing annotation counts by month and highlighting the month with the highest activity.

#### **Example Output**
```
======================================================================
Annotation Analysis Report
Total files in folder: 206
Total annotation files processed: 206
Annotations per year and month:
Year: 2024, Month: 01, Annotations: 27
Year: 2024, Month: 06, Annotations: 52
Month with the most annotations: Year 2024, Month 06 with 52 annotations
======================================================================
```

---

## Task 2: Group Annotations by Month and Save to JSON/Pickle

### **Objective**
Create a dictionary where each key represents a month, and each value contains a list of annotation filenames for that month. Save this dictionary in both JSON and Pickle formats.

### **Steps**
1. **Extract Metadata**:
   - Use regex to parse `date` and `time` from annotation filenames.
   - Convert metadata into `datetime` objects.
2. **Group by Month**:
   - Organize annotation filenames into a dictionary keyed by their month of creation.
3. **Save Data**:
   - Save the dictionary as a JSON file using `json.dump()`.
   - Save the same dictionary as a Pickle file using `pickle.dump()`.
4. **Load and Verify**:
   - Load the JSON file and print its contents to confirm correctness.

### **Outcome**
Two output files containing grouped annotations:
- `annotations_by_month.json`
- `annotations_by_month.pkl`

#### **Example Output**
```
======================================================================
Annotation Processing Report
Total annotation files processed: 206
Data successfully saved in:
- JSON file: annotations_by_month.json
- Pickle file: annotations_by_month.pkl
Loaded Data from JSON:
{
    "1": [
        "20240102_185527_SN27_QUICKVIEW_VISUAL_1_1_10_SATL-2KM-11N_740_3850.txt",
        "20240116_192856_SN24_QUICKVIEW_VISUAL_1_1_10_SATL-2KM-10N_552_4164.txt"
    ]
}
======================================================================
```

---

## Task 3: Filter and Display Annotations from the Second Half of 2024

### **Objective**
Filter annotation files from July to December 2024 and display them in chronological order.

### **Steps**
1. **Extract Metadata**:
   - Use regex to parse `date` and `time` from filenames.
   - Convert to `datetime` objects.
2. **Filter by Date**:
   - Filter annotations for dates between July and December 2024.
3. **Display Results**:
   - Print filenames and corresponding datetimes for matching annotations.
   - Sort and display them in chronological order.

### **Outcome**
A list of annotations from the specified period, or a message indicating no matches found.

#### **Example Output**
```
======================================================================
Annotations from the Second Half of 2024
No matching annotations found for the specified period.
======================================================================
```

---

## Prerequisites

- **Python Version**: Python 3.8+
- **Required Libraries**:
  - `os`, `glob`, `re`, `json`, `pickle`, `datetime`
- **Installation**:
  Install any missing libraries with the following command:
  ```bash
  pip install -r requirements.txt
  ```

---

## Conclusion

This project offers a comprehensive analysis of annotation files, focusing on organized reporting, efficient grouping, and time-based filtering. The modular design of the scripts ensures adaptability for similar datasets and workflows.

---
