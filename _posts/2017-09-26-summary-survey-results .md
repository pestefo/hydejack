---
layout: post
title: '"Survey on Collaboration and Package Reuse in ROS", Summary of Results'
tags: [survey,results,research,phd]
comments: true
---

# **"Survey on Collaboration and Package Reuse in ROS", Summary of Results**

## **Context**

We are researching on the phenomenon of package reuse within the Robot Operating System (ROS) community and the collaboration dynamics of this community. We invited ROS users to answer a short survey to get insights on these topics.

The questionnaire consisted of 22 questions (half of them were mandatory), with an average response time of 7 minutes. The questionnaire was available between August 8th and 29th, we got 127 responses (89.7% of them complete) from 23 different countries.

## **Profile of the participants**

Participants were profiled by their experiences using ROS (in years) and their personal opinion of their background in Software Engineer.

<IMG Q4><IMG Q5>

![image alt text](image_0.png)

![image alt text](image_1.png)

The large majority (93%) of the participants indicate that they know what Software Engineering is. In fact, two thirds of the participants do have a Software Engineering background, among them a little more of the half has a strong background on the area. Regarding their experience using ROS, beginners (up to 1 year of experience) and intermediate users (more than a year and up to 3 years of experience) are represented in a similar proportion (29% and 31%). Although the proportion of advanced users is slightly bigger (40%).

## **Reusing ROS packages**

The reuse of ROS packages is one of our main interests on this survey.The large majority of our participants (93%) have had the experience of reusing a 3rd party ROS package, this means, a package that is maintained by the community.

<IMG Q6>

![image alt text](image_2.png)

From these participants, around 73% has failed trying to reuse a 3rd party ROS package. These packages are shared and maintained by the community, but are later not  straightforward to reuse. In this context, the effort that the community commits to improve the software ecosystem is not being fully leveraged.

<IMG Q9>![image alt text](image_3.png)There are many reasons why this situation happens. From 10 different reasons provided, the three most common are:

1. The package was for an outdated ROS distribution, 65% of participants

2. The user could not figure out how to use it (lack of documentation), 53% of participants

3. There was a bug that prevented the package from working properly, 47% of participants.

As evidenced by the top reason picked by the participants, apparently there is a significant delay between ROS distribution updates and their implementation in packages by maintainers, meaning that this task is carried over to the users. The aforementioned reason and the third one raise the question about issues with the feedback dynamics from users to package maintainers, who seem not to realize that there are problems with their packages.

#### Abandon Packages phenomenon and dependency to 3rd party ROS packages

Another phenomenon that we are interested in is Package Abandonment. These are packages that were released and stopped being updated at some point. This situation affects package users because abandoned packages are not usually compatible with newer versions of ROS. Users that may want to contribute fixes or updates cannot do so, since no one is maintaining the package.

We ask the survey participants about the frequency with which  they experience this situation.An important number of the participants (65%)  indicated that they experienced this situation "Sometimes", “Very Often” or “All the time”. Around a 8% have never experienced this situation. Even though 1 out of 4 participants rarely found an abandoned package, we can conclude that it happens in practice.

<IMG Q8>

![image alt text](image_4.png)

The *Abandoned Package *phenomenon becomes particularly relevant when an application depends on packages that are abandoned or are in risk of being abandoned. We discovered that a large portion (92%) of our surveyed participants relies on 3rd party ROS packages for the operation of their projects.

<IMG Q7>

![image alt text](image_5.png)

#### Resources for study a dependency addition

When integrating external software it is useful to have resources that help test it. An informed developer can take better decisions of the dependencies of their software. The reuse of packages can then be supported by tests and/or ROS Bags.  In this context we asked our participants how frequently they find these types of resources in 3rd party ROS packages.

According to the results, a bit more than a half of our surveyed participants say that it is very rare to find tests in these packages, with one third claiming to have "Occasionally" found tests . In the case of ROS Bags, a large majority (82% “Never” or “Rarely”) say that it is very difficult to have access to ROS Bags that could ease the task of evaluating the operation of a package.

<IMG Q11>

<IMG Q12>

![image alt text](image_6.png)

![image alt text](image_7.png)

[As discussed in ….](LINK) that the second most frequent reason why users fail at reusing packages is due to a lack of documentation: users can’t figure out how to use a package. We dug into this topic by asking what documentation is relevant when reusing 3rd party ROS packages and how relevant: highly relevant, relevant, somewhat relevant, hardly relevant and not relevant. We offered a pool of 8 kind of documentations to evaluate regarding: *general documentation*, *benchmarks*, *issue tracker information*, *API documentation*, *configuration guidelines*, *troubleshooting information* and *the robots in which a package has run* (and an option "*Other*").

We found that "*General documentation about the purpose of the package and its features*", “*API documentation*” and “*Guidelines for configuring the package launch files*” are a “must”: 88%, 82%, 82% (respectively) of participants think that these are “Relevant” or “Highly Relevant”. Moreover, “*Troubleshooting experiences from other users*” and “Issue tracker information” are “desirable” documentation: 88% and 83% of participants think that they are “Somewhat Relevant”, “Relevant” or “Highly Relevant“.

Results show that users lack information when choosing 3rd party ROS packages that may be useful to them. Users lack of enough documentation to configure and use these packages. Users  can then end up reusing buggy or abandoned packages. Furthermore, responses also show that packages are usually provided without tests for evaluating packages or ROS Bags for testing the integration to the their systems.

## **Collaboration in the ROS Ecosystem**

The second big topic covered in this  survey is collaboration in the ROS ecosystem.

#### What do ROS contributors contribute?

We first wanted to know what kind of contributions  members of the ROS Community do share, so  we asked participants to indicate the types of contribution that they have made. A list of 10 possible type contributions was offered, with an "Other contribution" option . It is worth noting that this list seems to be quite complete because we got a minimal amount of “Other contribution” responses.

<IMG Q17>

 ![image alt text](image_8.png)

We saw that 28% of our respondents acknowledged that they have never made a contribution. From those participants that have contributed, 70% represents *Bug Reports* and 56% *Bug Fixes*. Also, 62% have *Posted a Question* in ROS Answers or Stack Overflow, while a 51% has *Answered one question* on these platforms.

#### Why are there missed contribution opportunities?

Despite the numbers about collaboration showed in the previous section, contributing can be difficult. Sometimes contributors fail at doing it and for several reasons. We presented a list of 14 different reasons why someone could fail to make a contribution. From these option, the most frequent by far was *lack of time* (61% of participants selected this option). The next most popular reason for not contributing,  marked by nearly a third of respondents (32%), was that they think that the issue was too specific to his/her project and that the contribution would be worthless to the community. And slightly more a quarter of the participants were not confident in the quality or correctness of the contribution (27%), or could not make their  contribution because the targeted package was abandoned (26%).

Now, regarding  the community Q&A platform, ROS Answers, two thirds of the surveyed participants considered that answering a question on the platform is a task that demands too much time, since it requires replicating the situation described in the question. A quarter of the participants do not answer  because several follow-up questions needed before they can write  a good answer.

Our participants, as users, do contribute and in different ways. Those contributions need to be validated, integrated and made available by someone, in many cases this responsibility falls on the package maintainer. Hence, the phenomenon of Package Abandonment not only makes the reuse of packages more difficult, but also hampers collaborations. The latter is particularly critical because maintainers and users invest time in updating and testing packages that may end up being abandoned, which is a regrettable waste valuable effort and may discourage future collaborations.

## **Feedback?**

Would you like to complement some of the results found? Do you have a different opinion of the results? Any other question? Don’t hesitate commenting below or sending me an email to pestefo@gmail.com.
