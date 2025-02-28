# mimic-spreadsheet Project Overview
This web application is designed to closely mimic the user interface and core functionalities of Google Sheets with a focus on mathematical functions, data quality functions, and key UI interactions. It provides the ability to input data, format cells, perform mathematical operations, apply data quality functions, and manage spreadsheet elements like rows, columns, and cell dependencies.
# Frontend:

React: Used to build the dynamic user interface and handle the state of the spreadsheet.
CSS / CSS-in-JS (styled-components): Used for styling the spreadsheet interface to resemble Google Sheets.
Redux (or Context API): Used for state management to keep track of the spreadsheet's data and operations.

# Mathematical Engine:

JavaScript Math Functions: Built-in JavaScript functions (such as Math.max(), Math.min(), Math.sum(), etc.) are used for mathematical calculations.
Custom Formula Engine: For advanced formula parsing, custom functions for cell dependency management are created in JavaScript.
# Data Quality Functions:

Custom JavaScript Functions: Data manipulation functions like TRIM, UPPER, LOWER, and REMOVE_DUPLICATES are implemented using plain JavaScript.
Data Structures
# Spreadsheet Data:

A 2D array (array of arrays) is used to represent the spreadsheet’s grid where each element corresponds to a cell.
Each cell contains an object with properties like value, formula, format, etc.
# State Management:

Redux / Context API manages the global state of the application, including the data inside the spreadsheet, cell formatting, and formulas.
Actions & Reducers in Redux are used to update the state based on user interactions, such as adding/removing rows, applying functions, or editing cell content.
# Cell Dependency Management:

Each formula in a cell keeps track of dependent cells. For example, a SUM formula will know which cells to re-evaluate when one of the dependent cells changes.
Dependency trees are constructed dynamically as users add formulas and apply operations.
# Example:

1. Enter "10" in cell A1
2. Enter "20" in cell A2
3. Enter "30" in cell A3
4. Click cell A4
5. Type "=SUM(A1:A3)" in the formula bar
The result (60) should appear immediately in cell A4 without needing to save.
Similarly we can apply for functions which are given above.
note:1.must use '=' before function and need of two arguments.
2.If a fuction should be applied for a single variable then take its cell for both arguments.
# Features

1. Spreadsheet Interface
Mimicking Google Sheets UI: The app replicates the visual design of Google Sheets, including the toolbar, formula bar, and cell structure.
Drag Functions: Users can drag content, formulas, and selections, similar to how Google Sheets behaves.
Cell Dependencies: Formulas and functions are accurately updated when changes are made to related cells.
Basic Cell Formatting: Users can apply formatting to cells such as bold, italics, font size adjustments, and font color changes.
Row/Column Management: Users can add, delete, and resize rows and columns.
2. Mathematical Functions
The app supports the following functions:

SUM: Calculates the sum of a range of cells.
AVERAGE: Calculates the average of a range of cells.
MAX: Returns the maximum value in a range of cells.
MIN: Returns the minimum value in a range of cells.
COUNT: Counts the number of cells containing numerical values in a range.
3. Data Quality Functions
TRIM: Removes leading and trailing whitespace from text in a cell.
UPPER: Converts text in a cell to uppercase.
LOWER: Converts text in a cell to lowercase.
REMOVE_DUPLICATES: Removes duplicate rows from a selected range.
FIND_AND_REPLACE: Allows users to search for and replace specific text within a range of cells.
4. Data Entry and Validation
Users can enter various types of data, such as numbers, text, and dates.
Basic data validation checks are implemented, such as ensuring numeric cells only contain numbers.
5. Testing
Users can test the implemented functions with their own data and view the results clearly within the application.
Bonus Features
Additional Functions: Support for more advanced mathematical and data quality functions.
Complex Formulas & Cell Referencing: Support for relative and absolute references in formulas.
Save/Load Spreadsheets: Users can save their work and load saved spreadsheets for future use.
Data Visualization: The app includes chart and graph functionalities for visual representation of data.
