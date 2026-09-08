# U.S. Treasury Data Pipeline

## Project Overview

This project uses Python and the U.S. Treasury Fiscal Data API to collect and organize daily Treasury deposit and withdrawal data.

The goal was to create a repeatable process for retrieving financial data instead of manually downloading a new dataset each time updated information becomes available.

The program retrieves data from the API, cleans and validates the records, stores them in a CSV file, and checks for new records when the program is run again.

## Project Goal

The main goals of this project were to:

- Practice working with a real-world API
- Automate the data collection process
- Clean and organize financial data using Python
- Create a dataset that can be updated as new information becomes available
- Prepare the data for future analysis and visualization

## Data Source

The project uses data from the U.S. Treasury Fiscal Data API.

The API endpoint provides Daily Treasury Statement data related to deposits and withdrawals from Treasury operating cash.

The project collects the following fields:

- Record Date
- Transaction Type
- Transaction Category
- Daily Transaction Amount

For the initial dataset, the program retrieves records beginning January 1, 2024.

## How It Works

The program follows several steps:

1. Checks whether a Treasury data CSV file already exists.
2. If the file exists, finds the most recent date currently stored.
3. Compares the most recent record with the current date.
4. Requests new records from the Treasury API when the dataset needs to be updated.
5. Uses pagination to retrieve large amounts of API data across multiple pages.
6. Converts the JSON API response into a pandas DataFrame.
7. Cleans and validates dates and transaction amounts.
8. Removes missing values and duplicate records.
9. Sorts the completed dataset by date.
10. Saves the updated data to a CSV file.

## First Run

If the CSV file does not already exist, the program requests Treasury records beginning January 1, 2024.

Because the API returns data in pages, the program loops through each page until all available records have been collected.

The records are then combined into a pandas DataFrame, cleaned, and saved as a new CSV file.

## Future Runs

If the CSV already exists, the program reads the existing dataset and identifies the most recent record date.

Instead of downloading the entire dataset again, the API request only asks for records that are newer than the data already stored.

The new records are then combined with the existing dataset and checked for duplicates before the CSV is updated.

This makes the data collection process more efficient and allows the dataset to continue growing over time.

## Data Cleaning

Before saving the data, the program:

- Converts record dates into datetime values
- Converts transaction amounts into numeric values
- Handles non-numeric values
- Removes rows containing missing values
- Checks for duplicate records
- Sorts the data by date

These steps help create a consistent dataset that can be used for analysis.

## Tools & Technologies

- Python
- pandas
- requests
- REST API
- JSON
- CSV
- Git
- GitHub
- Linux
- GitHub Codespaces

## Challenges & What I Learned

One of the biggest challenges in this project was working with a large amount of data from an API.

The Treasury API uses pagination, so I had to create a loop that requests multiple pages of data rather than relying on a single API request.

I also learned more about troubleshooting API connections, working with JSON responses, converting API data into pandas DataFrames, and creating a process that can update existing data instead of starting over every time the program runs.

## Skills Demonstrated

- API Data Collection
- Python Programming
- pandas DataFrames
- Data Cleaning & Validation
- API Pagination
- JSON Processing
- CSV Data Storage
- Data Pipeline Development
- Git & GitHub
- Troubleshooting

## Future Improvements

Future improvements to this project could include:

- Creating visualizations of Treasury deposits and withdrawals
- Analyzing changes in Treasury activity over time
- Comparing different transaction categories
- Adding additional error handling for API requests
- Automating when the data pipeline runs
- Creating a dashboard to display important trends

## Project Files

- `pythonproject.py` - Python program used to retrieve, clean, and update Treasury data
- `treasury_data.csv` - Cleaned Treasury dataset created by the program
