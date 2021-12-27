---
title: How I (finally) Changed The Template Chirpy Avatar
date: 2021-12-27 20:30:00 +0900
categories: [DailyBlog, HowTo]
tags: [it, tech, blog, daily, til, jekyll, chirpy]     # TAG names should always be lowercase
---

>This post will cover how my understanding of Jekyll increased slightly, and how I managed my way into setting up this awesome Jekyll Template for my Github Pages personal website.  

Shout-out to Chirpy Theme's creator [Cotes on Github][1].  

It is this very theme that I am using on this blog. I thought this was sleek, easy, and neat to put up.  

So I get onboard the hype train (just me riding it alone in my dark room), and this wasn't my first time ever trying to install a Jekyll theme properly onto my Github Pages. A little embrassing that I have tried to Jekyll few months back which ended quite abruptly with a disgruntled me, a headache, and more procrastination.  

Spoiler alert, I succeeded this time.  
  
  &nbsp;
>**It Was All Going As Planned**

Although there was success, I felt the need to share the frustration I had while following the guide in [changing the favicon][2]. It may be my lack of knowledge. But I had **0 clue** how Jekyll publishes websites (*now* I can get a sense of it).  

I wanted to change the cute little Chirpy avatar to something that would represent me more. I was like *"Well, there's a nice little guide on how to change it. How hard could it be ?"* 
  
  &nbsp;
![You almost gave me another headache, Chirpy](/assets/img/posts/2021-12-27-A/chirpy-avatar-capture.png)
  &nbsp;
>**Just Needed One Line of Hint**😭

So, it turns out that I had no idea files under `_site` folder gets reproduced every build. Now it seems obvious to me, but back then... not so much. As per instruction, I continuously tried to put my avatar and favicons into `_site/assets/favicon` since that was the only asset folder I could find. 😂 It got erased everytime, and almost gave me a headache.  

![Just needed one hint from the guide](/assets/img/posts/2021-12-27-A/customize-favicon.png)
  
  &nbsp;
**I now realize that the we needed to put any static content inside `assets` folder at the root folder. Any content within `_site` gets rebuilt EVERYTIME.**

Or any other named folder. While stackoverflow did suggest the above fact, I just didn't know if I needed to make an `assets/` folder to my discretion! (maybe it was somewhere else in the guides, and I missed it)  

I created and put all my images into the `assets/img/` folder, and voila! All was good.
  
  &nbsp;

:-------------------------:|:-------------------------:
![Project File Tree](/assets/img/posts/2021-12-27-A/project-file-tree.png)   |  ![Project File Tree](/assets/img/posts/2021-12-27-A/project-file-tree2.png)



As you can see, the created `assets` folder contains the static img content. And its image was properly replaced Chirpy.  
  
The `_sites` folder is grey (not tracked by git) which an intelligent person (not me) would obviously fiddle with. But I did. And I was able to learn a few things about Jekyll -- the hard way.

Aaaand... That's it!  
Thanks for reading!  
  
Hopefully this was able to help somebody 😁  

[1]: <https://github.com/cotes2020/jekyll-theme-chirpy#usage> "Chirpy Theme for Jekyll"
[2]: <https://chirpy.cotes.info/posts/customize-the-favicon/> "Guide on customizing favicon for Chirpy"