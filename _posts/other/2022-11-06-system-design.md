---
layout: post
title:  "The Best Way To Prepare For System Design Interviews"
author: david
tags: [systemdesign, interview]
image: "assets/images/articles/sd_resources/hadoop.png"
---
The ambiguity of system design interviews can be daunting for most candidates. I've never formally studied computer science and when preparing myself for system design interviews, I was a bit surprised by the lack of concise and practical study information. The first system design interview that I ever experienced was an utter failure. I had no idea how to do a back of the envelope calculation to determine my system requirements or even knew how long a round trip would be from client to server. <br /><br />
Now, after a month of studying and a month of applying, I've received numerous offers from companies such as Databricks and many accolades about my system design chops. Using the resources that I detail in this article, I strongly believe that anyone can achieve the success that I've had.


# Reading Materials

![sd]({{ site.baseurl }}/assets/images/articles/sd_resources/books.jpg)

I've gone through a few books on System Design including [Azure for Architects](https://www.amazon.com/Azure-Architects-scalable-high-availability-applications/dp/1839215860/ref=sr_1_1?crid=12CW5IJF66BK3&keywords=azure+for+architects&qid=1667748601&sprefix=azure+for+architects%2Caps%2C104&sr=8-1) and [Designing Data-Intensive Applications](https://www.amazon.com/Designing-Data-Intensive-Applications-Reliable-Maintainable/dp/B08VL1BLHB/ref=sr_1_1?crid=3A27FXVFC5QM4&keywords=designing+data-intensive+applications&qid=1667748648&sprefix=designing+%2Caps%2C108&sr=8-1). However, the most practical book that I've ever read on System Design has been [System Design Interview](https://www.amazon.com/System-Design-Interview-insiders-guide/dp/B08B35X2ND/ref=asc_df_B08B35X2ND/?tag=hyprod-20&linkCode=df0&hvadid=598359496472&hvpos=&hvnetw=g&hvrand=9968472418848449604&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9061312&hvtargid=pla-1041143569357&psc=1) by Alex Xu.<br /><br />
Alex Xu's guide is an easy-to-read 300-page book in a small paperback form. It's packed with practical information such a table of rough estimations of general computations and processes such as an estimate for how long an L1 cache reference takes or a packet roundtrip from California to the Netherlands. It goes over many fundamentals such as consistent hashing, vector clocks, and rate limiting techniques before diving deep into common interview questions such as building a social media feed system and creating a web crawler. Almost each page contains an image so that you can verify your understanding as you go along and each chapter is short with concise summaries.<br /><br />
This book has become my little pocket bible and I always consult it before an interview for a last minute refresher.<br /><br />
Alex Xu has also published a [System Design Volume 2](https://www.amazon.com/s?k=system+design+interview+volume+2&i=stripbooks&crid=3USWV9XLWVRMQ&sprefix=system+design+%2Cstripbooks%2C113&ref=nb_sb_ss_pltr-ranker-lnopsacceptance_3_14). It is a terrific read, detailing the designs of many complex systems including Google Maps. This book is less digestible and less applicable for a typical system design interview but contains some very specific designs that have come up in my interviews such as a payment system and hotel reservation system. I would strongly encourage you to read volume 1 first though as volume 2 builds upon many of the concepts from volume 1.

# Online Resources

![pay]({{ site.baseurl }}/assets/images/articles/sd_resources/pay.jpg)

There are many great online resources to help sharpen your system design toolset. Donne Martin's [System Design Primer](https://github.com/donnemartin/system-design-primer) repo contains many useful examples of system design problems with an in-depth analysis of how to go about approaching the problem and iterating on your solution.<br /><br />
[Pramp](https://www.pramp.com/dashboard#/) is a great online resource for practicing interview questions. You can practice with peers for free on pramp. You and your assigned partner take turns answering interview questions and each session is about 80 minutes long but you and your partner are free to set limits. Pramp provides system design, coding, and behavioral interview practice.<br /><br />
These are the primary resources that I would suggest. There are also many paid resources, such as [interviewing.io](https://interviewing.io/). On interviewing.io, I've spent about $500 for 2 mock interviews. These interviews were not very challenging and I found the feedback to be quite basic. However, interviewing.io also has a free peer-to-peer option as well which may be comparable to pramp. I love the idea of paying for professional and detailed interview prep, but this unfortunately was a bit of a waste of money to me. Perhaps, the dedicated coaching sessions($4000+) are more beneficial.
<br /><br />

# Conclusion
A System Design interview is like a box of chocolates. They are often so unstructured, that it's difficult to determine how your interviewer will grade your performance. They most important steps are to
1. Ask MANY questions about the functional and technical system requirements and priorities of the problem
2. Come up with a basic design that meets those requirements
3. Iterate on and improve your design with performant architecture components (such as caching and message queues)
<br />

With these resources, I'm absolutely sure that you will rock the system design interview! Stay calm, keep your interviewer engaged, and best of luck!
