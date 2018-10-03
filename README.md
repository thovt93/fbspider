# fbspider
Facebook Web Crawler
Content is most often shared to Facebook in the form of a web page. The first time someone shares a link, the Facebook crawler will scrape the HTML at that URL to gather, cache and display info about the content on Facebook like a title, description, and thumbnail image.

# Crawler Access
The Facebook crawler needs to be able to access your content in order to scrape and share it correctly. Your pages should be visible to the crawler. If you require login or otherwise restrict access to your content, you’ll need to whitelist our crawler. You should also exempt it from DDoS protection mechanisms.
If content isn’t available at the time of scraping, you can force a rescrape once it becomes available by passing the URL through the Sharing Debugger.

# Identifying the Crawler
The Facebook crawler can be identified by either of these user agent strings. You can target one of these user agents to serve the crawler a nonpublic version of your page that has only metadata and no actual content. This helps optimize performance and is useful for keeping pay walled content secure.


Facebot is Facebook’s web crawling robot that helps improve advertising performance. Facebot is designed to be polite. It attempts to access each web server no more than once every few seconds, in line with industry standards, and will respect your robots.txt settings.

Keep in mind Facebot checks for changes to your server’s robots.txt file only a few times a day, so any updates will get noted on its next crawl and not immediately.

## Crawler rate limiting
You can label pages and objects to change how long Facebook’s crawler will wait to check them for new content. Use the og:ttl object property to limit crawler access if our crawler is being too aggressive.

## Giving the Crawler Access
There are two ways to give the crawler access:

### Whitelist the user agent strings listed above, which requires no upkeep
### Whitelist the IP addresses used by the crawler
### Ensuring reasonable latency
You need to ensure that the resources referenced in URLs to be crawled can be retrieved by the crawler reasonably quickly, in no more than a few seconds. If the crawler isn’t able to do this, then Facebook will not be able to display the resource.
