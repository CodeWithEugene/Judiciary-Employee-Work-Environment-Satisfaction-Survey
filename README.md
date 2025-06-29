# Judiciary Employee Work Environment Satisfaction Survey Analysis 🌟

## Project Overview

This project focuses on the comprehensive preprocessing and initial analysis of a dataset derived from a "Judiciary Employee Work Environment Satisfaction Survey." The primary goal is to transform raw survey data into a clean, structured, and analysis-ready format, ensuring data quality, consistency, and adherence to ethical guidelines.

The dataset contains valuable insights into various aspects of the work environment, including:

- Job satisfaction
- Workload
- Training and professional development
- Remuneration and benefits
- Promotion and career progression
- Communication
- Performance management
- Work environment (office and equipment)
- Employee wellness
- Psychosocial support
- Sexual harassment

---

## ✨ Features

- **Data Loading & Initial Inspection:** Efficiently loads the dataset and provides a preliminary view of its structure.
- **Missing Value Handling:** Identifies and addresses missing data, including imputation for categorical and numerical columns, and dropping columns with excessive missingness.
- **Duplicate Removal:** Identifies and eliminates duplicate records to ensure data integrity.
- **Text Standardization:** Cleans and standardizes text-based columns by converting to lowercase, stripping whitespace, and normalizing internal spacing.
- **Logical Error Checks:** Identifies and reports inconsistencies in survey responses (e.g., age vs. experience, awareness vs. sensitization).
- **Categorical Variable Encoding:** Transforms categorical data into numerical formats suitable for analysis using:
    - Ordinal Encoding (e.g., Likert scales, age groups, education levels)
    - One-Hot Encoding (e.g., designation, court type, gender)
- **Date/Time Conversion:** Converts the 'Timestamp' column to a proper datetime format for temporal analysis.
- **Outlier Detection & Handling:** Visualizes numerical distributions and applies capping methods to manage outliers.
- **Ethical & Privacy Considerations:** Outlines critical aspects of data privacy, informed consent, anonymization, and compliance with the Data Protection Act.

---

## 🚀 Getting Started

### Prerequisites

To run this analysis, you'll need Python and the following libraries:

- pandas
- numpy
- matplotlib
- seaborn

Install them using pip:

```bash
pip install pandas numpy matplotlib seaborn
```

### Dataset

The project utilizes a CSV file named `Judiciary Employee Work Environment Satisfaction Survey.csv`. Please ensure this file is located in the specified path or update the loading path in the code.

### Usage

The analysis is structured as a series of sequential steps within a Python script or Jupyter Notebook. Each step addresses a specific data preprocessing or quality assurance task.

#### Load the dataset:

```python
import pandas as pd

df = pd.read_csv('C:/Users/USER/Documents/Eugenius/Projects/Judiciary Employee Work Environment Satisfaction Survey/Judiciary Employee Work Environment Satisfaction Survey.csv')
```

#### Perform Data Cleaning and Preprocessing

Follow the steps outlined in the analysis, including:

- Handling missing values
- Removing duplicate rows
- Standardizing text formatting
- Checking for and fixing logical errors
- Splitting multiple-response questions (if applicable)
- Encoding categorical variables
- Converting date/time fields
- Validating data quality and addressing outliers
- Cross-verifying responses for consistency

---

## 📊 Data Preprocessing Steps

1. **Handle Missing Data**
     - Categorical/Free Text: Imputed with the mode or a placeholder like 'No suggestion'.
     - Numerical: Converted to numeric (coercing errors) and imputed with the median.
     - High Missingness/Identifiers: Columns like 'Email Address', 'Column 43', and 'Column 44' were dropped.

2. **Remove Duplicates**
     - Duplicate rows were identified and removed.

3. **Standardize Text Formatting**
     - All object (text) columns, excluding 'Timestamp', were standardized by:
         - Converting to lowercase
         - Removing leading/trailing whitespace
         - Replacing multiple internal spaces with a single space

4. **Check for and Fix Logical Errors**
     - Inconsistencies identified (e.g., age vs. experience, awareness vs. sensitization).
     - No automatic corrections applied due to the sensitive nature of survey data.

5. **Split Multiple-Response Questions**
     - Checked for delimiters (`,`, `;`, `|`). No true multiple-response questions found.

6. **Encode Categorical Variables**
     - Ordinal Encoding: For ordered categories (e.g., tenure, age, Likert scales).
     - One-Hot Encoding: For nominal categories (e.g., designation, court type, gender).

7. **Convert Date/Time Fields**
     - 'Timestamp' column converted to datetime.

8. **Validate Data Quality and Address Outliers**
     - Outliers in numerical columns handled by capping at IQR-defined bounds.

9. **Cross-Verify Responses for Consistency**
     - Checked for logical consistency across related survey questions.

---

## 🔒 Ethical Considerations and Data Privacy

Data privacy and ethical considerations are paramount. This project adheres to principles guided by the Data Protection Act.

**Key Ethical Considerations:**

- Informed Consent: Assumed obtained from all participants.
- Data Anonymization: Direct identifiers removed.
- Avoiding Discriminatory Practices: Analysis avoids bias.
- Transparency: Clear about data usage and purpose.

**Compliance Steps:**

- Secure Storage
- Limiting Access
- Data Retention Policy
- Data Minimization
- Data Subject Rights

**Limitations and Assumptions:**

- No direct access to original data collection processes or consent forms.
- Assumed dataset is de-identified.
- General steps provided; comprehensive review may require more context.

---

## 🤝 Contributing

Contributions are welcome! If you have suggestions for improving the data preprocessing steps, analysis, or documentation, please open an issue or submit a pull request.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
