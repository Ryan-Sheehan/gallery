---
layout: post
title: "Blubirdband.com"
description: "Commission for Griswald"
tags: [web design, svg, music]
---

A friend of mine from home (Philadelphia) is in an indie band named Blubird and his band went on tour this summer. They were in need of a website to help spread the word and sell merch so I threw this together:

{% include image.html path="blubird/001.png" path-detail="blubird/001.png" alt="" %}

The main navigation tool for the desktop version of the site is this big svg ribbon that kind of snakes around the page as the user goes between different sections. There's a fair amount of trigonometry involved so I'll save you the Algebra 2 lesson and just say that it wouldn't have been possible without [Snap.svg](http://snapsvg.io/), a framework for working with SVGs.

Since I knew the ribbon wasn't going to work as well for mobile, I opted for a more simplistic menu button. However, I still wanted something unique for the landing page so I tried implementing a kind of hacksaw version of a feature that had really stood out to me earlier on [Warby Parker's](https://www.warbyparker.com/) mobile store. When looking at a pair of glasses, if the user tilts their phone, the model's head will tilt accordingly so that different perspectives of the glasses are available. But since I didn't have any glasses to show off, I instead used a character from Blubird's lore, Gooseman to attempt this:

Not the prettiest but it'll do the trick.

Another idea I had for the mobile landing page was include a TV interface. At the last Blubird show I went to they had a big projection going on behind them that was playing a supercut of [Binging with Babish](https://www.youtube.com/channel/UCJHA_jMfCvEnv-3kRjTCQXw) while they did their set and I wanted that to somehow make an appearance on the site. 

{% include image.html path="blubird/005.jpg" path-detail="blubird/005.jpg" alt="" %}

What I came up with ended up being to resource intensive to actually be feasible on a mobile connection but you can still check it out [here](http://blubirdband.com/testing/). The bigger knob changes the channel between gifs featuring an old, banned animatic, a snippet from their [latest music video](https://www.youtube.com/watch?v=AJ23Bs29neI), and, of course, Babish. The smaller knob handles other features like turning the TV off, and initiating custom SVG animations.

{% include image.html path="blubird/002.png" path-detail="blubird/002.png" alt="" %}

After doing this I just had to come up with some interface for the actual store section that would sell the merch. I wanted it to feel kind of low tech because this is an indie band and seeing as the music itself isn't highly refined, I didn't want the website to look like it had just come fresh off of Squarespace. 

What I ended up with is this simple flexbox layout featuring Gameboy Colors as the containers for the merch overlayed across an interactive SVG background to keep the ribbon/squiggle motif present.

{% include image.html path="blubird/003.png" path-detail="blubird/003.png" alt="" %}

Now all I had to do was make this site actually capable of handling transactions and since I wasn't about to go write up an entire encryption method for handling credit cards, I just went ahead and used [Chec.js](https://chec.io/) to save myself from having to deal with all that gross and uncessary backend stuff for such a simple site like this. 

{% include image.html path="blubird/004.png" path-detail="blubird/004.png" alt="" %}

First sale done.

Site is hosted on gh-pages because it's static, I'm cheap, and it gets the job done.

Edit: Blubird was just featured in Spotify's Fresh Finds playlist (700,000 followers) so maybe this site will actually get some good use. 

{% include image.html path="blubird/006.jpg" path-detail="blubird/006.jpg" alt="" %}


