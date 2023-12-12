# Welcome to Team 8's Business Analytics Capstone Project 👋

# Introduction
The project is **Gen AI for Prospect Information Report** for **Marsh** which aims to use generative AI and other possible technologies to automate the production of elementary company reports for brokers in Marsh.
There are currently 5 different repositories listed below:
| Repositories        | Purpose           |
| :-------------: |-------------|
| [user-portal](https://github.com/BT4103-Grp8/user-portal/tree/main) | To start the front-end user portal for the user to start using the web-application |
| [webscraper](https://github.com/BT4103-Grp8/webscraper)| Contains the python code which web scrapes the internet for information of the company keyed into the front-end user portal |
| [pdfparser](https://github.com/BT4103-Grp8/pdfparser) | Contains the python code which parses the 20-F form of the company (if there is one) to push into the AI model |
| [info-extraction](https://github.com/BT4103-Grp8/info-extraction)  | Contains the python code which runs the Generative AI model to answer fixed prompts given to it using the information that has been web scraped and inputted by the user |
| [report-generator](https://github.com/BT4103-Grp8/report-generator) | Contains the python code which formats the front-end user dashboard into a markdown format for the user to download as a PDF file |

# To get started
To get access: Feel free to email longja05@gmail.com to request for access

Step 1: Download the following repositories into local machine
- (https://github.com/BT4103-Grp8/user-portal/tree/main)
- (https://github.com/BT4103-Grp8/info-extraction)
- (https://github.com/BT4103-Grp8/webscraper)
- (https://github.com/BT4103-Grp8/report-generator)
- (https://github.com/BT4103-Grp8/pdfparser)

Step 2: Order of project execution
1) webscraper-main
2) pdfparser-main
3) info-extraction-main
4) report-generator-main [Use report-generator-integration-google-cloud for google cloud setup]
5) user-portal-main [Use user-portal-local-dev for local setup]

Step 3: Follow the instructions found on the ReadMe of each repository to execute the code.

# Additional Notes

## Difference between user-portal branches
**user-portal-main**: Uses google cloud functions for web-scraper and info-extraction (without Dolly)

**user-portal-local-dev**: Uses server.py to run all 4 python scripts

For local setup, use user-portal-local-dev branch, server.py file has all the scripts that needs to be customised before execution.

## Difference between report-generator branches
**report-generator-main**: works with user-portal-main

**report-generator-integration-google-cloud**: edited to work as a google cloud function but still facing some issues which can be resolved by using another library (instead of pyhtml2pdf) to convert the html to pdf which does not download the pdf locally.

# Mongo DB
The details of the MongoDB Atlas we have made use to store our data is as follows:
Organization ID: 60ae8bc742cb863bc3886a0b
Project ID: 650b2f2afc01295b14c3d942
Project Name: Marsh
Database name: marsh
Collections:
- company_data (collection containing data from web-scraper script execution)
- info_extraction (collection containing data from info-extraction script execution)
- risk_data (collection containing data from pdfparser script execution)
- fs.chunks [No longer in use]
- fs.files [No longer in use]






