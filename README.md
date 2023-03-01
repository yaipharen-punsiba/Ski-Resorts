# Finding The Right Ski Resort (Power BI)

Youtube link: https://youtu.be/d-kZvuM__x4

## About this project
An interactive one-page dashboard on Power BI to explore and eventually find one's desired Ski Resort across the world.

## GOAL:
The goal here is to make, for Skiers, Skiing enthusiasts and families, an easy-to-explore-and-find the right Ski Resort that fits their best choices.

## BRIEF ABSTRACT OF SOLUTION:
1.An attempt is made to build a user(skier)-friendly one-page dashboard to help them in their decisions on selection of Ski resort with respect to
  * Their budgets
  * Choices of seasons
  * Locations and their heights
  * Modes of transportation
  * whether child-friendly or not
  * Availability of snow-parks and level of difficult slopes.
  * Percentage of time in each months covered with snow.
  * 
## ONE OF THE TOUGH CHALLENGES:
* Developing relationships between the two tables - "resorts table" and "snow table"
* 
## SOLUTION (Exploration and transformation):
* Looking at the values of latitude and longitude in the snow table, I NOTICED that their values AFTER decimal points were one of these: 125,375,625 and 875 which, in fact, are mid points of intervals 0-250, 250-500, 500-750 and 750-1000 respectively.
* And so, some changes has been made in the data in the power query as per my mental approach -
  1. Firstly, new latitude and longitude columns are inserted in the resorts table, whose values are tweaked to the nearest latitude and longitude values found in the snow table (using conditional column)
  2. Secondly, a new - snow table is created by merging (LEFT OUTER JOIN) snow table and resorts table and inserted only resort ID and resort name columns (from the resorts table) based ON the the new latitude and longitude values in the resorts table.
* The purpose of this was to make it easy to establish relationship (in our data model) between the two tables using either resort ID or resort name.
* The rest is loading to and building report (dashboard), including creation of few basic measures.

## LIMITATIONS:
Although the new tweak in the latitude and longitude values are informative, it doesn't represent 100% accurate snow cover percentage.
Thank you so much for your time in getting to learn about this project.

## Prerequisites/Dependencies
1. The ***Data sources settings*** to need to be changed to proper locations where the relevant files and folders (data sources) are saved/located.

#powerquery #datamodeling #powerBI #datavisualization #dataanalysis
