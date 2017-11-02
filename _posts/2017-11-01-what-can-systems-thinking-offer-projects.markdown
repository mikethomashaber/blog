---
layout: post
title: How can Systems Thinking support Projects
---

I wrote this post after seeing an upcoming seminar on how systems thinking can help projects from the Association of Project Management. As I write this, this seminar is in the future, so I'll have to see what it says.

The question made me think, and I've produced the following way that systems thinking can help a project assess successes in delivering value. I think this suggestion is both simple, and has sound basis in practice and theory. I've used ideas from Werner Ulrichs' Critical Systems Heuristics combined with the framework of Test Driven Software Development, and Clean Interviewing based on David Groves Clean Language.

## What do I mean by Project?

I'm using the word project in the widest possible sense here, as a container for purposeful work. So redesigning Government Departments, building relief roads, developing software solutions all count however they are managed.

## What is the problem we're looking at?

I'm going to assume that following is a problem. Projects is they often start with goals of doing some thing to help people, or improve a situation , but end up having success measured by a tick list of 'deliverables'.

Not all projects suffer from this, but I think enough do to make looking at this a worthwhile goal.

I see this as a problem because often projects are funded because of the benefits to people or situations.There is no systematic, repeatable, way to ask - 'who are we benefiting and how do we see if the project helped in the way' that was claimed when funding was allocated.

So something can be funded because it should benefit you, but can be seen as a success even it it makes things worse for you.

## Overview

I propose to use a framework based on Software Test Driven Development(TDD) that systematically allows you to select your Stakeholders and ask them a pre defined set of questions, with Clean Language follow up questions. T

The answers are used to measure if the project has delivered the benefits that it set out to deliver. By asking questions first, this approach defines 'done' before any work is started.

## Measuring Success

The two sides of project success are

* the technical implementation of the thing that can be measured quantitatively.
* Do we have a thing?
* how the thing meets it's purpose.
* Measure qualitatively, with value and needs met.


## Problems with measuring purpose

It's possible to develop a technically brilliant solution to the wrong problem. This is summed up in the phrase "Doing the wrong thing righter". Did we stay in budget, did we deliver on time are quantifiable, but it's possible to build the wrong thing, but be on time and on budget.  Did we do the right thing is harder to define.

Building the wrong thing, but on time and in budget is not 66% success. It's 0% success.

## How do we currently measure Success?

Measuring success is complicated. Project success can be categorised into Time, Cost and Quality.

A post from Aexlos suggests the following metrics, based on the PRINCE2 methodology suggests the following

Benefits Achieved
Goals, Milestones achieved
Stakeholder Satisfaction
User Satisfaction
As far as I can see there isn't a set, repeatable way to measure these things.

Stakeholder and User Satisfaction are both groups who can be asked questions about the benefits that have been achieved. Goals and Milestones can be answered with a yes/no.

So I'm going to concentrate on what to ask users and stakeholders to see if their benefits have been achieved.

I think we can systematically approach this, by having a standard set of questions we ask stakeholders. Even thought the answers are not simple yes/no we can still compare between projects.

We can also do this within a framework based on Test Driven Development, where tests for success are written before progress starts. This may seem difficult at a project level, but is just a case of asking whose problems you promised to solve, and asking them some before and after questions.

 

## Part 1. Who are our stakeholders?

To find stakeholders, ask

Who did we offer to help?
These are stakeholders!
If we didn't offer to help these potential stakeholders would the project still get funded?
If we're getting funding because we've offered to improve someone situation, we should get their ideas of project success before we start.
The answers are captured before any work is done or money is spent in solutions.

Make a note of who the project is supposed to benefit, and add people who represent the interests of the beneficiary to the list of stakeholders.

If the project has funding because it will benefit someone who is not on the list of stakeholders alarm bells should ring.

If the project is just to build a thing, because someone wants thing and doesn't value people who may be affected that is fine too.

## Part 2. What do we ask stakeholders?

We can use to published academic research, rather than design our own questions. In 1983 Werner Ulrich created Critical System Heuristics (CSH)to look at what he calls 'Boundary Judgements'.

We're asking what are the boundaries of what we care about. For example

is meeting this stakeholders needs inside the boundary of what we care about? Is it critical to project success?

This book chapter from the Open University is a great introduction to CSH if you'd like to learn more.

From the perspective of each set of stakeholders CSH questions are: 

Who ought to be the intended client or beneficiary of the Project?
What ought to be the purpose of the Project?
What ought to be the measure of Success of the Project?
When you've done some work on the project you can then do Test Driven Project Development, and see if your solution passed the tests by asking from each set of stakeholders:

Who currently benefits from the Project output? Is this who we thought ought to benefit?
What is the purpose of the Project, based on it's functional outputs? Is this what the purpose ought to have been?
Does the Project output meet my measures of success?
Answering the questions above should be done using "The Purpose of a System is What is Does" as a guide. This great quote is from Stafford Beer, whose work features in other posts on this blog.

If your project doesn't pass the tests you're not done yet, because you're using an approach based on Test Driven Development. You specify tests for success before you start, and keep working until the tests pass. (See To-Do for when requirements change).

 

## Test Driven Software Development

In software development there is a thing called test driven development. It's a pretty good way to write software and it's been around for a while.

Test Driven Development goes like this

Understand what functionality you want, broken down into single function components
Write a test for that functionality
when you've written your code, the test will pass if the code works and fail if not
Run the test and See it fail
Write the code to make it work.
Add more tests if you think of them.
The TDD [workflow](http://www.agiledata.org/essays/tdd.html) looks like this


)
Tests are small, and there are often lots of them. Usually when a developer commits some code all the tests automatically run, and you don't go home until they pass.

Test Driven Development, or TDD, gives reassurances that when things change all the known tests still work, or you get visible errors.

## Systems Thinking and Projects To Do

Produce some examples of projects measured in this way.
Design the feedback loops and communications required if the success criteria  changes around what stakeholders we vaule.
This is moving something from within the boundary of what we care about to outside this boundary
What to do when stakeholder requirements change. This is expected, as stakeholders learn more about the situation, and the output of the project takes shape.
:w
