# Extract Stock Data

- Extract Stock data from a Python library
- Extract Stock data using a web Scraping

### From a Python library: yfinance

```python
!wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/data/apple.json # download file

import json
with open('apple.json') as json_file:
  apple_json = json.load(json_file)
apple_json >> {'zip': '95014',
 'sector': 'Technology',
 'fullTimeEmployees': 100000,...}
apple_json['sectore'] # Technology

!pip install yfinance==0.2.4
import yfinance as yf
import pandas as pd
apple = yf.Ticker("AAPL")
apple_data = apple.history(period="max")
```

Use the `history` method of the Ticker object to <u>download the historical data</u> for the stock. The `period` parameter of the `history` method specifies the time period for which we want to download the data. In this example, set it to `max` to download the maximum amount of available historical data.

Here are some of the possible values for the period parameter and what they represent:

- period="1d": Download 1 day of historical data.
- period="5d": Download 5 days of historical data.
- period="1mo": Download 1 month of historical data.
- period="3mo": Download 3 months of historical data.
- period="6mo": Download 6 months of historical data.
- period="1y": Download 1 year of historical data.
- period="2y": Download 2 years of historical data.
- period="5y": Download 5 years of historical data.
- period="10y": Download 10 years of historical data.
- period="ytd": Download historical data since the beginning of the current year.
- period="max": Download all available historical data.

```python
apple_data.head() # Date is index
```

| Date                      | open     | high     | low      | close    | volume    | dividends | stock splits |
| ------------------------- | -------- | -------- | -------- | -------- | --------- | --------- | ------------ |
| 1980-12-12 00:00:00-05:00 | 0.099450 | 0.099882 | 0.099450 | 0.099450 | 469033600 | 0.0       | 0.0          |

```python
apple_data.reset_index(inplace=True)
apple_data.head()
apple_date.plot(x="Date", y="open")
```

|      | Date                      | open     | high     | low      | close    | volume    | dividends | stock splits |
| ---- | ------------------------- | -------- | -------- | -------- | -------- | --------- | --------- | ------------ |
| 1    | 1980-12-12 00:00:00-05:00 | 0.099450 | 0.099882 | 0.099450 | 0.099450 | 469033600 | 0.0       | 0.0          |

**Dividends** are the distribution of a companys profits to shareholders. In this case they are defined as an amount of money returned per share an investor owns. Using the variable `dividends` we can get a dataframe of the data. The period of the data is given by the period defined in the 'history` function.

```
apple.dividends
```

# Extracting Stock Data Using a Web Scraping

Not all stock data is available via the API in this assignment; you will use web-scraping to obtain financial data. 
You will extract and share historical data from a web page using the **BeautifulSoup** library.

1. Extracting data using BeautifulSoup (Parse HTML)
   - Download the web page Using Requests Library 
   - Parse HTML on a web page using BeautifulSoup 
   - Extract data and build a data frame 
2. Extracting data using pandas

```python
!mamba install bs4==4.10.0 -y
!mamba install html5lib==1.1 -y 
!pip install lxml==4.6.4

import pandas as pd
import requests
from bs4 import BeautifulSoup
```

Using Webscraping to Extract Stock Data Example:

We will extract Netflix stock data https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/netflix_data_webpage.html.

| Date                      | open     | high     | low      | close    | Adj close | Volume |
| ------------------------- | -------- | -------- | -------- | -------- | --------- | ------ |
| 1980-12-12 00:00:00-05:00 | 0.099450 | 0.099882 | 0.099450 | 0.099450 | 469033600 | 0.0    |

# Steps for extracting the data

1. Send an HTTP request to the web page using the requests library.
2. Parse the HTML content of the web page using BeautifulSoup.
3. Identify the HTML tags that contain the data you want to extract.
4. Use BeautifulSoup methods to extract the data from the HTML tags.
5. Print the extracted data

### Step 1: Send an HTTP request to the web page

