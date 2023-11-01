# Webscraping with Python Example

This Python script aims to gather text data from websites or YouTube videos and save it within a directory named 'data'. It allows users to reference an Excel file containing URLs or create a list of URLs for scraping.

## Overview

#### Installation of Required Libraries
Ensure the required libraries are installed within the virtual environment. See the `requirements.txt` file for more information on necessary libraries.

#### Imported Packages
```python
from pathlib import Path
from bs4 import BeautifulSoup
from urllib.parse import urlparse, urlunparse
from youtube_transcript_api import YouTubeTranscriptApi
from youtube_transcript_api.formatters import TextFormatter
import json
import openpyxl
import requests
import re
import os
import shutil
```
### Webscraping Process
##### Retrieve URLs from Excel File
The script reads URLs from an Excel file containing website and YouTube video links, storing them in separate lists for further processing.

##### Scrape Websites
The script traverses through the list of website URLs, retrieves their content, removes unnecessary elements (headers, footers), and saves the extracted text content and metadata in separate lists. These details are then saved to individual .txt files and a metadata file.

##### Scrape YouTube Transcripts
For YouTube video URLs, the script retrieves their transcripts, cleans the text, and saves it into .txt files. Similarly, metadata regarding the video is stored in the metadata file.

##### Save All Webpage Content
The script saves all collected webpage content, including websites, transcripts, and additional content, into .txt files, while also storing metadata about each piece of content.

### Instructions for Use
1. Ensure the required libraries are installed.
2. Prepare an Excel file with URLs or create a list of URLs.
3. Replace `your_file_name_here` with the relevant file path in the script.
4. Run the script, and it will scrape text content from the provided URLs, saving the data and metadata in the 'data' directory.

**Note:** Prior to running the script, ensure the environment is set up and the necessary packages are installed to execute it successfully. Adjustments to the code might be necessary based on specific website structures and changes in the YouTubeTranscript API or website layouts.

Feel free to modify and adapt the script for your specific requirements.
