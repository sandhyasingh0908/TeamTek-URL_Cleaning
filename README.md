# TeamTek-URL_Cleaning
URL cleaning refers to sanitizing and optimizing URLs for better readability, user experience, and search engine optimization (SEO). It involves removing unnecessary characters, parameters, and symbols, making URLs descriptive and user-friendly. 

**About the Project**

**Extraction of Relevant String from URLs:**
This Python script extracts the relevant string from a given URL. It reads a CSV file (should contain URL column header) containing URLs as well as user-defined URLs and extracts the desired information from each URL by removing the irrelevant parts

**Source:**
The URLs for extraction and parsing are sourced from the following GitHub link containing the csv file: https://raw.githubusercontent.com/kennethtangca/CanTekWebScraping/main/To%20TekTeam/output%20by%20using%20selenium.csv

**Working Example:**
Many URLs contain information relevant to the thesis of the article. For example, the relevant part extracted from the URL "https://www.reuters.com/world/us/fake-biden-robo-call-tells-new-hampshire-voters-stay-home-2024-01-22/" would be "fake biden robo call tells new hampshire voters to stay home 2024 01 22". This is achieved by removing irrelevant parts such as 'https', 'www.reuters.com', 'world' and 'us'

**Key Results:**
The function takes any URL(s) as input
Removes '.com', '.org', and other irrelevant parts of the URLs
Removes characters such as dashes and slashes
Extracts the desired sentence from the URLs, with words separated by spaces

**Notes:**
1. Certain websites such as Reuters prohibit the scraping of content and might return an undesired result
2. It is not necessary that an ideal relevant string can be extracted from all of the URLs, as highlighted in the example used where '2024 01 22' has also been extracted despite being irrelevant, this is due to the variation in the formatting of the URLs highlighting a lack of uniformity which makes the process inexact 

**Libraries/Modules Used:**
[cleanurl]: To clean and normalize URLs by removing unnecessary parameters, query strings, and fragments
[urllib]: For making HTTP requests and interacting with web pages by providing a high-level interface for working with URLs
[urlparse]: Parses a URL string into its individual components
[pandas]: For data manipulation and analysis, particularly for handling structured data in tabular form
[requests]: For making HTTP requests to web servers and handling responses
[pathlib]: For working with filesystem paths, making it easier to navigate directories and manipulate file paths
[re]: For working with regular expressions, allowing for pattern matching and text manipulation tasks

**Workflow:**
1. Removes clutter from URLs and returns a canonicalized version after installing it using pip command
2. Removes the unwanted part from the URL and extracts only the relevant string/query
2.1 Extracts extension of file to covert it into a dataframe using the appropriate method
2.2 Converts and cleans dataframe extracted from .csv file
2.3 Converts & clean any url
2.4 Displays extracted string(s) from the URL
2.5 Fetches each URL one by one in case .csv files
2.6 More cleaning is done as one word URL is irrelevant (having junk characters), thus excluding it
2.7 Accepts URL from user/.csv of URLs for cleaning
