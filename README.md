# Analysis of ICE Detentions During President Trump's Current Inaguaration Year — 2025
This repository contains data, analytic code, and findings that support portions of the article, “"XXXXX," published XX/XX/XXX. Please read that article, which contains important context and details, before proceeding.

### Data:
This analysis uses a processed Excel sheet from The Deportation Data Project. As of press time, the latest data stops at mid-October 2025. To access the three Excel sheets used for this analysis, please visit: https://archive.org/details/detention-stays

## The spreadsheets come from the following sources:
Name of source: The Deportation Data Project
- name_of_processed_spreadsheet.xlsx: "detention_stays.xlsx"

The spreadsheet contains, among others, the following columns relevant to the analysis:
- "stay_book_in_date_time" - The "detention_stays.xlsx" spreasheet, which contains detentions from September 2023 to mid-October 2025, was processed and labeled by The Deportation Data Project. This column indicates when a detainee was inputted into ICE's system for detainment.

- "year" - This column derived the year from the date column mentioned above to ensure only 2025 detentions were included in the analysis.

## Methodology
### The notebook part_A.ipynb focuses on 2025 detentions. It performs the following analyses:
- Part 1: Store the "detention_stays.xlsx" into a dataframe. We first looked at the types of data in the spreadsheet and printed its length (number of rows).

- Part 2: Convert "stay_book_in_date_time" into a string to make new "year" column We then converted the book-in dates into strings in order to split the column and obtain the year someone was detained by ICE into a seperate column labeled "year."

- Part 3: Reconvert "stay_book_in_date_time" back into dates This step was crucial for resetting the dataframe's index to book-in dates, which would allow us to resample the total number (or count) of detentions by month later in the analysis.

- Part 4: Boolean - Does "year" column contain 2025? This section performed a boolean function on the "year" column, which is considered an object (or string) type. We then created two subsets : one that includes rows that have 2025 in its "year" column" and those that do not have 2025 in its "years" column.

- Part 5: Resample & Illustrate This final section resamples the subset that does contain 2025 in its "years" column, allowing us to only count the number of monthly detentions in 2025. Then, using the resample's results, we created a line graph and tally table that was saved in the notebook's output folder.

Outputs: The notebook's output folder contains monthly total detentions in 2025 as a table: output/2025_month_tally_table.csv. It also contains the monthly totals as a line graph: detentions_2025_monthly_chart.png.

## Running the analysis yourself
You can run the analysis yourself. To do so, you'll need the following installed on your computer:

Python 3 The Python libraries specified in requirements.txt Licensing All code in this repository is available under the MIT License. The data file in the output/ directory is available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?
Contact Gabriela Flores at floresreporter@gmail.com.
