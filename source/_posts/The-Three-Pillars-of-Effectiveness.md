---
title: The Three Pillars of Effectiveness
date: 2021-05-14 20:35:53
tags: management effectiveness responsibility empowerment knowledge
---

> To be effective you need to be responsible, empowered, and knowledgeable. If you only have one or two, seek the others. If you're unable to acquire the others; let it go.

## Some Challenges

I'd like to introduce this post writing up a few challenges I've had in my career (anonymized). 

1. I was told to hire a team of consultants to work on a project. Having observed how the company worked, I knew that the project was not ready to be worked on, and raised this as a concern. However, I was told to still hire; the roadmap indicated we would need more people. They were let go after a few months due to underutilization.
2. I had to evaluate the delivery of a project by a team of consultants. I saw that the project had not been written in a scalable fashion (each service assumed a single node), and raised this as a concern. The consultants answered they would add scalability later, an answer leadership was happy with. When they later claimed this functionality had been implemented, leadership wished to accept it. I had my concerns, tested it, and found an issue. I told this to leadership, who did not know what to make of my claims. I convinced the consultants to run the same tests I had, at which point they agreed more work was needed.
3. At one company, three teams had been working in one particular business domain, some supporting legacy code, others building new services. When upper management decided the legacy system needed to be rewritten, they inserted themselves in as the decision maker, along with an architect who was not responsible for implementation or support. Progress was extremely slow, and people started to quit.
4. At one company, a core infrastructure team existed. The department they were a part of had to use them; the department I was a part of did not. The department that had to use them found their needs unmet, and their progress slowed. The department I was a part of found our needs unmet, but was able to own spinning up our own infrastructure and so were able to quickly make progress. This led to a bit of bad blood all around. 

All of these problems stem from the same core issue. There were misalignments between responsibility, empowerment, and knowledge. The goal of this post is to dive into this idea.

## Clarification

I want to start by being very clear - this is a tool for defining a problem. It helps to make sense of the problem, and provides some direction for potentially solving it, but it does not dictate or guarantee a solution. I'll discuss a bit about the ramifications of that at the end.

So to begin, I want to describe a situation everyone has encountered. I'll speak to it from the perspective of a software development engineer, but I think it extends beyond this domain. It is namely this - in any sort of organization, there are times when a desired outcome is clear, and yet it is unclear how to make progress towards it. Even if one's entire job is to make progress towards a particular goal, it sometimes feels impossible to be effective.

This differs from operating as an individual; a single goal that an individual wishes to pursue is usually straightforward. It may be hard, it may involve a lot of work and learning, and it may turn out the goal is itself impossible (due to a limitation in physics or similar), but making progress is comparatively clear.

Innately this is due to the difficulty of working in an organization. The more people involved, the more communication has to happen and the more likely people are to be misaligned, in goals, in responsibilities, etc. Dealing with this can be challenging; even if one's role is clear, it may not be clear how to be effective in it. 

To this end I have developed this loose heuristic to determine what I should put effort into - those things that I feel responsible for, empowered to change, and knowledgeable about, are those things I can affect. Responsibility, Empowerment, and Knowledge. 

## Responsibility

When I say responsibility I am not speaking about those things a manager might have said one is responsible for. Ideally that will align with what I'm speaking about, and it certainly is a good starting point in a new organization, but what I truly mean are those things that the individual is directly affected by.

A way of describing this is "if this breaks, who gets blamed" - yes, I know, many cultures eschew blame, but nevertheless there is an instinctual understanding of who is responsible (responsible being simply a more positive synonym for blame). If the code breaks, no one looks to marketing to fix it. 

This is different than how organizations speak of responsibility in a key way - management may be "responsible" for the system, but they aren't delivering it. No director is answering the PageDuty alarm; they aren't actually responsible for it. They're responsible for hiring the right people, and creating the right processes and incentives. It's the dev, or the ops team, or whomever, that is actually responsible. They feel the effects of it.


## Empowerment

At it's simplest, empowerment means being able to make desired changes in a particular context. Like responsibility, this is not what management says; management often says "you're empowered to do this", and it's more wishful thinking than actuality.

If you can make a decision, and actually carry it through, you are empowered. 

