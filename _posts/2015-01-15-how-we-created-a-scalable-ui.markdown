---
layout: post
title:  "How We Created Scalable UI - A Case Study"
date:   2015-01-15
categories: case-study
author: juhani
tags:
- UX
- Case Study
---

In this article I want to introduce few of the solutions we used at Onefootball to a create scalable UI that works seamlessly across a broad range if Android devices.

<!--more-->

I rarely get to write about projects I've been involved with myself so writing this one makes for a pleasant change. For more than a year I've been working as a consultant embedded as a part of a very talented Android design and dev team at Onefootball. Onefootball, an awesome startup based in Berlin, have been developing apps for multiple platforms to bring football (soccer for my American readers) news, statistics and results to their users.

[DOWNLOAD THE APP FOR FREE FROM GOOGLE PLAY](https://play.google.com/store/apps/details?id=de.motain.iliga)

As a company, Onefootball has great ambition to do things right and be the best football app on every platform. This ambition is found from the management to the design and development team. A bit more than a year ago it started to become clear that an Android app wasn't good unless it utilised larger screens as well. That is when I joined the team.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-fc-bayern.png" title="Onefootball FC Bayern" width="800"/>

The app is extremely rich with content. The amount of leagues and competitions available to users to browse for is mind boggling. Each of the competitions comes with massive amount of data complete with full season history, match data, team compositions, player statistics for each player and news related to teams and competitions.

### Scalable design

Arranging this amount of information is not easy. Creating responsive UI to accommodate all the different data display variations required us to use multiple different approaches. In this article I want to introduce few of the solutions we used to a create scalable UI that works seamlessly across a broad range if Android devices.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-bundesliga.png" title="Onefootball Bundesliga" width="800"/>


<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-live-ticker.png" title="Onefootball Tabs to Columns" width="300" align="right"/>

### From tabs to columns

A lot of the app's content is split into multiple content sections that exist at the same level of the information hierarchy. On a smaller screen the natural component to use is a tab bar. For example the match screen shows things like the match overview, live ticker, line-up and stats.

Each tab's content is created as a flexible screen that spans the width of the screen on most phone sizes.

To get the match screen ready for larger screens the approach we chose to take was to remove the tabs altogether and show the tabs as columns which forms horizontally scrolling content. This created a display that easily scaled up to any tablet size and utilised the available screen space without feeling like the components information was cramped or constrained by space.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-lineup.png" title="Onefootball Lineup" width="700" align="center"/>

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-fc-bayern-phone.png" title="Onefootball FC Bayern" width="300" align="right"/>

### Tabs to tabs

On other screens with a similar structure we went a different way. This was when the content of the tabs itself was nicely scalable and was able to utilise the available screen real estate.

Many screens like the match screen were perfect for this. The content of each tab was already using card-style layouts and simple reorganising the way the cards are laid out in the screen allowed us to utilise the full screen on larger devices.

In some cases we also adapted the content of the cards to limit the amount of information shown when space is more limited. In this case, for example, the number of teams shown in the competition table is only three when on a smaller screen device and on larger screens we can show more. The full table is only a tap away for the users who want the complete information.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-fc-bayern-tablet.png" title="Onefootball FC Bayern" width="700" align="center"/>

### Cards are flexible

It's not an accident that a lot of Android apps use card-style visuals to show their content. Cards are easily arranged into flexible layouts and scalable UI forms itself nearly automatically.

Content like news articles with rich visuals and mixed sources create a great opportunity to use staggered list-style approach to create visually pleasing, content rich screens.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-fc-bayern-news.png" title="Onefootball FC Bayern News" width="200" align="left"/>

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-fc-bayern-news-tablet.png" title="Onefootball FC Bayern News" width="550" align="right"/>

In some cases simply arranging the cards wasn't possible. If the cards used are different in size and must maintain strict chronological order using a staggered list is not the right way to display them. For us, the solution was to break some of the cards into smaller content components and show them as a grid.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-matches-phone.png" title="Onefootball Matches" width="200" align="left"/>

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-matches-tablet.png" title="Onefootball Matches" width="550" align="right"/>

In some cases the smaller screens displayed the content in a simple list while for larger screens we utilised grid-like layouts. This is something Google advises against in the Material Design guidelines but in this case we decided to break from the guidelines as this created the best possible scalable result.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-bundesliga-phone.png" title="Onefootball Bundesliga" width="200" align="left"/>

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-bundesliga-tablet.png" title="Onefootball Bundesliga" width="550" align="right"/>

### Viewpager is easy to adapt

Viewpager is a very powerful component. On the team screen we wanted to show recent and upcoming matches.

For smaller screen widths we only show one match and a small slice of the next one to communicate to the users that there's something more just a swipe away.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-fc-bayern-team.png" title="Onefootball FC Bayern" width="400" align="center"/>

When there's enough screen width to fit more than one match comfortably we adapt the viewpager to show two or three pages to reveal more information to the user.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-fc-bayern-team-ls.png" title="Onefootball FC Bayern" width="700" align="center"/>

### Adaptive navigation

In some cases we chose to change the navigation hierarchy slightly when user was on a larger device. 

For example in case of the list of matches, we made the selection in the mast screen open a quick view of the match instead of navigating directly to the match page (like it does on smaller devices). This allows users to browse multiple matches more easily while still making it easy to jump into the full match page when the user desires. 

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-matches-tablet2.png" title="Onefootball Matches" width="800" align="center"/>

On the competition stats detail page we improved navigation between the different stat details on larger screens. Larger screens meant there was empty space on both sides of the list and it felt like a natural place to place quick navigation to the other details pages.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-assists-phone.png" title="Onefootball Assists" width="200" align="left"/>

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-assists-tablet.png" title="Onefootball Assists" width="550" align="right"/>

For the competition matchday list we ended up using a dropdown navigation on smaller screens but larger screens have room to show the matchday list on the side allowing user to jump between the matchdays more easily.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-bundesliga-match-phone.png" title="Onefootball Match" width="200" align="left"/>

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-bundesliga-match-tablet.png" title="Onefootball Match" width="550" align="right"/>

### User Delight

Going for good app to a great app requires more than just nice scalable UI. You need to delight your users. In case of Onefootball a lot of details were added to the app to push it from being good to great.

In a football app the right place to start making users delighted is the team page. Onefootball app affords each team a fully themed page. A fan of any team will immediately recognise the colour theme and prominent team logo.

<img src="{{site.baseurl}}/blog/images/2015-01-15-how-we-created-a-scalable-ui/onefootball-team-screens.png" title="Onefootball Teams" width="700"/>

The team page was also improved with subtle but meaningful behaviour. The header of the page transforms into toolbar when scrolled. Lollipop's activity transitions were also spot on for this content. The hero element transition is both delightful as well as helpful.

<iframe width="780" height="475" src="https://www.youtube.com/embed/eyqJIKUShJA" frameborder="0" allowfullscreen></iframe>

<br/>

### Conclusion

The Onefootball was great fun. Working with a company that wants to do Android right is rewarding. The results are something I can be very proud to have been part of. Elegant Android scalability can be challenging but approaching it the right way makes it possible to get great results. There are pitfalls but they are avoidable. In our case the app ended up being featured multiple times - most recently as the Editor's Choice in the Google Play Store and in the Google's 2014 Best Apps List.

