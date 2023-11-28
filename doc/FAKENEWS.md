# Full-Stack-Fake-News-Detection
Full Stack Fake News Detection using machine learning with code and documents

### Youtube Video : https://youtu.be/RvvYV73JWqg
<!-- r8_2pVJDbJXo04t0U73Tb942CfpEF1sFIr3U3mVB -->

[README.md](https://github.com/Vatshayan/Full-Stack-Fake-News-Detection)
[FakeNewsNet](https://github.com/KaiDMML/FakeNewsNet)
[Processing and narrating a video with GPT's visual capabilities and the TTS API](https://cookbook.openai.com/examples/gpt_with_vision_for_video_understanding)
[How to build an agent with the Node.js SDK](https://cookbook.openai.com/examples/how_to_build_an_agent_with_the_node_sdk)
![fake_news_YT](https://user-images.githubusercontent.com/28294942/233419123-cecece7b-4775-4481-abb0-f4ebae8a3d5c.png)
[Build a Full Stack Application with OpenAI, Next.js 13, Vercel and Chakra UI](https://www.youtube.com/watch?v=coPqAHe_oac)
[How to Add Custom GPTs to Any Website in Minutes (OpenAI GPTs Tutorial)](https://www.youtube.com/watch?v=Uk5f3ajkfSs)
[How to build a Full Stack Web Application with Open AI's API](https://www.youtube.com/watch?v=lGvb-gQHw98)
[Easily add captions to your images using AI](https://www.youtube.com/watch?v=9TZsh_-y9DA)
[Narrating a video with GPT's visual capabilities and the TTS API](https://github.com/openai/openai-cookbook/blob/main/examples/GPT_with_vision_for_video_understanding.ipynb)

[Next JS 13 + TypeScript + Chakra UI Project: Fetch from NEWS API](https://www.youtube.com/watch?v=k4NL2Z-9TUk)
[https://www.geeksforgeeks.org/fetching-top-news-using-news-api/](https://www.geeksforgeeks.org/fetching-top-news-using-news-api/)
[react news](https://github.com/MitulMistry/react-google-news)
[Full-Stack-Fake-News-Detection](https://github.com/Vatshayan/Full-Stack-Fake-News-Detection)
[FakeNewsNet](https://github.com/KaiDMML/FakeNewsNet)
[FakeNewsNet](https://github.com/KaiDMML/FakeNewsNet)

### Abstract :
With the advancement in technology, the consumption of news has shifted from Print media to social media. The convenience and accessibility are major factors that have contributed to this shift in consumption of the news. However, this change has bought upon a new challenge in the form of “Fake news” being spread with not much supervision available on the net. In this paper, this challenge has been addressed through a Machine learning concept. we will apply machine learning algorithms for prediction and detection of fake and real news

### Tech Used :

Front End : HTML & CSS

Back End : Python 

Model : Jupyter Notebook

### Hi there 👋

You Can use this Beautiful Project for your college Project and get good marks too. 

Email me Now **vatshayan007@gmail.com** to get this Full Project Code, PPT, Report, Synopsis, Video Presentation and Research paper of this Project.

### Need Code, Documents & Explanation video ? 

## How to Reach me :

### Mail : vatshayan007@gmail.com 

### WhatsApp: **+91 9310631437** (Helping 24*7) **[CHAT](https://wa.me/message/CHWN2AHCPMAZK1)** 

### Website : https://www.finalproject.in/

### 1000 Computer Science Projects : https://www.computer-science-project.in/

### Youtube Explanation : https://youtu.be/RvvYV73JWqg

Mail/Message me for Projects Help 🙏🏻

Getting Errors / problems : Contact me will help you !

Creating web crawlers involves programming and knowledge of web technologies. Here's a simplified guide on how to create a basic web crawler:

1. **Choose a Programming Language:** Python is commonly used due to its simplicity and various libraries like Scrapy and BeautifulSoup.

2. **Understand HTML and DOM:** Learn the basics of HTML structure and how the Document Object Model (DOM) represents web pages. This knowledge helps in extracting data from web pages.

3. **Select a Library or Framework:** Libraries like Scrapy, BeautifulSoup, or Selenium are popular for web crawling and scraping.

4. **Use Scrapy for Advanced Crawling:**
    - Install Scrapy using pip (`pip install scrapy`).
    - Create a new Scrapy project (`scrapy startproject project_name`).
    - Define a spider, which is a class that defines how to crawl a website and how to extract data.

    Example of a simple Scrapy spider:

    ```python
    import scrapy

    class MySpider(scrapy.Spider):
        name = 'example_spider'
        start_urls = ['http://example.com']

        def parse(self, response):
            # Extract data from the webpage using XPath or CSS selectors
            title = response.xpath('//title/text()').get()
            yield {'title': title}
    ```

    This spider crawls 'http://example.com' and extracts the title.

5. **Use BeautifulSoup for Simple Crawling:**
    - Install BeautifulSoup using pip (`pip install beautifulsoup4`).
    - Use requests library to fetch web pages.
    Example of a simple BeautifulSoup script:
    ```python
    import requests
    from bs4 import BeautifulSoup

    url = 'http://example.com'
    response = requests.get(url)
    soup = BeautifulSoup(response.text, 'html.parser')

    # Extract data using BeautifulSoup selectors
    title = soup.title.text
    print(title)
    ```
    This script fetches 'http://example.com' and prints the title using BeautifulSoup.

6. **Respect Robots.txt and Website Policies:** Always check the website's robots.txt file and terms of service to ensure compliance with crawling restrictions and legalities.

7. **Handle Parsing and Data Storage:** After crawling, parse the retrieved content, extract the necessary data, and store it in the desired format, such as CSV, JSON, or a database.

8. **Handle Errors and Exceptions:** Implement error handling mechanisms to deal with issues like connection errors, timeouts, or website changes.

Remember, while web crawling is a powerful tool, it's important to respect website policies, avoid overloading servers with excessive requests, and ensure ethical use of the collected data.

Creating a web crawler involves writing a program that systematically navigates the internet, collects information from websites, and stores it for analysis or other purposes. Here is a step-by-step guide to creating a basic web crawler using Python and the BeautifulSoup library:

### Step 1: Set Up Python and Required Libraries

Make sure you have Python installed. Then, install the required libraries:

```bash
pip install requests
pip install beautifulsoup4
```

### Step 2: Import Libraries

Create a Python script and import the necessary libraries:

```python
import requests
from bs4 import BeautifulSoup
```

### Step 3: Fetch Web Page Content

Use the `requests` library to fetch the content of a web page:

```python
url = 'https://example.com'  # Replace with the URL of the website you want to crawl
response = requests.get(url)
```

### Step 4: Parse HTML Content

Parse the HTML content of the webpage using BeautifulSoup:

```python
soup = BeautifulSoup(response.text, 'html.parser')
```

### Step 5: Extract Data

Use BeautifulSoup's methods to extract the desired data from the HTML content. For example, to extract all the links on the page:

```python
links = soup.find_all('a')
for link in links:
    print(link.get('href'))
```

### Step 6: Implement Crawling Logic

To crawl multiple pages, you'll need to implement logic to navigate through different links. This typically involves iterating through links found on each page:

```python
# Example of crawling multiple pages
base_url = 'https://example.com'
visited_links = set()

def crawl_page(url):
    if url in visited_links:
        return
    visited_links.add(url)
    response = requests.get(url)
    soup = BeautifulSoup(response.text, 'html.parser')
    
    # Extract data or perform operations here
    
    # Find links on the page
    links = soup.find_all('a')
    for link in links:
        next_link = link.get('href')
        if next_link and next_link.startswith(base_url):
            crawl_page(next_link)

# Start crawling from the base URL
crawl_page(base_url)
```

### Step 7: Handle Errors and Add More Functionality

Implement error handling, respect website policies (robots.txt), handle different types of content, and add functionality as per your requirements.

### Important Notes:

- Respect website policies and terms of service. Do not overload servers with excessive requests.
- Web scraping may be subject to legal restrictions. Ensure you have the right to scrape the data you are collecting.
- Continuously test and update your crawler as websites may change their structure or layout.

This is a basic example to get you started with web crawling using Python and BeautifulSoup. Depending on your project's requirements, you may need to add more features and error handling to your crawler.

Creating a web crawler involves writing a program that systematically navigates the internet, collects information from websites, and stores it for analysis or other purposes. Here is a step-by-step guide to creating a basic web crawler using Python and the BeautifulSoup library:

### Step 1: Set Up Python and Required Libraries

Make sure you have Python installed. Then, install the required libraries:

```bash
pip install requests
pip install beautifulsoup4
```

### Step 2: Import Libraries

Create a Python script and import the necessary libraries:

```python
import requests
from bs4 import BeautifulSoup
```

### Step 3: Fetch Web Page Content

Use the `requests` library to fetch the content of a web page:

```python
url = 'https://example.com'  # Replace with the URL of the website you want to crawl
response = requests.get(url)
```

### Step 4: Parse HTML Content

Parse the HTML content of the webpage using BeautifulSoup:

```python
soup = BeautifulSoup(response.text, 'html.parser')
```

### Step 5: Extract Data

Use BeautifulSoup's methods to extract the desired data from the HTML content. For example, to extract all the links on the page:

```python
links = soup.find_all('a')
for link in links:
    print(link.get('href'))
```

### Step 6: Implement Crawling Logic

To crawl multiple pages, you'll need to implement logic to navigate through different links. This typically involves iterating through links found on each page:

```python
# Example of crawling multiple pages
base_url = 'https://example.com'
visited_links = set()

def crawl_page(url):
    if url in visited_links:
        return
    visited_links.add(url)
    response = requests.get(url)
    soup = BeautifulSoup(response.text, 'html.parser')
    
    # Extract data or perform operations here
    
    # Find links on the page
    links = soup.find_all('a')
    for link in links:
        next_link = link.get('href')
        if next_link and next_link.startswith(base_url):
            crawl_page(next_link)

# Start crawling from the base URL
crawl_page(base_url)
```

### Step 7: Handle Errors and Add More Functionality

Implement error handling, respect website policies (robots.txt), handle different types of content, and add functionality as per your requirements.

Building a web crawler involves using programming languages and libraries to navigate websites, gather information, and store the data for analysis or other purposes. Here's a step-by-step guide to creating a basic web crawler using Python:

### Step 1: Choose a Programming Language
Python is commonly used due to its simplicity and rich set of libraries for web scraping and crawling.

### Step 2: Install Necessary Libraries
For web crawling, you can use libraries like `requests` (for making HTTP requests) and `BeautifulSoup` (for parsing HTML).

```bash
pip install requests
pip install beautifulsoup4
```

### Step 3: Create the Crawler

#### Example using `requests` and `BeautifulSoup`:

```python
import requests
from bs4 import BeautifulSoup

def crawl(url):
    try:
        # Send a GET request to the URL
        response = requests.get(url)
        
        # Check if the request was successful
        if response.status_code == 200:
            # Parse the HTML content of the page
            soup = BeautifulSoup(response.content, 'html.parser')
            
            # Extract information from the page (modify according to your needs)
            title = soup.title.text
            print("Title:", title)
            
            # Find links on the page and crawl them
            for link in soup.find_all('a', href=True):
                absolute_link = urljoin(url, link['href'])
                crawl(absolute_link)  # Recursive call to crawl each link
                
    except Exception as e:
        print("Error:", e)

# Start crawling from a specific URL
start_url = 'https://example.com'
crawl(start_url)
```

#### Notes:
- The above code performs a basic crawl by visiting a given URL, extracting the title, and recursively crawling all the links found on the page.
- Customize the data extraction logic (`soup.find`) according to the specific information you want to collect.
- Be cautious about the depth and breadth of your crawl to avoid overwhelming servers or violating website terms of service.

### Step 4: Handle Crawling Restrictions and Limitations
Respect `robots.txt` files, set crawl delays, and avoid making too many requests in a short time to prevent being blocked by websites.

### Step 5: Data Storage
After retrieving the desired data, you can store it in files (CSV, JSON) or databases for further analysis or use.

### Step 6: Continuous Maintenance and Testing
Websites often change their structure or policies. Regularly test and update your crawler to ensure it works effectively and complies with website rules.

import scrapy

class MySpider(scrapy.Spider):
    name = 'example_spider'
    start_urls = ['http://example.com']

    def parse(self, response):
        # Extract data from the webpage using XPath or CSS selectors
        title = response.xpath('//title/text()').get()
        yield {'title': title}


Keep in mind that while web crawling can be a powerful tool, it's crucial to respect the website's terms of service and not overload their servers with excessive requests.