---
layout: post
title: Today I Made a SWF animation
excerpt: How I quickly created an outdated solution for a current platform.
---
A decade and a bit late, but I’ve finally got my hands dirty and created a SWF video from (nearly) scratch. It was relatively painless … except for one silly part, but I’ll get to that.  

There was a need for an overlay on a site today at work and due to miscommunication between offices in different parts of the world and the impending deadline, I ended up creating the overlay which is normally outsourced. I don’t know anything about Flash, ActionScript, or how one goes about editing an SWF file. But I know where to go when one is stuck.  

Some Googling got me to a freeware called [JPEX Free Flash Decompiler](http://www.free-decompiler.com/flash/) (FFDec), which ended up being really useful (see, I can’t get Adobe Flash on a whim on a work computer, (un)fortunately). I found an old overlay, opened it with FFDec and started poking around the innards of the SWF file.  

The interface was part WYSIWYG, part IDE. After figuring out its logic (somewhat), I began to play around with the parameters and got in on the action with ActionScript – not scary at all and in fact quite succinct in its syntax.  

I got into one snag, though, which was driving me crazy – somehow only the letters used in the previous version were loaded as font so when I tried to add text, it was coming out in gibberish. I couldn’t figure it out. Googling didn’t help, as I couldn’t find an analogous problem.  

So I dug more and realised that there were a lot of characters missing in the font stack. I started adding the alphabet and the common punctuation marks, which meant now my text was rendering quite well. The end result was as good as I could have done within the time and tools at my disposal, so I was pretty chuffed about it all day.  

Would I want to create more SWF animations? No. But knowing now that I could kinda feels good!  