Empowerment can encompass both organizational empowerment, and technological empowerment. Ideally these match; many orgs attempt to create constraints to ensure they do, but they're worth calling out separately. Organizational empowerment is being able to make a decision others won't question. Technological empowerment is being able to do something without being prevented. I.e., I am not organizationally empowered to install crypto mining software on my company laptop, but as I have root, I am technologically empowered to be able to.

## Knowledge

It almost goes without saying that if you don't have knowledge to inform a decision you shouldn't be making it, and yet we see examples of this all the time. 

Knowledge is simply knowing all the variables that need to be taken under consideration for a decision. This is surprisingly hard to do, but it is in fact the entire point of communication within an org. There is no need to communicate a decision to another part of an org unless it is relevant for a decision they face. HR does not need to inform dev of most of their decisions, and vice versa, because it is not relevant. Not that it isn't sometimes interesting (and not that some organizations don't overshare irrelevant information; these are the townhalls that get skipped, and the emails that get binned unread). 

## Addressing Examples

None of this comes as a surprise, and yet it's something that is oftentimes missed by leadership. I want to start by addressing the examples I gave above -

1. The hiring of unnecessary consultants: The decision here was hiring consultants. Upper management was lacking in knowledge; specifically, that the situation on the ground did not match what their timelines dictated should be the case. They were not willing to (or aware of the benefits of) delegate responsibility or empowerment for making the decision, either. Worse still, by delegating the responsibility and empowerment for *carrying out* the decision, they hurt morale, as it meant the person executing the action was the one who knew it was a waste of money. 
2. Consultants delivering a non-scaling solution: Upper management did not have the knowledge to evaluate non-functional requirements of the system, recognized it, and delegated responsibility and empowerment to me to vet that the consultants were delivering (if we accepted delivery it would be on me and my teammates to support it, ergo, responsibility). When the consultants indicated scalability would be added later, upper management did not have the knowledge to understand how hard that was, and at that point chose to retain empowerment around how to handle the consultants. When a scaling system was delivered, they took it at face value. However, knowing I was responsible, I sought out how the consultants tested the system, and tested it myself to gain knowledge as to whether it really supported multiple nodes and could scale out. I did not have any empowerment to accept or reject the consultants' work at this point, and so had to convince them to admit to upper management it did not work.
3. Rewriting the monolith - Upper management did not have the knowledge for the existing systems, but still chose to retain empowerment for making decisions. The tech team would be responsible for them. 
4. The infrastructure team had the knowledge and empowerment to make infrastructural and DevOps decisions. They were not, however, responsible for feature delivery. The feature team within the same department was responsible for feature delivery, but was not empowered to solve infrastructural/DevOps problems themselves. My department was responsible for feature delivery, and *was* empowered to solve infrastructural/DevOps problems ourselves, and we sought out knowledge to be able to.

## Putting It Together

So, what to make of this? Well, as I started this post with, I've found this a useful heuristic. A framework for thinking about a problem, if you will. It helps me determine what I need to pursue, or whether I need to reframe a particular problem, or even whether I need to just accept I am not in control of something. It also has led to a few lessons in how to apply this idea.

If you find yourself responsible for something, and are missing the other two, seek out knowledge first. The process of gaining knowledge often makes getting empowerment easier.

If you are not responsible, but have either of the other two, seek to find out who is responsible. Again, using the definition of "who is affected by this". Chances are good that enabling that party will lead to you getting one of the things you are missing. As an easy example, the relationship between product and development. Product has knowledge about what the business cares about, but is neither responsible nor empowered for delivering a solution. Product IS, however, responsible and empowered to make decisions about tradeoffs for the product. By giving the dev team knowledge about the problem, it enables the dev team to reciprocate knowledge about what tradeoffs there are (and in enabling product to make those decisions, it enables the dev team to deliver what they are responsible and empowered for; namely, delivering a software solution the business cares about).

Lastly, there will be times you can't get all three. Recognize these situations as ones you are powerless to change. If you're not responsible, this is pretty easy to do. But frequently you are responsible for something, but either not empowered or not knowledgeable about it. In these situations, you either have to reframe the problem ("the alarm went off, I'm responsible for things working in prod, but I don't have permissions; I'm not empowered to make changes in prod...okay, let me reach out to someone empowered to make changes, provide them the knowledge I have, and responsibility will fall on them then"), or find ways to move responsibility off of yourself, or to otherwise allow yourself peace of mind even when things are falling apart around you.