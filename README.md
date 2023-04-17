# ScrapingBee Writing Guidelines

This is the writing guidelines for the ScrapingBee blog: [https://www.scrapingbee.com/blog/](https://www.scrapingbee.com/blog/)

On the ScrapingBee blog, you will find many articles about web scraping, crawling, proxies and more. 

Most of our writers have a software developement background, but we expect them to follow these writing standards.

⚠️ Please read carefully before submitting your content to review 🙂!

The guide is splitted into three parts: 


[Content](#content)

[Conventions and Formatting](#conventions-and-formatting)

[Deliverable](#deliverable)


***This guide is a work in progress, don't hesitate to send any feedback to kevin [at] scrapingbee.com***

## Content

### Structure 

Most articles on ScrapingBee's blog have the same structure. 

For a How-to article this will look like: 

- Title 
- Introduction 
- Goal & Prerequisite (optionnal)
- Step 1...N
- Conclusion 

The detailed structure will be sent to you in the content brief. 

The introduction is the most important section of the article. It should not only describe what the article is about, but also ***hook the reader***. 

This is boring, too descriptive: 

> In this article, we will take a look at the different HTTP clients for Python. Then we will do a benchmark and see what is the best one.

This is better:

> There are a huge number of HTTP clients available for Python - a quick search for ***Python HTTP Clients*** on Github returns over 1700 results(!) How do you make sense of all of them and find one which is right for your particular use case?

### Style

Our tutorials are friendly, engaging and formal. Don't include slang or memes. Occasionnal emojis and jokes are welcome. 

You can use the first person to talk about your experience occasionnaly. But the focus should be on the reader, so ***use the second person*** when possible (avoid we/our): 

Good:
> In this article, you will scrape data from Wikipedia with the BeautifulSoup package.

Bad:
> In this article, we will scrape data from Wikipedia with the BeautifulSoup package.

Our articles are read by people from different background and experience level. You should avoid words like "simple", "obvious" or "easy". 

### Technical Correctness 

> It doesn't work on my machine

One of the most frustrating thing when reading a technical article is having errors in the code. Make sure to include the installation steps for every major operating system (Windows, MacOS, Linux) and test your code. 


### Use a Diagram to Illustrate Complex Concepts

Diagrams are useful to make to explain complex technical complex (workflows, protocols...). 
[https://excalidraw.com/](https://excalidraw.com/) is a great tool to quickly draw a hand-drawn like diagram.


## Conventions and Formatting

Please be careful with typos and English errors. 
You can use [Grammarly](https://www.grammarly.com/) to quickly edit the typos. 


### Some Rules

**Introducing Terms & Acronyms & Initialisms**

When writing technical content, it's very common to use acronyms. If you are not sure the audience is familiar with a term, make sure to explain what it is on the first mention. Then use parenthesis with the shortened version and from then on, only use the shortened version. 

> XML Path Language (XPath) is a query language for selecting nodes from a document. XPath is commonly used for web scraping.

**Use Title Case**

Use [title case](https://en.wikipedia.org/wiki/Title_case) for headers (## and ###). 

**No spaces between words and punctuation:**

Bad:
> Word : another word

Good:
> Word: another word

**Examples**

When you give an example, it's clearer to write "For example" before the example rather than after. 

Bad:
> [Example], for example.

Suggested:
> For example, [example].

**Really and very**

Really and very are in most case unnecessary. It simpler and sometimes stronger to avoid using it. 

**Notes**

When you include a note to the reader, I recommend capitalizing the first word after “note:” so that you can keep the formatting of all notes consistent, whether there is only one sentence or more than one sentence.

> Note: Here is my note. And another one.

**Things**

Avoid using "things" and try to be more specific. 

**Formatting**

Ensure formatting is consistent for similar types of things (headers, list, notes...). It helps with clarity. 

**Simple Sentences & Paragraphs**

Use your judgement, but I recommend erring on the side of shorter, simpler sentences, especially in blog posts. This will help keep the reader engaged. The same goes for paragraphs in blog posts. Over time, you will develop a feel for when the text sounds too choppy and longer sentences are needed in those cases.
Long/Complicated:
> I went to the grocery store because Iwanted flour to make bread for dinner so that there would be enough food.

Shorter/Clearer:
> I was worried there wouldn’t be enough food for dinner. So, I decided to pickup flour at the grocery store and make bread.

## Deliverable

### Directory structure

We ask you to follow the current structure when submitting a new article for review.

If the article you write is called "Web Scraping Basics".

Please send us an archived directory called `web-scraping-basics.zip` or `web-scraping-basics.rar`. You can use any well-known archived file format.

Once unarchived, the directory should have this structure:

```
web-scraping-basics:
  ⌞ index.md 
  ⌞ screenshot.png
  ...
```

Main content of the article should be in an `index.md` file. All other linked ressources should be at the same level as the `index.md` file. Please do not use `/images`, `/gif`, ... subfolders.

### Images and ressources

If you need to add images to your article, instead of using the classic MarkDown images command `![A screenshot of ScrapingBee](scrapingbee-screenshot.png)`

We ask you to use this shortcode instead:

```
{{<img src="scrapingbee-screenshot.png" alt="A screenshot of ScrapingBee" >}}
```
⚠️ Do not prepend the file name with "./" otherwise it will break on our end, just use the raw filename with extension.

⚠️ Starting tag is `{{<` and closing tag is `>}}` **not** `/>}}`

```
🚫 {{< img src="./scrapingbee-screenshot.png" alt="A screenshot of ScrapingBee" >}}
🚫 {{< img src="scrapingbee-screenshot" alt="A screenshot of ScrapingBee" >}}
🚫 {{< img src="scrapingbee-screenshot.png" alt="A screenshot of ScrapingBee" />}}
✅ {{< img src="scrapingbee-screenshot.png" alt="A screenshot of ScrapingBee" >}}
```

You can use this find and replace regexp to make the swap easier if you've already written your content:
```
Replace
!\[(.*)\]\((.*)\)
By
{{<img src="$2" alt="$1" >}}
```

We also ask you to avoid using generic name for your images and ressources like `image1.png` or `picture.png` and use descriptive name and alt atribute.

### Front Matter

We also ask you to write those FrontMatter directives at the top of the `index.md`

```
---
title: Web Scraping Basics
date: 2022-09-15
draft: true
author_id: pierre
description: 
---

Please set `title`, `date` and `description` with the relevant values. For the description, write max 2 sentences explaining what the article is about.
Please leave `author_id` and `draft` as is. The `author_id` value will be updated by us once we've created your profile on our CMS.

# Web Scraping Basics
This is the content of the article ...
```

### Author information

If this is the first time we're working together, and if you want to get credited as the author of the article, please add 
- a small bio ( 2 sentences max)
- a profile picture of you
- Github and / or Twitter profile link
To the email you've send us to show us your article.
