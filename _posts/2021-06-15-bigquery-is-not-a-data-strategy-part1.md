---
layout: blogpost
title: "BigQuery is not a Data Strategy - Part 1 - Identifying Symptoms"
category: "Data Engineering"
type: "TECH"
filename: /blog/bigquery-is-not-a-data-strategy-part1
date: 15-06-2021
image: /images/manja-vitolic-unsplash.jpeg
imageAltText: "A cat staring intently"
image_attribution: Photo by <a href="https://unsplash.com/@madhatterzone?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Manja Vitolic</a> on <a href="https://unsplash.com/s/photos/nerd-cat?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
---

*This is the first in a 4-part series where I talk about what a Data Strategy is, how to identify a lack of or poor data 
strategy in a business and it's systems, implementing a good Data Strategy, 
how to avoid those problems and what to do if you're already experiencing them 
and want to get out of data chaos, into data clarity.*



I've worked in data and reporting since the beginning of my career (2011), and particularly, in the last 3 years,
I've worked with, consulted with or heard from through the developer grape-vine, about problems that:

A - Big Data was supposed to have solved but didn't, and  
B - a set of consistent complaints and problems companies are experiencing with their data. 

So while some of these problems have been around for a while, some are new, and the fancy new Big Data tools are not solving them.
Indeed, it is a combination of tooling, process and culture that will solve our data problems. This should not be too
surprising. Let's get into it some details about those 3 things in this series. First we'll be looking at what symptoms occur with 
people in organisations solving data problems.

**People Symptoms**  

If you work with data in some capacity, you've likely to have heard these phrases from others (or yourself) before:

* "Check with "ultimate data person" -they know the data"
* "Oh, I thought this data explained <this> but you're using it for that"
* "Remember to refer to this extensive list of data quirks on the wiki"
* "We can't really trust the data"
* "The analytics are quite slow"
* "This field is repeated in multiple places"
* "These reports are supposed to match but never do"
* "It takes hours for me to put this report together" 
(I once watched a report "pulling-together" process where the individual 
 had to go across 3 different systems, tying together data they gathered using ID fields of the data extracts and manually 
 aligned all the data into a report, not just once, but regularly as part of their job. This not just inefficient for the 
 business but soul-sucking for the analyst too).


**System Symptoms**  

These are identifiers that you can look for in your data systems:

* All your data is in a tool, none in files
* Data Systems (ie custom reporting, dashboards, ETLs) are slowing down
* Data flow is not documented
* No schema management, not even manual records
* Data Scientists/Analysts/other folks using the data, are spending more than half their time cleaning
* and normalising the data or you have no Engineers at all.
* Hardly any access control - relying on trust
* The same data is being maintained in different places by different team
* Little to no Load Testing. In this Big Data age, systems rapidy cripple under the load. There is no excuse for not testing them under load.

Tools like BigQuery enable companies to rapidly collect, store and query large swathes of data but the tool alone, as with any tools,
is not a sustainable way to go about managing and evolving your data. It alone does not solve the above problems.
In our next section we'll look at what a Data Strategy is and start to look at how to solve these problems.

*In part 2, we'll define a data strategy and in parts 3 and 4, we'll discover what an implementation looks like and what to do if you already have data
infrastructure and need to turn the ship around in order to solve common data problems.*