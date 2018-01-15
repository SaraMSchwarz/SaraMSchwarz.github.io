---
layout: post
title:      "My CLI Data Gem Project"
date:       2018-01-15 22:43:44 +0000
permalink:  my_cli_data_gem_project
---


For my CLI Data Gem project I wanted to choose a topic that I find interesting and would have fun to play around with. So, I ended up scraping a knitting website for knitting patterns, based on categories. 

The design of this gem is as follows:

When a user runs the gem, they will be greeted with "Patterns for knitters:”. The CLI then asks the user to enter a number of pattern category they want more info on or to type exit to exit the program.

The categories are:

1. Sweaters
2. Hats
3. Scarves
4. Cardigans
5. Blankets and throws

If the user types anything else than numbers 1:3, exit or list, the application tells them their selection is incorrect, please type list to see the categories or exit to exit the program.

The data is scraped off of http://www.loveknitting.com/us/knitting-patterns using the categories mentioned above. The idea is that when a user selects for example the sweater category (1), a list of all sweaters should show up with the name and price.

Seemed pretty straightforward and simple. First I created the file structure by using a gem bundler. My bin includes console, knit_purl (which creates a KnitPurl::CLI.new.call object) and setup files. My lib folder includes a knit_purl.rb file which creates the module for KnitPurl and also acts as the environment, requiring relatives under a knit_purl subfolder. Those files include the cli, version, scraper and patterns ruby files. 

Cli.rb acts as the CLI controller which greets the user and gives them options on what to do with the menu. This is where I added just a little bit of flair in the form of smiling heart eyes and a semi-box around the title. 

In the scraper.rb file, the website is being initialized utilizing string interpolation. This was to make it easier to scrape for the categories without having to create separate methods. So instead of creating a scraping methods for sweaters, then another for hats and so on, the string interpolation part of the url reads the category from the HTML.  

Overall, this was a project that made me really think of everything I’ve learned so far and ask for other people’s input on how to do something like this. I think I will return to this project later on and see if anything can be added or changed. However for now, I’m pretty satisfied with the way this turned out. 




