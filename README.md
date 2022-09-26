# jobs_scraper
This notebook demonstrates the usefulness of a web scraper to extract data prior to analysis.

The libraries used are requests, pandas and selenium.

Selenium is used to navigate to the LinkedIn Jobs website, input a job title to search for (in our case, Data Analyst), and scrapes the results from the page with different filters.

Since LinkedIn only allows a maximum number of 1000 search results in the page, we need selenium to scroll to the bottom, after clicking the "Click more Jobs" button multiple times to get the maximum number of search results for different combinations of filters.

Once we have all the results loaded, we scrape the results and save it into a pandas dataframe.

Eventually, the goal is to automate the process of scraping and saving the results into an AWS RDS database which can be called from a different script for the purposes of analysis of ML.
