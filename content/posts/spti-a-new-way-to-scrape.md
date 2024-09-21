---
title: "SPTI: A New Way to Scrape"
date: 2024-09-21T05:30:00.000Z
# weight: 1
# aliases: ["/first"]
tags: ["Web Scraping"]
author: "pyscripter99"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Learn how scrape, parse, transform and insert benefit over traditional scraping"
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/pyscripter99/retzer.xyz/content"
    Text: "Suggest Changes"
    appendFilePath: true
---

The traditional approach to web scraping that you see when searching learning how to scrape, quickly leads to messy and unmaintainable code. As I am now diving into more and more complex web scraping projects, I am finding that methods I am using needs to change, as logic is bundled together, and plain messy.

Let's take a look at an example that all scarping articles would give.

```python
import requests
from bs4 import BeautifulSoup

url = "https://www.scrapethissite.com/pages/forms/?per_page=100"

response = requests.get(url)
soup = BeautifulSoup(response.text, "html.parser")

class Team:
    name = ""
    year = 0
    wins = 0
    losses = 0
    win_percentage = 0
    goals_for = 0
    goals_against = 0
    goals_difference = 0

# TODO: Add logic to scrape data


```
