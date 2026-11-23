# Experiment 4 : Yearly Revenue Growth Visualization Using Matplotlib

## Aim

To visualize the yearly trend of company revenue and expenses from 2017 to 2023 using Matplotlib by plotting multi-line charts with customized markers, labels, legends, gridlines, and point annotations.

## Algorithm

1. **Start** the program.
2. **Import Libraries**: Import `matplotlib.pyplot` as `plt` for plotting and `numpy` as `np` for numeric array generation and index lookup.
3. **Initialize Dataset**:
   * Generate an array `years` spanning `2017` to `2023` using `np.arange(2017, 2024)`.
   * Define lists `revenue` and `expenses` representing annual amounts in Lakhs.
4. **Configure Figure & Plot Lines**:
   * Initialize a figure canvas of size $8 \times 5$ inches using `plt.figure(figsize=(8, 5))`.
   * Plot `revenue` against `years` as a solid green line with circular markers (`marker='o'`).
   * Plot `expenses` against `years` as a dashed red line (`linestyle='--'`) with square markers (`marker='s'`).
5. **Format Chart Aesthetics**:
   * Add a bold chart title (`plt.title()`) and axis labels (`plt.xlabel()`, `plt.ylabel()`).
   * Enable dashed semi-transparent gridlines (`plt.grid()`) and place the legend in the upper-left corner (`plt.legend(loc='upper left')`).
6. **Annotate Peak Values**:
   * Find the indices of maximum revenue and maximum expenses using `np.argmax()`.
   * Highlight both peak data points on the chart with directional arrows and text callouts using `plt.annotate()`.
7. **Adjust Layout & Display**:
   * Prevent label clipping via `plt.tight_layout()` and render the final plot with `plt.show()`.
8. **Stop** the program.

## Functions and Methods Used

| Category | Function / Method | Purpose / Description |
| :--- | :--- | :--- |
| **Numerical Operations** | `np.arange()` | Generates evenly spaced integer years (`2017` through `2023`) |
| | `np.argmax()` | Returns the array index of the maximum revenue and expense values |
| **Line Plotting** | `plt.figure()` | Initializes a new figure window with custom dimensions |
| | `plt.plot()` | Draws line plots with customized markers, colors, line styles, and widths |
| **Chart Formatting** | `plt.title()`, `plt.xlabel()`, `plt.ylabel()` | Adds descriptive title and axis labels with custom font sizes |
| | `plt.grid()`, `plt.legend()` | Adds background gridlines and displays series labels in the upper left |
| **Annotations & Display** | `plt.annotate()` | Places text labels with arrows pointing to peak revenue and expense points |
| | `plt.tight_layout()`, `plt.show()` | Optimizes spacing to avoid overlapping elements and renders the figure |

## Program / Code

#Company Revenue and Expense Visualization using Matplotlib
import matplotlib.pyplot as plt
import numpy as np

#Step 1: Create dataset

import pandas as pd

#Step 1: Create a sample retail dataset

data = {

"Order_ID": [101, 102, 103, 104, 105, 105, 106, 107],

"Product": ["Laptop", "Tablet", "Phone", "Printer", "Monitor", "Monitor", "Tablet", "Laptop"],

"Region": ["East", "West", "North", "South", "East", "East", "West", None], "Sales": [55000, 32000, None, 18000, 24000, 24000, 32000, 55000],


"Discount": [5, None, 10, 8, 5, 5, None, 8],

"Profit": [8000, 5000, 4000, None, 3000, 3000, 5000, 8000]

}

df= pd.DataFrame(data)

print("---- Original Retail Dataset ----")

print(df)

print("\nDataset Shape:", df.shape)


#Step 2: Plot Revenue and Expenses

print("\nMissing Values per Column:\n", df. isnull() sum())

#Step 3: Add titles, labels, and grid

df["Sales"] fillna(df["Sales"] mean(), inplace True)

df["Discount"]. fillna(df["Discount"] mean(), inplace True)

df["Profit"] fillna(df["Profit"].mean(), inplace True)

#Step 4: Add legend

df["Region"].fillna(df("Region"].mode()[0], inplace True)

#Step 5: Annotate highest revenue and expense

df.drop duplicates (inplace=True)

print("\n---- Cleaned Retail Dataset --")

print(df)

print("\nDataset Shape after Cleaning:", df.shape)


#Step 6: Adjust layout and show plot

print("\nSummary Statistics:\n", df.describe())


## Output
<img width="717" height="1600" alt="WhatsApp Image 2026-11-23 at 9 21 44 PM" src="https://github.com/user-attachments/assets/d164ab74-71bd-4e21-9ec7-a2473afd3c93" />

## Result

The program successfully creates datasets for yearly company revenue and expenses and renders an annotated multi-line comparison chart using Matplotlib.
