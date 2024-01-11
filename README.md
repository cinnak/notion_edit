# Story of this repo
- This Python script uses the Notion API to manage and create blocks in your Notion pages.
- I wrote this script because I wanted to move my reading records from 2023 over to Notion. Can you believe it? I read a whopping 68 books in 2023! 
Anyhow, when I imported my excel file, the "Comments" column, usually this long stretch of words ends up being a property in the database. Kinda rough on the eyes, you know? So, I decided to clean things up a bit by moving the "Comments" property to a page block. Things are looking good now!
- However, the story doesn't end here. The next step in my plan is to extract all the images from the excel spreadsheet and transfer them to the Notion database. The interesting part of this task is that these images will serve as the page covers. It's a pretty straightforward, yet creative approach.
# Overview
The script has two main functions:
- get_pages(): It retrieves pages from a Notion database; you can specify the number of pages to return or get all pages by default.
- create_block(): This function creates new 'paragraph' blocks in a given Notion page.
In the main part of the script, get_pages() is used to retrieve all pages from a specified database. Then, it loops through these pages, gets some content from the '简评' property of each page, and uses create_block() to add this content to the page as a new paragraph block.
# Requirements
- Python 3
- Requests library
- Notion library
- Notion account and API key
# Setup
- Before running the script, replace YOUR_API_KEY & DATABASE_ID in the following line with your Notion API key
- YOUR_API_KEY and DATABASE_ID are used to authorize the script to access and modify your Notion workspace.

PS: The Notion Postman Workspace is a valuable resource when interacting with the Notion API.
https://www.postman.com/notionhq/workspace/notion-s-api-workspace/overview
