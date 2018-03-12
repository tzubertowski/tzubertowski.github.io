+++
date = "2018-03-12T08:04:08+01:00"
draft = false
title = "Sunday sermon #3 - face to face code reviews loose their value"
categories = ["sermon", "sunday", "code review", "codereview", "cr", "pr", "asynchronous", "synchronous"]
image = "images/2018/03/codereviews.jpg"
+++

### What are code reviews? 
Hopefully most of my readers whom are programmers are working in an environment where code reviews are part of the software development process.
For those readers who have no idea what those are: code reviews are self-explainatory, it's a process of reviewing changes submitted by one programmer by other programmers working on the same project. 

Mind you - such reviews were not so popular just a few years back but benefits of including them in software development pipeline made them adapted widely anywhere from open source communities to business teams.

### Why are code reviews important?
They aim to shield your codebase against changes which are faulty or do not comply with agreed standards. This means that any change which is not compatible architecturally, does not follow best practices, introduces bugs or simply do not solve the issue at hand will not get to the codebase.

In addition to protecting the codebase against unwanted changed code reviews are also a place where discussion and knowledge sharing happens.

### Why doing code reviews face to face decreases their value
In teams that follow methodologies closer to rapid development a practice of holding face to face, or sit down with me please, code reviews is common.
Naturally smaller treams, eg. startups, tend to favour face to face communication over asynchronous communication - mostly due to the former being faster.

At the same time they don't realise that:

* **Sitting down with someone to explain them your changes makes the whole review process biased.** Code should speak for itself. If it does not - that should be caught by someone whom does not see it from your perspective. The moment you **explain** a solution you change this unbiased approach of your reviewer. Now he thinks about a problem from your perspective.

* **Your discussions are only kept to you and your reviewer(s).** Knowledge share, which I briefly mentioned before, is something that written code reviews excell at. Writting down your opinion, linking to resources, being able to come back to a comment any time without needing to keep it in your mental stack and verifying the review against other's - you are loosing it the moment you don't share it. You could say - "yea, but I'll write it down later" - how is that faster? Why not do it in the first place?

* **Software development requires focus.** And code reviews are part of software development process. You want quality code? Give the programmer time, resources and let him focus. You want quality code review? Give the programmer time, resources and let him focus. As simple as that. 
It is ignorant to think your reviewer will read, **understand** and **verify** your solution while you are looking over their shoulder. They got hired to think, same like you, let them do what they are good at.

### Ending words
Just make sure you don't limit yourself to discussing over internet. This post was aimed to target the **issues** of synchronous communication and while writing down comments sure is great, once Your opinions and arguments have matured it sure helps to discuss face to face.
