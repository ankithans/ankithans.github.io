---
author: "Ankit Hans"
title: "GSoC'21 journey begins"
date: "2021-06-10"
description: "Google Summer of Code 2021 starts with JBoss(Red Hat)"
tags: ["gsoc", "opensource"]
categories: ["GSoC'21 @JBoss"]
ShowToc: true
image: "./gsoc-jboss.png" 
thumbnail: "./gsoc-jboss.png" 
---

## Get started with open-source
![github-timline](https://cdn.discordapp.com/attachments/852928325197234256/852932535117545482/unknown.png)

I myself started with **opensource** in end of the year 2020. Explored a lot of organizations, according to my interest and tech-stack. And I got a list of 20+ orgs, so I took my time, may be a week and gone through the projects of all of them. Then finally I found [LibreHealth](https://librehealth.io/) and [JBoss](https://www.jboss.org/). 

I started my opensource journey with [LibreHealth](https://librehealth.io/). The project was [Cost of Care Application](https://gitlab.com/librehealth/toolkit/cost-of-care/lh-toolkit-cost-of-care-app) which aims to to provide patient friendly costs of care, to help patients get better cost estimates for medical procedures of Hospitals.

I knew [flutter](https://flutter.dev/) before hand and so I did solve some issues and improvements. As I became active member in the [LibreHealth community](https://forums.librehealth.io/) the admins gave me `new user of the month` badge, after some days they promoted my trust level on their forums and this really encouraged me to contribute more to open-source! The maintainers were quick in reviewing my merge requests and this filled me with confidence and persuaded me to apply for GSoC this year.

## How the Journey started with JBoss
![gsoc-with-jboss](https://cdn.discordapp.com/attachments/852928325197234256/852945224166801428/Group_1_2.png)

After a great kickstart in the journey of opensource, I found a project [graphql-link](https://github.com/aerogear/graphql-link) in **Aerogear(JBoss)**. I knew that it was a Golang project overall(PS: I didn't knew how to print hello world in golang), but there were some beginner friendly issues in the repository, like website for documentation([docusaurus](https://docusaurus.io/)), example servers etc.

I started resolving some good-first issues and got in touch with my mentor [Wojciech Trocki](https://github.com/wtrocki). He persuaded me to learn golang and contribute more. I am so glad to have a mentor like him. He helps in every way possible, like giving hints, code reviews, appreciations, guidance etc.

> **After my proposal got selected in JBoss, I got this from my mentor at LibreHealth** and I was in seventh heaven 🤩🤩

![librehealth-chat](https://cdn.discordapp.com/attachments/852928325197234256/852928676826710066/unknown.png)

## Open Source Projects
There are typically two types of projects in open-source.
1. The Project is already there on internet. You need to develop, propose and fix on the top of that.
2. The idea is validated on paper, but still it's not on internet.

My project comes in second category, I have to start everything from the ground level, deciding the architecture, code structure and documentation. In my opinion, this is a little harder to do than the projects in first category. 
You may think, you can decide the code structure and other things without any restrictions. But if you are not experienced enough then you might fail in doing this. 

> The best way to decide design/architecture is -
> - get the thorough idea of the project, then try to think by yourself
> - show it to your mentor for validation
> - improve it from the feedbacks provided and repeat this cycle until you and your mentor is satisfied by the design.

## About my Project
![charmil](https://cdn.discordapp.com/attachments/852928325197234256/852951299501850634/unknown.png)

The project on which I will be working throughout this summer is **[Charmil](https://github.com/aerogear/charmil/)**. A Golang based Framework on the top of [cobra](https://cobra.dev/) which will help the developers to create CLI's as Plugins and later they can be installed/imported into any CLI. This can be achieved with a package manager similar to npm, apt, pip etc. 

The user will import charmil in their CLI, which will provide them all the extensions out of the box. The user will be able to install specific plugins with the install command. After installing the extension, users will be able to use the features of that plugin without writing code for that particular feature which that plugin provides.

So it's a SDK + CLI kind of stuff.

I cannot imagine working on something big like this own my own. That's where [Google Summer of Code](https://summerofcode.withgoogle.com/) gave me the platform and my mentors who are always there to support me.

## How is it going?
I would say learning wise it's going truly awesome, I learn new stuffs daily while working. **Most important skill I got is plan before code.** This really helps in using the time effectively. Whenever I am stuck, I like to write that up in notion or github(depends), and it always leads me from nowhere to somewhere.

### Week 1 report
- Misunderstood some requirements of POC and explored how external CLI's with binary can be used as plugins [#37](https://github.com/aerogear/charmil/pull/37)
- Implemented correct wrapper approach according to the requirements [#45](https://github.com/aerogear/charmil/pull/45)
- Compared how wrapper and 2nd(plugin's use cobra) approaches are different, what do we loose/gain in wrapper approach [link](https://github.com/aerogear/charmil/discussions/43#discussioncomment-851017)

### Next Week
- Get the architecture of the final approach ready and move to 2nd phase
- Decide specific initial features and start implementing and documenting

### Blockers
- What validation do we do when we implement other than wrapper approach?
- Once the POC is ready then it should be easy to move with features

## Open Source Projects vs Personal Projects
There is huge debate on this topic on internet. But according to me, **open-source projects are much more worth than personal projects**. While working on OSS projects, you will be exploring the unknown code written by some engineer. You will collaborate with other open-source developers. Most of the project maintainers work full time in big tech companies and working with them will be a huge plus and you will get familiar with the industrial work.

All this above has been personally experienced by me in past months.

Connect with me here - [LinkedIn](https://www.linkedin.com/in/ankithans/) [Twitter](https://twitter.com/AnkitHans15) [Github](https://github.com/ankithans)