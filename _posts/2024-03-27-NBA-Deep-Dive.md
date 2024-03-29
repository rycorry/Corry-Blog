---
layout: post
title:  "NBA Free Throw Deep Dive"
author: Ryan Corry
description: "Countless NBA fans hate when a team is shooting too many Free Throws in a game, I took a deep look into the data to see if there was any credit to the claims that certain teams or players shoot more free throws than others and which teams are the best if you took out the free throw completely."
image: "/assets/images/hoops.jpg"
---

## The Impact of Free Throws

### Where I Got This Data

I am an **AVID** NBA fan. I love the game of basketball; I could watch it all day every day. Part of what drew me to being a stats major was my love of the NBA and how interesting the stats side of the game of basketball really is. There are plenty of advanced stats like a player +/- or a player PER or Players Efficiency Rating. I got the base for my new data set from <a href="https://www.fantasypros.com/nba/stats/overall.php" target="_blank">Fantasy Pros</a>. This base data set included a lot of base stats like points, rebounds, and assists for every player in the NBA. Once I was able to web scrape this base data, I wanted to research the very controversial stat of the free throw line. A common complaint of NBA fans is that certain players manipulate the rules to get to the free throw line more than they should and it is a negative to the game. So, I decided to take a deep dive into the stats behind the free throw line to see if that claim holds any weight!

![Figure]({{site.url}}/{{site.baseurl}}/assets/images/freethrow.jpg)

### Total Points vs Non-FT Points

The First thing I had to do was convert all of the data points outside of player from a string to numeric, this will make it possible for me to run tests and calculate new data types. The first thing I wanted to know is if there was a massive change in a player’s total points if you took out their FT points, I made a new column in my data set called ***Non-FT*** which simply was the players total points – their FT made. I then made a scatter plot, seen below, that shows the difference. There wasn’t that strong of a slope change for the majority of the players, but for some of the upper tier scorers, the ones who have scored the most, there is a significant drop in their total points vs their non-FT points. This is expected though, because if you are one of those upper tier scorers you have the ball more often than not and so it is natural for you to get more FT’s. 

![Figure]({{site.url}}/{{site.baseurl}}/assets/images/FT-vs-Non-FT.jpg)

### Group By Team's Average FT's Per Player

The next thing I wanted to see is which teams averaged the most FT's per player. I grouped each player by their team which I had to extract from the player column. Then I took the average free throws made (FTM) per team and threw those into a histogram. It was interesting to see that there was a clear-cut number one team, the Los Angeles Lakers. They average **84.89** FTM per player on their team. The rest of the top-5 is as follows, the Philadelphia 76ers at **81.94**, the Milwaukee Bucks at **81.5**, the Miami Heat at **77.27** and the Atlanta Hawks at **76.78**. This conclusion is not very surprising at all because these 5 teams are some of the most talked about teams when NBA fans talk about drawing fouls an abnormal amount of time. LeBron Janes, Joel Embiid, and Giannis Antetokounmpo are three of the best players in the world, but they are also three of the most notorious players when it comes to baiting fouls to try and get to the free throw line.

![Figure]({{site.url}}/{{site.baseurl}}/assets/images/teamFT.jpg)

### Group By Team's Average Non-Ft's Per Player

After looking at teams FTM overall, I wanted to look at which teams are the best at scoring the ball outside of the FT line, so in a similar manner to the graph above. I took the same groups of players by their team and took the average ***Non-FT*** points per player for each team. I plotted these into a histogram and the results were very interesting. 4 of the 5 teams that were at the top of the Free Throw Made stat, were not in the top-5 of the non-FT stat. This is very telling and would imply that if those teams did not get as many FT’s as they do, their offense would be significantly worse, and their team overall would struggle more. As for the non-FT stat, the Boston Celtics were **BY FAR** the highest scoring non-FT team, with an average of **459.41** pointer per player, the difference between the Boston Celtics and the 2nd place team is over double the difference between the 2nd place team and the 5the place team. The rest of the top-5 are as follows, the Los Angeles Lakers at **436.27**, the Indiana Pacers at **435.88**, the Oklahoma City Thunder at **431.94** and the Golden State Warriors at **428.71**.

![Figure]({{site.url}}/{{site.baseurl}}/assets/images/teamNonFT.jpg)

### Conclusion

In conclusion, there isn’t much data to imply that certain players are getting dramatically more free throws than any of their peers, but what is interesting is that the teams are the best at getting to the free throw line to be able to get those ***”Easy”*** points, are no where near the top of the league when it comes to scoring beyond the free throw line. The Los Angeles Lakers are the only team in the top-5 for free throws made and non-FT points. This could also be because of the Lakers abnormally high free throw numbers; the opposing team is in foul trouble more so they can not play as physical of defense. But that would need to be something I study in the next blog. Overall, if you are an NBA fan who hate constantly watching players shoot free throws, watch the Boston Celtics, they have the best scoring offense in the league and the best offensive rating of all time as of the time of this blog being written at **122.5**<a href="https://www.nba.com/stats/teams/advanced-leaders" target="_blank">NBA.com</a>! The Boston Celtics have a generational team and offense, so if you want to watch a great team get some great shots and score a lot of points, the Boston Celtics are for you!

![Figure]({{site.url}}/{{site.baseurl}}/assets/images/Celtics.jpg)