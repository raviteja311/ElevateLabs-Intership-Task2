# Titanic Dataset - Simple EDA (Task 2)

## What is this?

This project explores the famous Titanic dataset (`Titanic-Dataset.csv`) using the `Task2.ipynb` notebook. The goal was to look at the passenger data, clean it up a bit, and make some basic charts to understand it better.

## Dataset Used

*   `Titanic-Dataset.csv` - Contains info about Titanic passengers like:
    *   `Survived`: Did they survive? (0 = No, 1 = Yes)
    *   `Pclass`: Ticket class (1st, 2nd, 3rd)
    *   `Sex`: Passenger's sex
    *   `Age`: Passenger's age
    *   `SibSp`, `Parch`: Family size info
    *   `Fare`: How much the ticket cost
    *   `Cabin`: Cabin number (had lots of missing data)
    *   `Embarked`: Where they got on

## What Was Done in the Notebook (`Task2.ipynb`)

1.  **Loaded Data:** Read the `Titanic-Dataset.csv` file.
2.  **Looked at Data:** Used `.head()`, `.info()`, `.describe()` to get a first look at the data types, size, and basic stats.
3.  **Cleaned Missing Data:**
    *   Filled missing `Age` values with the median (middle value).
    *   Removed the `Cabin` column because too much data was missing.
    *   Filled the few missing `Embarked` values with the most common port.
4.  **Calculated Stats:** Got summary statistics (mean, median, min, max, etc.) for the number-based columns again after cleaning.
5.  **Made Charts:**
    *   **Histograms:** Showed how `Age`, `Fare`, and other number columns were distributed.
    *   **Boxplots:** Helped spot the range, median, and outliers (unusual values) in columns like `Age` and `Fare`.
    *   **Pairplot:** Looked at relationships between `Age`, `Fare`, `SibSp`, `Parch`, and colored the points by whether the passenger `Survived`.

## Key Things Found

*   Needed to handle missing data, especially in `Age` and `Cabin`.
*   Most passengers were younger adults (20s-30s).
*   Ticket `Fare` varied a lot, with most being cheap but some very expensive (outliers).
*   Many passengers traveled alone (0 `SibSp` and `Parch`).
*   The pairplot hinted that `Age` and `Fare` might be related to survival, but more analysis is needed.

## Tools Used

*   Python
*   Pandas (for data handling)
*   Matplotlib / Seaborn (for charts)

## How to Run

You need Python and the libraries listed above. Put the `Titanic-Dataset.csv` file in the same folder as `Task2.ipynb` and run the notebook cells.
