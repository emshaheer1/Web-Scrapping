# Create Custom Proxy Middleware
*  Middleware is basically a piece of code that Scrapy will run when processing requests.
 ```python 
  DOWNLOADER_MIDDLEWARES = {
    'myproject.middlewares.CustomProxyMiddleware': 350,
    'scrapy.downloadermiddlewares.httpproxy.HttpProxyMiddleware': 400,
}
```
# User Agents
* When scraping the web, sometimes the site you want to scrape don't really want you scraping their data so you need to disguise who you are.
* To do so we need to manage the User Agents we send along with our HTTP requests.
* User Agents are strings that let the website you are scraping identify the application, operating system (OSX/Windows/Linux), browser (Chrome/Firefox/Internet Explorer), etc. of the user sending a request to their website.
* They are sent to the server as part of the request headers.
```python 
user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/98.0.4758.82 Safari/537.36
```
