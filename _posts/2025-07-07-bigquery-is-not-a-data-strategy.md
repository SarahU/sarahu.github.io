---
layout: blogpost
title: "BigQuery is not a Data Strategy"
category: "Data Engineering"
type: "TECH"
filename: /blog/bigquery-is-not-a-data-strategy
date: 07-07-2025
image: /images/manja-vitolic-unsplash.jpeg
imageAltText: "A cat staring intently"
image_attribution: Photo by <a href="https://unsplash.com/@madhatterzone?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Manja Vitolic</a> on <a href="https://unsplash.com/s/photos/nerd-cat?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
---


I've worked in data and reporting since the beginning of my career (2011), and particularly, in the last 7 years,
I've worked with, consulted with or heard from through the developer grape-vine, about problems that:

A - Big Data was supposed to have solved but didn't, and  
B - a set of consistent complaints and problems companies are experiencing with their data. 

My biggest gripe though is the consistency of a certain sales pitch which many companies and colleagues
cling to, in hope that it's all they need to do data well, and that is this idea, that you simply can 
put all of your data into a powerful data warehouse, process your data in there and call it a day. 
Data done.

Ultimately the same problems arise in very company that implements this:
1. The data becomes difficult to manage. Often the team managing and cleaning the data is not the same team who created it
2. The pipeline becomes slow. While these warehouses are very powerful, the pipelines still seem to become slow and cumbersome.
3. The cost becomes a major problem. It's now a trade-off as to whether we pay astronomical vendor fees or degrade any data-backed features or experiences.
4. The funneling of all this important work become a bottleneck in the business, meaning feature building slows and relations with the data team suffer. The data team members also burn out rapidly.

Almost every job I have has in the last few years has been to deal with the aftermath of this implementation.

So where are we going wrong? Surely this solution should suffice for most regular businesses.

In theory, many business can get away with an approach that is fast, but not real time, and can deal with a couple of
Terrabytes of data. The problem comes in because people don't treat data as something that can change.
The importance of data maintenance iis usually an after-thought. It's become a more prevalent concern as more
companies try to make use of their data in AI features, and hope to improve their data analytics. They do not
consider that their data processing tech stack may need to change or be more flexible beyond the ability to scale horizontally
or vertically (ie using bigger and better machines).

We neglect to consider:
1. Scaling using machines is not free
2. Vendor locking
3. That some data may need to move at a different pace of processing than other data.

Much of this is avoidable, by:
1. Storing your Raw data in a standard format, in files.
2. Embracing redundancy
3. Accepting that different datasets will go through different data processing stacks/pipes.
4. Engineering with a data-first mentality.

Storing your Raw data, puts you in position where you can re-play your data, through an entirely differently tech stack,
while maintaining your current implementation. Storing it in files, outside of your warehouse, means that you don't need 
to first extract the data from the warehouse (which costs money).

This introduces redundancy. Yes it's not free to keep files in cloud object storage either, but by paying for
this level of redundancy, you buy yourself flexibility and the ability to more easily migrate onto a new stack when needed.

You can also experiment with processing different datasets through different pipelines, and in fact can be open to 
applying different solutions to different datasets. Large data that needs to move rapidly is better processing
using a cluster technology like Spark, whereas your financial calculations are highly suited to a warehouse flow, with
slowly changing dimensions and aging data.

All of this requires one to look at data not as a by-product of a systems flow or product feature, but as the main element
which is to be considered when designing a solution, from the beginning of the data's life, to its end. 
As we move towards truly data-backed features - not just AI, but features which 
use data to tell customers - they have vouchers to use, suggestions based on real-time behaviour, notifications based on preferences which
were updated 1 second ago, etc.; we must accept that one solution for every types of data, will simply never work.

So, if you're in position to set yourself up for a future of data flexibility, please follow the principles above, but if
like most of my customers, you're caught in the trap of one warehouse to win them all, there is no time like the present to make changes now
and set yourself up for slightly easier future changes. We live and learn :)
