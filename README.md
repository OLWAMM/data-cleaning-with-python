# data-cleaning-with-python
Overview This document outlines the steps taken to preprocess and transform the FIFA 21 dataset for analysis. The preprocessing involves cleaning and standardizing data, extracting new information, and adding new columns.
# Steps taken
## Loading the Data
- The FIFA 21 dataset was loaded into a pandas DataFrame, and a copy was created to work with while preserving the original data.
- All columns were configured to be fully visible for easier analysis.
## Cleaning the Club Column
- Extra spaces before and after club names were removed to ensure consistency and avoid duplicate entries caused by formatting differences.
### Processing the Contract Column
- Extracting Contract Details
- Contracts with Free or On Loan status were identified. These do not have specific start or end dates, so placeholders (NaN) were used for these values.
- For standard contracts, start and end dates were extracted, and the contract length in years was calculated.# Adding New Columns
### Three new columns were added to store:
- Contract Start: The start date of the contract.
- Contract End: The end date of the contract.
- Contract Length(years): The duration of the contract in years.
### Categorizing Contract Status
- Contracts were classified into one of three categories:
- Free: Players without a current contract.
- On Loan: Players loaned to another club.
- Contract: Players with active standard contracts.
- A new column, Contract Status, was added to reflect this categorization.

## Standardizing the Height Column
- Heights were provided in mixed units, either in centimeters (e.g., 180cm) or feet and inches (e.g., 6'2").
- All height values were converted into centimeters for uniformity and renamed as Height(cm).
## Standardizing the Weight Column
- Weights were recorded in mixed units, either kilograms (e.g., 75kg) or pounds (e.g., 165lbs).
- All weight values were converted into kilograms for consistency and renamed as Weight(kgs).
## Cleaning the W/F Column
- The W/F column (Weak Foot rating) included star symbols (★), which were removed to leave only numerical values. This made the column easier to analyze.
# Final Outputs
##  New Information Added:
- Detailed contract information, including start and end dates, contract length, and contract status.
- Standardized height and weight values in consistent units.
## Columns Cleaned:
- Club names were made uniform.
- Unnecessary symbols in ratings columns were removed.
- Consistency: Mixed formats (e.g., units of measurement) were standardized.
-  Cleaning steps improved the usability of key columns for analysis.
