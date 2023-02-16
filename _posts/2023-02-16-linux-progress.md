---
title: "Linux Makes a Great Audio Workstation"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - thoughts, gear
---

Everything I've found online advises against using Linux for pro audio.  All I can say is that for me
Linux not only works great, it works better than Windows.

<!--more-->
Over a week ago I set out to buy an inexpensive machine and experiment to see how well it could 
substitute a digital audio workstation running in Windows.   

I will tell you upfront that it was an overwhelming success.  However, it was not easy.   

## The Problems

As with most things linux there are just so many options.  A newbie is absolutely drowning in
possibilities.  What distro will you use?  Will you use a realtime kernel?  What audio server?   

And there is no 'all in one guide' here because nobody knows what you need.  Are you going to run
Windows VST plugins? Maybe you'll need yabridge.  etc. etc.

### The Choices I made

* **Operating System** - For my part I wanted a very lean operating system so that I could dedicate as
much computing power to my audio software as possible.  I don't need a bunch of windows with rounded
corners swishing about.  So I started with Ubuntu server as a base.  The first thing to do after
installing Ubuntu server is to remove all the cloud faff they pack in.

* **Window Manager** - Like all Linux bubbies worth anything I'm using DWM and the ST terminal.

* **Optimizations** - I installed a realtime kernel and the rtkit package.  I also passed some kernel
parameters for optimization.

* **Audio Server** - Pipewire baby.

* **DAW** - Reaper.

## Challenges

The biggest mistake that I made was that I didn't know you do not make an 'audio' group and assign
your user to it when you are using pipewire.  The group has to be called 'pipewire' and you have to
give that group realtime permissions.   

Also, when I installed yabridge and brought in my favorite Windows plugin the interface would not
redraw.  Apparently many of the new plugins developed with the JUCE framework expect vulcan and
wine is not using the vulcan drivers out of the box.  Not a difficult fix but takes some legwork.

Finally, None of the Izotope products work in wine.  Their insistance on DRM and an all powerful
manager just for their products really screws everything up.  Thankfully they do not have anything
that cannot be substituted.  If you're on Linux don't buy Izotope plugins.

## So What's the Deal Pickle?

Well I have Reaper reporting a 4ms latency with the Pipewire server.  With the exact same settings
on my Windows machine I get 10ms.  Now consider that the Windows machine has an 11th generation
i7 processor and it's getting bested by a box with a 6th generation i7 processor.   

And the Linux machine simply runs better.  It does everything better.  And why shouldn't it?
It was designed at every step of the way for this specific application.  That is why the job was
so difficult wasn't it?  Turns out excellent engineering is difficult.  But the payoff is huge.