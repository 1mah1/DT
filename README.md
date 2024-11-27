# README for Screen Time and Sleep Analysis Script

## Overview

This Python script analyzes and visualizes the relationship between screen time and sleep patterns. Using data from two files, the script explores trends in screen usage, sleep duration, and sleep quality. It includes statistical analyses, regression models, polynomial fitting, and error metrics to provide insights into the interactions between these variables.

## Features

### 1. Data Preprocessing
- Loads screen time and sleep data from CSV files.
- Cleans and formats data:
  - Converts time strings into numerical values (hours, minutes, seconds).
  - Removes unnecessary columns and handles missing values.
- Calculates total screen time and sleep time in hours.

### 2. Statistical Analysis
- Computes descriptive statistics for sleep quality:
  - Minimum, maximum, and midpoint values.
  - Highlights sleep quality levels using conditional formatting in a styled DataFrame.

### 3. Visualization
- **Scatter Plots**:
  - Daily screen time in hours.
  - Time asleep per day.
  - Sleep quality as percentages.
- **Bar Charts**:
  - Comparison of screen time vs. time asleep.
  - Time in bed vs. time asleep, with differences annotated.
- **Regression and Polynomial Fitting**:
  - Linear regression line with correlation coefficient (`r`).
  - Polynomial models (degrees 4, 5, 6) with R² values.
  - Visualization of polynomial curves.

### 4. Machine Learning Metrics
- Validates and compares `screen time` and `time asleep` arrays using:
  - Mean Squared Error (MSE).
  - Mean Absolute Error (MAE).

## Requirements

The script requires the following Python libraries:
- `numpy`
- `pandas`
- `matplotlib`
- `scipy`
- `scikit-learn`

Install dependencies using:
```bash
pip install numpy pandas matplotlib scipy scikit-learn
```

## Usage

### Input Files
1. **Screen Time Data**: `/Week 2/Screenw2.csv`
2. **Sleep Data**: `/Week 1/Sleepw1.csv`

Ensure the CSV files are formatted correctly and available at the specified paths. Update file paths in the script if necessary.

### Running the Script
Execute the script in a Python environment:
```bash
python script_name.py
```

### Outputs
1. **Plots**:
   - Scatter plots for screen time, sleep time, and sleep quality.
   - Bar charts comparing screen time and sleep patterns.
   - Regression line with annotated equation and correlation coefficient.
   - Polynomial fit curves for various degrees.

2. **Statistics**:
   - Minimum, maximum, and midpoint sleep quality values.
   - R² values for polynomial fits.

3. **Error Metrics**:
   - MSE and MAE for screen time vs. time asleep.

4. **Styled DataFrame**:
   - Sleep quality highlighted with color-coded conditional formatting.

## Code Breakdown

### Data Loading and Cleaning
- Reads and processes CSV files:
  - Extracts relevant columns and rows.
  - Converts time strings to numerical values (hours).

### Visualization
- **Scatter Plots**:
  - Screen time, sleep time, and sleep quality trends.
- **Bar Charts**:
  - Time asleep vs. screen time.
  - Time in bed vs. time asleep.

### Regression and Polynomial Fitting
1. **Linear Regression**:
   - Computes correlation coefficient (`r`) and regression line:
     ```
     y = intercept + slope * x
     ```
   - Visualizes the regression line with scatter plot data.

2. **Polynomial Fitting**:
   - Fits polynomials of degrees 4, 5, and 6.
   - Calculates R² values for each fit.
   - Visualizes polynomial curves.

### Error Metrics
1. Flattens `Tas` and `Tuse` arrays for validation.
2. Computes:
   - **Mean Squared Error (MSE)**: Average squared differences.
   - **Mean Absolute Error (MAE)**: Average absolute differences.

### Example Metric Output
For correctly shaped data:
```
Mean Squared Error (MSE): 0.1234
Mean Absolute Error (MAE): 0.5678
```

## Example Outputs

### Statistical Insights
```
The minimum sleep quality is: 72.0%
The maximum sleep quality is: 95.0%
The midpoint sleep quality is: 83.5%
```

### Regression and Polynomial Fitting
- **Regression Line**: `y = 1.25 + 0.75x, r = 0.85`
- **Polynomial Models**:
  ```
  | Degree | Equation                    | R²       |
  |--------|-----------------------------|----------|
  | 4      | ...                         | 0.93     |
  | 5      | ...                         | 0.94     |
  | 6      | ...                         | 0.95     |
  ```

## Customization
- Modify file paths to match your directory structure.
- Adjust regression and polynomial degrees to explore different relationships.
- Add more visualization styles or metrics as needed.

## Contact
For questions or further suggestions, feel free to reach out!
