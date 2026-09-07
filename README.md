# project_portfolio
My project portfolio to display all of my projects! 

FINAL PROJECT FOLDER: 
# U.S. Treasury Data Pipeline & Analysis

## Project Overview

This project uses Python and the U.S. Treasury Fiscal Data API to collect and organize daily Treasury deposit and withdrawal data.

The goal of the project was to build an automated data pipeline that can retrieve financial data, clean it, store it in a CSV file, and keep the dataset updated without needing to manually download new data.

## What the Program Does

The program:

- Connects to the U.S. Treasury Fiscal Data API
- Retrieves Treasury deposit and withdrawal records from January 2024 to the present
- Handles API pagination to collect large amounts of data
- Cleans and validates dates and transaction amounts using pandas
- Saves the cleaned data to a CSV file
- Checks the most recent date already stored before requesting new data
- Only pulls new records when the existing dataset needs to be updated
- Removes duplicate and missing records before saving the data

## Tools & Technologies

- Python
- pandas
- requests
- REST API / JSON
- Git & GitHub
- Linux / GitHub Codespaces

## Data

The data comes from the U.S. Treasury Fiscal Data API's Daily Treasury Statement data.

The dataset includes:

- Record date
- Transaction type (deposit or withdrawal)
- Transaction category
- Daily transaction amount

## Why I Built This

I created this project to practice working with real-world financial data and develop my skills in API integration, data cleaning, automation, and data analysis.

One of my main goals was to create a process that could continue to update itself as new Treasury data becomes available rather than working with a static dataset.

## Skills Demonstrated

This project demonstrates experience with:

- API data collection
- Data cleaning and validation
- Working with large datasets
- API pagination
- Python loops and error handling
- pandas DataFrames
- CSV data storage
- Automating repeatable data processes