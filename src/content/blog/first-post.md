---
title: "Figuring out an FPGA"
description: "A blog/diary of me learning to use the Altera DE2 FPGA"
pubDate: "Sep 12 2025"
heroImage: "../../assets/FPGA.jpg"
---

## Introduction

Heya. This series of blog posts is about my exploration with the Altera DE2 development and education FPGA board! Why this one? We'll get to it!

Let's start somewhere else: Why am I even exploring FPGA boards? As an Electrical Engineering student, some of my fields of interest have been:
- Communication systems
- Signal processing
- Programming (Especially low-level things like drivers)
- The interaction between the physical and digital world


There are other things I've found enjoyable, but they're not super related to Electrical Engineering (things like scientific computing and data analysis come to mind!). A possible way to explore all the above fields is via an FPGA, and thus, the course is set. (I must also say that I have used an FPGA before, in class. Specifically the [Zybo Z7](https://digilent.com/reference/programmable-logic/zybo-z7/start), however, I desire to do some exploration on my own, and so here we are.)

So, FPGAs, where to start? Firstly, finding an actual board seems like a good idea. Luckily, I study at a pretty awesome university, and so they have a giant stock of, well, everything an Electrical Engineer could ever dream of, free to borrow! For FPGAs, there was basically just the one option, [an Altera DE2](https://www.terasic.com.tw/cgi-bin/page/archive.pl?Language=English&CategoryNo=183&No=30&PartNo=1#contents). While it is quite old, it does have some awesome features, including a 16x2 LCD panel. This will do nicely!

## Configurable Clock Counter

Before starting this section properly, I have to admit that this first blog post is written at a later time, since I only got the idea to do this blog afterwards. However, all the later posts will be written during the exploration. With that out of the way, let's begin!

The first thing to do, is to get a good idea for a project! Actually, the real first thing to do, is figure out how to hook up this ancient piece of hardware to modern technology. All the info that came with this thing is from 2006, and on a bloody CD. So:

![One Research Later](../../assets/one_research_later.png)

And we're back. It seems like the best option is [Intel's Quartus II](https://www.intel.com/content/www/us/en/software-kit/711791/intel-quartus-ii-web-edition-design-software-version-13-0sp1-for-windows.html), though it has to be a slightly older version, since they discontinued support for architecture of my FPGA, which is called Cyclone II... Hm. Anyways, let's install it.

![Skeleton waiting at a PC](../../assets/waiting_skeleton.jpg)

Dang that took a while. With that out of the way, it is now time to figure out how to actually use it. I watched [this youtube video](https://www.youtube.com/watch?v=auQ7wpVH-0Q) from 2012, however basically nothing has changed with the software since then. I guess enterprise software has a much longer half-life than basically the rest of the software world. Huh. 

There is just one last thing to do before actually getting started though, there is a choice to be made. What language? I will be using [VHDL](https://en.wikipedia.org/wiki/VHDL), since it's what I used in class. I might try [SystemVerilog](https://en.wikipedia.org/wiki/SystemVerilog) in the future though. However Quartus actually supports surprisingly many Design languages, including basic block diagrams!

# TO BE CONTINUED