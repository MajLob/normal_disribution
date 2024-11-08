# Normal disribution generator and ANOVA calculator

This script allows users to generate and analyze normally distributed data, perform ANOVA, and export the results to an Excel file. The script follows a series of steps, starting from data input and distribution generation to statistical analysis and post-hoc tests.

## Features

- **Normal Distribution Generation**: Based on user-provided parameters (mean, standard deviation, size, and value range), the script generates normally distributed data.
- **Shapiro-Wilk Normality Test**: The script checks if the generated data follows a normal distribution.
- **ANOVA**: Performs a one-way ANOVA test to analyze the variance among groups of data.
- **Post-hoc Testing (Tukey's HSD)**: Performs Tukey's Honest Significant Difference (HSD) test for multiple pairwise comparisons between groups, with Sidak adjustment for multiple tests.
- **Sum of Squares (SS)**: Calculates the between-group and total sum of squares to assess variance.
- **Effect Size (Eta-squared)**: Computes the eta-squared statistic to interpret the magnitude of the effect.
- **Excel Export**: Exports the generated data and associated variables to an Excel file for further analysis or record-keeping.


## Script Overview
### 1. Data Input and Generation
The user inputs the number of averages they want to generate. For each average, the script collects the mean, standard deviation, sample size, and the minimum and maximum values for the generated distribution.
The script then uses the Box-Muller transform to generate normally distributed data, ensuring the generated values stay within the specified range.
### 2. Normality Testing
The Shapiro-Wilk test is applied to check if each set of generated data follows a normal distribution. If the data is normal, it proceeds to the next step.
### 3. One-Way ANOVA
The script performs a one-way ANOVA to test whether there are significant differences between the means of different groups of generated data.
It prints the F-statistic and p-value, with the p-value formatted for clarity.
### 4. Calculation of Sum of Squares
The script calculates the sum of squares between (SS_B) and total (SS_T) for the groups. This is used for variance analysis and computing the effect size (eta-squared).
### 5. Eta-Squared
The script calculates the eta-squared statistic to assess the effect size:
Small effect: η² < 0.06
Medium effect: 0.06 ≤ η² < 0.14
Large effect: η² ≥ 0.14
### 6. Post-hoc Testing (Tukey's HSD)
Tukey’s HSD test is performed to compare all pairs of groups. The p-values are adjusted using the Sidak correction to account for multiple comparisons.
### 7. Data Export to Excel
The user is prompted to provide a name for the Excel file. The script then exports the generated data and the corresponding variable groupings to an Excel file in .xlsx format.


### Step-by-step Execution:
Enter Number of Averages: The script will prompt you to enter the number of data sets (averages) you want to generate.
Input Parameters for Each Average:
For each data set, input the mean, standard deviation, sample size, and range (min and max values).
Enter Number of Additional Variables: After generating the data, you can add additional variables (e.g., gender, age group).
ANOVA Test: The script will automatically perform a one-way ANOVA and display the results.
Post-hoc Analysis: It performs Tukey's HSD test for pairwise comparisons, with Sidak correction for multiple tests.
Excel Export: Finally, you will be asked to specify a filename, and the script will export the generated data to an Excel file.
