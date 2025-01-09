# F-Test Calculator Documentation

## Overview

The **F-Test Calculator** is a web application designed to assist users in performing F-tests, which are statistical tests used to compare variances between two datasets. The application allows users to upload datasets in CSV format, define null and alternate hypotheses, select a significance level, and calculate the F-value. Results include the calculated F-value, degrees of freedom, critical value, and a conclusion based on the test results.

## Features

1. **Dataset Upload**: Users can upload datasets in CSV format.
2. **Hypothesis Definition**: Input fields for null and alternate hypotheses.
3. **Significance Level Selection**: Dropdown menu to select the significance level (0.01, 0.05, 0.10).
4. **F-Value Calculation**: Compute the F-value and display results, including critical value and conclusion.
5. **Interactive Design**: Includes loaders, animations, and a responsive interface.

## Technologies Used

- **HTML**: For structure and layout.
- **CSS (TailwindCSS)**: For styling and responsiveness.
- **JavaScript**: For functionality and calculations.
- **CSV Parsing Library**: For handling uploaded datasets.
- **F-Distribution Table**: Embedded for critical value lookup.

---

## File Structure

```plaintext
/
|-- index.html   // Main HTML file
|-- style.css    // Custom CSS styles
|-- script.js    // JavaScript logic
```

---

## Installation and Setup

1. Clone or download the repository.
2. Open `index.html` in a web browser to access the application.

---

## Usage Guide

### Step 1: Upload Dataset

1. Click on the **"Upload Dataset (CSV)"** field.
2. Select a valid CSV file from your computer.
   - Ensure the dataset is clean and properly formatted.

### Step 2: Define Hypotheses

1. Enter the **Null Hypothesis (H0)** in the provided text field.
2. Enter the **Alternate Hypothesis (H1)** in the corresponding text field.

### Step 3: Select Significance Level

1. Use the dropdown menu to select a significance level (e.g., 0.05).

### Step 4: Calculate F-Value

1. Click the **"Calculate F-Value"** button.
2. Wait for the loader to complete (if displayed).

### Step 5: View Results

1. The results section will display:
   - Calculated F-Value
   - Degrees of Freedom (df1, df2)
   - Critical Value
   - Conclusion
2. Use the information to accept or reject the null hypothesis.

---

## JavaScript Logic

### Key Functions

- **`calculateFValue(data1, data2)`**
  - Calculates the F-value based on two datasets.
- **`getCriticalValue(df1, df2, significance)`**
  - Fetches the critical value from the F-distribution table.
- **`parseCSV(file)`**
  - Parses the uploaded CSV file into arrays for analysis.

### F-Distribution Table

- The table is embedded in the `script.js` file for quick lookup of critical values.

---

## Example Dataset Format

```csv
Group A, Group B
23, 45
34, 56
12, 67
...
```

- Ensure datasets are separated by commas and include only numeric values.

---

## Error Handling

- **Invalid File Format**: Prompts the user to upload a valid CSV file.
- **Empty Fields**: Alerts if any required fields are left empty.
- **Dataset Size Mismatch**: Ensures datasets have matching lengths for comparison.

---

## Styling and Design

- **Colors**: Utilizes a gradient background with TailwindCSS classes.
- **Buttons**: Interactive hover effects for better user experience.
- **Loader**: Animated loader to indicate processing.

---

## Future Improvements

1. Add support for more statistical tests.
2. Allow multiple dataset uploads for group comparisons.
3. Export results as a PDF report.
4. Incorporate graphical representations of results.

---

## Credits

- **Developer**: [Your Name]
- **Libraries Used**: TailwindCSS, CSV Parsing Library

---

## License

This project is licensed under the MIT License.
