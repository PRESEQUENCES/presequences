---
layout: post
title: Some Passing Notes on Data Sonification
date: 2026-04-07 04:30
summary: 
tags: data sonification, music
---
I have a complicated and probably cynical opinion about data sonification. In the abstract it’s a really cool concept; instead of looking at raw data, you listen to it. Practitioners of data sonification are insistent. Some insist that it is more than a mere parlor trick. Others insist that it’s a useful tool for understanding and communication. I think they’re mostly wrong.

Benn Jordan recently made a plugin for VCV Rack[^patreon] that turns stock market data into CV, letting you listen to the fluctuation of stock prices over time.
He posted [a video demo on Instagram](https://www.instagram.com/p/DWCdsPvEfma/){:target="_blank"} that caught my attention because it was quite compelling — particularly by how tidily it exposed what I consider the fatal flaws of data sonification. 

The video provides a textbook definition of sonification (stock price as pitch), and/yet/but relies on text labels and a graph of the stock price over a time period. Each example is provided with context and editorialized. Alongside all of that information the sonification is an additional interpretation; but one with dubious value of its own. And this is kind of my point. 

The data visualization of the stock price (i.e. line graph with axis labels) is self-explanatory. A summary table of stock prices is self-explanatory as well. Granted, without the labels or column headings, those visualizations are an arbitrary line and a matrix of arbitrary numbers. But we’re talking about communicating a “data story” — visual vs. sonic. Sonification requires textual or graphic context. Let that marinate.

The video also demonstrated the more artistic side of sonification — albeit simplistic. To be clear, I’m not trying to trash Benn’s video. He did what most musicians do. He simply used the data as a modulation source for sound design. Fluctuating numbers are just like random voltages that you can limit, invert, attenuate, average, normalize, and quantize those signals. This begs the obvious question: why bother with data in the first place?

Most intentional sonification projects seek to tell a story that is based on the data. This requires establishing a rational relationship between the data and the sound so that meaning of the data can be communicated by sound . A simple example of this is using stock price for the pitch of a sound. Higher numbers are better than lower numbers, so higher pitched notes signify higher stock prices — simple. Now consider using a dataset of crime statistics where murder rate is used to modulate the pitch. In this case the relationship between the data and the sound, a more apt choice might be the inverse. Crafting a sonification that is faithful to the data requires establishing a consistent, cohesive, and thorough set of these types of relationships. 

This is the artistic conceit. It allows us to imbue a deeper meaning. Like: that bass line is being played by the murder rate in St. Louis, or  the low pass filter opens according to the time of sunrise, or the pace of a sequence changes with the number of new homes built in flood zones. Absent any justifiable basis for those decisions, it’s not much more than arbitrary. At best, it’s a parlor trick, and I think Benn’s video showed off the parlor trick perfectly. I don’t blame him for avoiding the semantics. After all he was doing a technical demo, not whinging endlessly about how most sonification projects are intellectually bankrupt.

I don’t mean to sound entirely critical of the practice. If this were a different conversation, I’d probably use the word agnostic. As a tool for data science, I have a difficult time seeing its utility. Data visualization can be used to explore and analyze data as well as communicate a data story. The visualizations can be static or animated. A visualization can be “read” instantly.[^cholera]

As a tool for musical composition or sound design, it can be a source for truly thoughtful and novel innovation. It’s not easy to do correctly, and it might be impossibly hard to do it well. But, if you’re at all curious, I encourage you to give it a shot. Even if the result isn’t notable, the effort and the process are worth knowing.

### Here are some resources to get started:

- If you’re interested in the field of sonification, check out [Loud Numbers](https://www.loudnumbers.net){:target="_blank"} — a sonification consultancy started by Duncan Geere and Miriam Quick. They have a blog, a podcast, a [VCV Rack plugin](https://library.vcvrack.com/LoudNumbers/LoudNumbers){:target="_blank"}, and a hosted [Jupiter Notebook](https://observablehq.com/@duncangeere/data-mapper){:target="_blank"} that helps you map CSV data to an indexed range (sounds boring but it’s a crucial task made dead simple).
- [csv-to-midi](https://csv-to-midi.evanking.io){:target="_blank"} is the easiest way to convert CSV to midi.
- If you use Ableton 12, check out this [CDM article](https://cdm.link/sonify-data-in-ableton-live-with-a-free-midi-tool/){:target="_blank"} about a M4L midi generator tool called [Datafree](https://manifest.audio/datafree){:target="_blank"} (and how to get access to publicly available datasets).
- TwoTone is a web app that makes it easy to try sonification. You can upload your own spreadsheet or use their example datasets, and it will generate midi and audio. The authors of the tool are clearly searching desperately for a business plan, so if you try it and like it, clone the repo and self-host it before it vanishes. See what I mean by going to the [official site](https://twotone.io){:target="_blank"} (pop-up typeform... no thanks)… but here’s [a direct link to the TwoTone app itself](https://twotone-midiout-beta.netlify.app){:target="_blank"}. 

---

[^patreon]: The plugin is only available to his [Patreon subscribers](https://www.patreon.com/posts/i-made-dumb-vcv-153373727){:target="_blank"}. 

[^cholera]: I’m thinking of [Dr. John Snow](https://education.nationalgeographic.org/resource/mapping-a-london-epidemic/){:target="_blank"} who in 1854 mapped the cholera cases around Soho and was able to identify the water pump that was responsible for the outbreak.
