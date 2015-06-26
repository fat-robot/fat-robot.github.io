---
layout: post
title:  "Hackathlon: a weekend well spent"
date:   2015-06-25 10:03:22
categories: google
author: lina
tags:
---

#Hackathlon: a weekend well spent


Not having attended a hackathlon before, I was torn. My summer weekends for me are usually fully booked with outdoorsy activities- however, spending a weekend with a bunch of other nerds, doing something we love powered by delicious Augustiner beer and Club Mate did sound pretty great.

The 2015 Wearable Data Hack (http://wearabledatahack.com/ ) was, as the name says, focused on wearables. Mobile devs, designers and data guys joined together to hack away some cool wearable-focused ideas.

As expected, the hackathlon was a great way to get to know wearables better. It creates a perfect environment to experiment, collaborate, and brainstorm ideas with like-minded people.

After some brainstorming and idea pitching, people teamed up to start making these ideas happen (though a few of us ended up going on a solo mission).

The Project: Stitch Counter

The key is to start off with a simple idea that is doable in the time frame. An idea you are passionate about. For me, this idea was to create a counter for smartwatches that helps me keep track of the stitches while knitting.

This is how the final product looks like: 

TODO Copy device screenshots here 

To get there I followed these steps:

Step 1: might sound trivial but sometimes takes longer than you’d like: setting stuff up. 

Step 2: Designing a UI. For this I followed the KISS principe (keep it simple, stupid). One the Stitch Counter is launched you just get a screen that says “go!” and when you tap on this you get the counter.

Step 3: Figure out how to “count” a stitch by tracking the wrist moments. For this Juhani Lehtimäkis Sensor Dashboard (link to play store) was a great help. It helped me choose a sensor that best served my purpose and figure how the data the sensor delivers looks like. Once I got this running I achieved the minimal viable product: a stand alone stitch counter. The biggest challenge in the whole weekend was to get the counter to work accurately. It is necessary to gather more data from other knitters to calibrate more precisely.  

Step 4: Bi-directional communication. Having a stand alone counter is cool, but even cooler is having the counter guide you through your knitting pattern. Outside of the hackathlon contest I had developed an app to create knitting patterns, so I decided to extend it with the Stitch Counter. From the existing pattern, I implemented a way to launch the Stitch Counter on the smartwatch and start counting away.

The Result

It was a very rewarding and fun experience, and hey, I got second place :)  
And of course, the weekend came to a perfect end when we wrapped things up with some Augustiner Beers.


