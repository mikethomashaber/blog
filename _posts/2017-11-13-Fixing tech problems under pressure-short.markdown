---
layout: post
title: Fixing Tech problems under pressure
---
SEE LONGER Version
## Overview
This posts looks how to overcome difficulties people have when they need to work together under pressure to solve a problem. The examples are from my experience with IT incidents involving complicated interdependent back end systems. Many large organizations have IT systems like this.


This post suggests
* the cause of some of the interpersonal problems we have working together
* Some things we can do to help
* issues with experts and non experts
* an overall framework for a team to solve problems with complicated IT systems that may ge generalizable
* a way to share and collaborate across knowledge silos to find the cause of an issue
 * using a technique to create cross silo documentation using graphs


### We use complicated Systems
We need to fix problems that no-one expected. Problems we expect can have planned and tested responses. The difficult problems have fell down the gaps in our knowledge.


### How we build things
How we build these systems has an effect on how we fix them when things go wrong.

If there are three teams building your application, you'll probably get an application with three parts. You may design it this way, of you may get a mirror of whatever your organisation structure is. This Conway's Law for your application (http://www.melconway.com/Home/Conways_Law.html).

It means the internal architecture of your system may have been decided by a manager dividing the work between teams, maybe with concerns about power and rewarding colleagues rather than how running and diagnosing the finished IT system.

When things go wrong it's something that hasn't gone wrong before, and was never supposed to happen. Very often, the solution be where two knowledge silos meet.

### We need silos
It tempting to say that having silos is bad and we need to get rid of them, and the frustration with some forms of silo behaviour is understandable. For complicated systems, knowledge silos are inevitable, in fact necessary, as 'fixing' them creates more problems (HOW) (http://www.strategicstructures.com/?p=851). We're going to have silos where deep technical expertise is required. We can choose where these silos are, and how we manage the boundaries.

### Problems with Silos
Under pressure people gravitate to general, rather than technical skills (http://bit.ly/AllspawThesis), and under pressure we may defend our silo territory before looking to solve the issue.

In high pressure situations there can be a lack of psychological safety, and people may avoid suggesting diagnosis because they risk being judged if they are not correct. (https://en.wikipedia.org/wiki/Psychological_safety).
Even where safety exists in a team, it may not exist between silos.

It may be career limiting in the organization to be seen to be the cause of issues.


### When things go South

When things have gone wrong a lot of people with gather in a space attempting to find a solution. Some are subject matter experts, others maybe responsible for teams involved, or for communication. There is likely to be senior management who are being asked what's gone wrong and how long until it's fixed.

The composition of people in the room is vital. You need the people who designed the system, configured it, wrote the tests and those who run it. There may be knowledge silos across teams here. Or it may be the same people.

I'm strongly biased here. I've worked on incidents where I've been in a team responsible for the the design, implementation and running of a system (SEE SRE), and I've also diagnosed incidents with separate architects, solution designers and operations. The latter can be slow and challenging, here's why:

### Looking for the fix

Perhaps someone senior has heard about component X. Maybe that's what broke last time. They'd really like you check that right now. Maybe the person responsible for X puts forward a strong case why it definitely isn't X. The defense works but the barriers are now up, and there is a round of finger pointing until someone risks losing an eye.

Alternatively, the more you know about something, the more you know you don't know (https://twitter.com/swardley/status/526074463175966720) so beginners are often more certain than experts. So someone technical, knowledgeable and dilligent may reply "well I suppose it could be X". And a group goes off to look at X. (Pro tip: It's probably not X).

This is clearly not the best way to work. People like to save face. Cross Sile meetings are not a safe space, being wrong is bad, being responsible for the system at fault may be worse.

Unfortunately experts are not enough here. The incident hasn't been caused by something that was expected. Experts know what to expect. The problem is investigated LINK. What is required is someone in the room 

### What do we need?
I've identified and tested two thing here.
1. A framework to follow.
What should we do, who should do it, what we do next. This is what goes in the ITIL service management box 'fix the broken thing'.

1. A overall systems map.
This is not an architecture model, or a level X solution design, those won't do what we want. It's purpose is to help solve problems, so it's different from the documents produced in architecture and design. It's owned by the DevOps or IT Operations team. It is a map of how all the bits fit together end to end, and when Observations happpen they can be placed on the map, and say 'This happened here, before this bit, and after this'.


### How to get a End to End systems diagram using Clean Interviewing
I created End to End diagrams of system I was interested in using mind map software. The map may contain a wide range of knowledge. Hopefullly they're not in separate silos. I really hope there are not one or more outsourcing partners. It happens.

An end to end map is produced by talking to experts, and I've found Clean Interviewing (https://make10louder.co.uk/2017/07/15/clean-interviewing-for-technology-converstaions/) really  useful for this. Clean Interviewing (http://www.cleanlanguage.co.uk/articles/articles/317/1/Clean-Evaluative-Interviewing/Page1.html) is a way of asking questions so that your prior knowledge or ideas does not get in the way. Clean Language is conceptually simple, but can take a bit of practice to get right.

An end to end systems map is a bit like a User Journey in UX. Where are we before and where d we go next.

Are each level we'd like to know "for *this part* to work, what needs to happen?". Using Clean Interviewing questions to get follow up details, and adding them to the mind map.
Other Clean Coaching techniques can get some *really* useful insights. The questions are designed to get information out of the interviewees head without the interviewers bias or ideas getting in the way.

### John Boyds OODA
"What we do next" can be answered by John Boyd. John was a jet fighter pilot, and designed the US Military Engagement Strategy for complex fast changing situations. OODA more than capable of solving an IT problem. (https://en.wikipedia.org/wiki/OODA_loop).

Additionally Brendan Gregg, who's the author of a load of linux and solaris performance tools lists OODA as one of a numbe of problem solving frameworks. If it's good enough for Brendan I'm happy. http://www.brendangregg.com/methodology.html

OODA stands for Observe, Orient, Decide, Act. This is a fast decision making loop. If you need to have an Emergency Change Approval Board before each Act decide who's on this, and make it happen quickly if you want things fixed. This is a feedback loop that can run really quickly.
If you have an daily ECAB your issue could take a long time to fix.

# Observe
What do we know, what is instrumented. Is there information from users? How much do we trust the data? This information will have been collected from somewhere on your end to end model.

# Orient
As an Incident Team, discuss what does this data mean? Where does it suggest the problem may be? What do we now know, and with what certainty?
You've probably just run and test, and you should already know what the results mean, but it's likely you also have new data from other sources too.

# Decide
Decide what test to run next.

# Act
Run and document the test and results.

# How to Decide
Using the End to End diagram, understand what the data may be suggesting. When evaluating proposed actions as "What is ruled out if the results are X, what is rules out if the result are Y". Ideally you'll design tests that give X or Y.

You need to decide as a Team what the results mean *before* the test is done. What the results mean should be visible on the End to End diagram. For example a test should allow you to rule out parts of the system.

Every test goes through this. So if the Highest Paid Person in the rOom thinks you should find what is being tested on the End to end diagram, and the things that can be learned from the results are discusses.


### Where do the fingers point now?
Instead of pointing fingers at each other, the Incident Resolution Team are pointing fingers are the End to End Diagram, and asking questions like "what would reconfiguring this tell us" or "We could replace this component to rule out all of this part of the diagram".

New ideas can be quickly evaluated, and extra detail is quick and easy to add where it is required.

### OODA In an ITIL and RACI framework

## Issues, and future
