---
layout: post
title:  "NBA Stats Deep Dive"
author: Ryan Corry
description: "My Blog based on the NBA data I found and worked on!"
image: "/assets/images/basketballcourt.jpg"
---

## The Impact of Free Throws

### Where I Got This Data

I am an **AVID** NBA fan. I love the game of basketball; I could watch it all day every day. Part of what drew me to being a stats major was my love of the NBA and how interesting the stats side of the game of basketball really is. There are plenty of advanced stats like a player +/- or a player PER or Players Efficiency Rating. I got the base for my new data set from <a href="https://www.fantasypros.com/nba/stats/overall.php" target="_blank">Fantasy Pros</a>. This base data set included a lot of base stats like points, rebounds, and assists for every player in the NBA. Once I was able to web scrape this base data, I wanted to research the very controversial stat of the free throw line. A common complaint of NBA fans is that certain players manipulate the rules to get to the free throw line more than they should and it is a negative to the game. So, I decided to take a deep dive into the stats behind the free throw line to see if that claim holds any weight!

![Figure]({{site.url}}/{{site.baseurl}}/assets/images/freethrow.jpg)

### Total Points vs Non-FT Points

The First thing I had to do was convert all of the data points outside of player from a string to numeric, this will make it possible for me to run tests and calculate new data types. The first thing I wanted to know is if there was a massive change in a player’s total points if you took out their FT points, I made a new column in my data set called ***Non-FT*** which simply was the players total points – their FT made. I then made a scatter plot, seen below, that shows the difference. There wasn’t that strong of a slope change for the majority of the players, but for some of the upper tier scorers, the ones who have scored the most, there is a significant drop in their total points vs their non-FT points. This is expected though, because if you are one of those upper tier scorers you have the ball more often than not and so it is natural for you to get more FT’s. 

![Figure]({{site.url}}/{{site.baseurl}}/assets/images/FT-vs-Non-FT.jpg)