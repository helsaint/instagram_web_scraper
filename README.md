# instagram_web_scraper
Semi automated web scraper. Uses jupyter notebook so some human interaction required
Uses the selenium library and chromium driver
The user will see the page being loaded
Collecting text from each post
Limitations:
  1. not automated and will require human interaction
  2. By.X_Path value may need to be manually changed so inspect the page you want to scrape and ensure you have the correct path for the cells required
  3. A count of iterations is included to prevent scrolling that can go on for a long time
  4. Close any chrome browser or you'll get WebDriverException
  5. Usage of proxies to prevent HTTP 429 errors were considered. However, the difficulty of find enough reliable and free proxies made this option untenable. Therefore we resorted to automatically rate limitin by inserting a random sleep between requests of 7-15 seconds. Additionally after every 15 requests a 180-240s interval was placed. Thus for large scrapes we suggest doing it overnight.