The `requests.get()` method takes a URL as its first argument, which specifies the location of the resource to be retrieved. 

 `.text` method for extracting the HTML content as a string in order to make it readable.

```python
url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/netflix_data_webpage.html"
# Step 1
data  = requests.get(url).text
print(data)
```

### Step 2: Parse the HTML content

#### Parsing the data using the BeautifulSoup library

- Create a new BeautifulSoup object.

  **Note:** To create a BeautifulSoup object in Python, you need to pass two arguments to its constructor:

1. The HTML or XML content that you want to parse as a string.
2. The name of the parser that you want to use to parse the HTML or XML content. This argument is optional, and if you don't specify a parser, BeautifulSoup will use the default HTML parser included with the library. here in this lab we are using "html5lib" parser. `soup = BeautifulSoup(data, 'html5lib') # parsing the data`

```python
soup = BeautifulSoup(data, 'html5lib') # parsing the data
```



### Step 3: Identify the HTML tags

As stated above, the web page consists of a table so, we will scrape the content of the HTML web page and convert the table into a data frame.

```python
# First we isolate the body of the table which contains all the information
# Then we loop through each row and find all the column values for each row
netflix_data = pd.DataFrame(columns=["Date", "Open", "High", "Low", "Close", "Volume"])
for row in soup.find("tbody").find_all('tr'):
    col = row.find_all("td")
    date = col[0].text
    Open = col[1].text
    high = col[2].text
    low = col[3].text
    close = col[4].text
    adj_close = col[5].text
    volume = col[6].text
    
    # Finally we append the data of each row to the table
    netflix_data = netflix_data.append({"Date":date, "Open":Open, "High":high, "Low":low, "Close":close, "Adj Close":adj_close, "Volume":volume}, ignore_index=True)  

netflix_data.head()
```

```python
soup.find('title') #<title>Amazon.com, Inc. (AMZN) Stock Historical Prices &amp; Data - Yahoo Finance</title>
att = soup.find('thead').find_all("th") #len:7
for item in att:
    item.text  # ['Date', 'Open', 'High', 'Low', 'Close*', 'Adj Close**', 'Volume']

# Get the value of the last line
amazon_data['Open'].values[-1]
amazon_data.at[60,'Open']
```



## What is read_html in pandas library?

`pd.read_html(url)` is a function provided by the pandas library in Python that is used to extract tables from HTML web pages. It takes in a URL as input and returns a list of all the tables found on the web page.

```python
# get a url, return a list of all the tables
read_html_pandas_data = pd.read_html(url)
read_html_pandas_data[0]

# convert the BeautifulSoup object to a string; there is only one table on the page
read_html_pandas_data = pd.read_html(str(soup))
netflix_dataframe = read_html_pandas_data[0]
```



You can ignore **warnings** using the warnings module.

```python
import warnings
# Ignore all warnings
warnings.filterwarnings("ignore", category=FutureWarning)
```

## Extract and Visualize Stock Data

Table of Contents

- Define a Function that Makes a Graph
- Question 1: Use yfinance to Extract Stock Data
- Question 2: Use Webscraping to Extract Tesla Revenue Data
- Question 3: Use yfinance to Extract Stock Data
- Question 4: Use Webscraping to Extract GME Revenue Data
- Question 5: Plot Tesla Stock Graph
- Question 6: Plot GameStop Stock Graph

```python
!pip install yfinance==0.1.67
!mamba install bs4==4.10.0 -y
!pip install nbformat==4.2.0
import yfinance as yf
import pandas as pd
import requests
from bs4 import BeautifulSoup
import plotly.graph_objects as go
from plotly.subplots import make_subplots
```



```python
gme_revenues = pd.read_html(str(soup))
gme_revenue = gme_revenues[0]
gme_revenue.columns=['Date', 'Revenue']
gme_revenue['Revenue'] = gme_revenue['Revenue'].str.replace(',|\$', "")
gme_revenue.dropna(inplace=True)
gme_revenue = gme_revenue[gme_revenue['Revenue'] != ""]
```

