---
title: Holiday Hackathon
cards:
  - title: Learn
    description: Attend talks and participate in workshops to further your coding skills, earn points, and win cool prizes! There's a lot to explore.
  - title: Build
    description: Build a project in the hackathon, and show it off to your friends! Do it just for fun, or compete with teams of 1 - 4 people for prizes!
tags:
  everyone:
    label: Everyone
    color: "#1584e2"
  beginner:
    label: Beginner
    color: "#00a700"
  intermediate:
    label: Intermediate
    color: "#e48f0f"
schedule:
  - day: Saturday, December 26
    events:
      - title: Hackathon & Event Kickoff
        time: 2:00 - 3:00 pm
        tags: ["everyone"]
      - title: Intro to Git, Open Source, and the CLI
        time: 3:30 - 5:00 pm
        tags: ["beginner"]
  - day: Sunday, December 27
    events:
      - title: Intro to Python
        time: 1:00 - 2:00 pm
        tags: ["beginner"]
      - title: Intro to Java
        time: 2:30 - 3:30 pm
        tags: ["beginner"]
      - title: Intro to Web Development
        time: 4:00 - 5:00 pm
        tags: ["beginner"]
      - title: Intro to Node.js & API servers
        time: 5:15 - 6:15 pm
        tags: ["beginner"]
  - day: Monday, December 28
    events:
      - title: Intro to Databases & SQL
        time: 1:00 - 2:00 pm
        tags: ["beginner"]
      - title: The Go Programming Language
        time: 2:30 - 3:30 pm
        tags: ["beginner"]
      - title: Writing Discord Bots in Python
        time: 4:00 - 5:00 pm
        tags: ["beginner"]
      - title: "\"Track This!\" - GPS tools and algorithms 101"
        time: 5:30 - 6:15 pm
        tags: ["beginner"]
  - day: Tuesday, December 29
    events:
      - title: <strong>"Quantum Computing" by Andrew Hacket from IBM</strong>
        time: 10 am - 11 am
        tags: ["everyone"]
      - title: Machine Learning & Neural Networks
        time: 2:00 - 3:00 pm
        tags: ["beginner"]
      - title: Building GUI Apps in Java
        time: 3:30 - 4:30 pm
        tags: ["intermediate"]
      - title: "\"Make a synthesizer!\" - Audio Synthesis and Processing"
        time: 5:00 - 6:00 pm
        tags: ["beginner"]
  - day: Wednesday, December 30
    events:
      - title: Web Scraping 101
        time: 1:00 - 2:00 pm
        tags: ["beginner"]
      - title: Hackathon Presentations
        time: 2:30 - 4:30 pm
        tags: ["everyone"]
      - title: Winners Announced
        time: 5:00 - 5:15 pm
        tags: ["everyone"]
---

## Overview

During the event, there will be lots of talks and workshops that we'll be hosting, ranging across various topics and fields. We plan to have plenty of workshops for all levels of coders, from beginners to pros, so that everyone can enjoy and learn something new!

There will also be a hackathon where you can build a project of your choice. Don't let this intimidate you though, because it'll be fun!

> [**Hackathon**](#hackathon---build-a-project)
>
> [**Activity Competition**](#activity-competition---just-participate)
>
> [**Schedule**](#schedule) - **featuring a seminar by Andrew Hacket from IBM on Quantum Computing**
>
> [**FAQs**](#faqs)

## Hackathon - Build a project

Throughout the week, you can build a project of your choice, with help and guidance from us as needed. The project could be of any size, and could be really, really simple. It doesn't have to be anything fancy — just have fun, learn, and build something!

For the competition, here are a few guidelines:

- Teams should be 1 - 4 people.
- Have your project be in a GitHub repo with a README, in order to share it.
- Projects should to be presented to the judges on Wednesday, December 30 ([see schedule below](#schedule)).

DO NOT worry if this does not make sense to you just yet, because we'll go over this in one of the workshops. And, don't hesitate to reach out to us!

## Activity Competition - Just participate!

This competition is meant for everyone, especially those who may not be experienced programmers. You earn points for doing all kinds of activities, and the participants with the most points will win a prize. Here’s how you get points:

| Activity                     | Points            |
|------------------------------|-------------------|
| Refer a friend               | 5 points / person |
| Attend a talk or workshop    | 10 points         |
| Do an activity in a workshop | 10 points         |
| Build a hackathon project    | 50 points         |

*By the way, you don't need to compete in the hackathon in order to get points for building a project. Simply building it and sharing it with us will be enough!*

## Schedule

<div class="schedule">
  {% for dayinfo in page.schedule %}
  <div class="day-container">
    <h3>{{ dayinfo.day }}</h3>
    {% for event in dayinfo.events %}
    <div class="event">
      <div class="title">
        {{ event.title }}
      </div>
      <div class="details-container">
        <div>{{ event.time }}</div>
        <div class="tags">
          {% if event.tags %}
            {% for tag in event.tags %}
              {% assign tagitem = page.tags[tag] %}
              <span class="tag" style="background-color: {{ tagitem.color }}">{{ tagitem.label }}</span>
            {% endfor %}
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
  {% endfor %}
</div>

{% comment %}
| Day       | Time             | Topic                                      |
|-----------|------------------|--------------------------------------------|
| Sat 12/26 | 2:00 - 2:15 pm   | Keynote Talk                               |
|           | 2:15 - 3:00 pm   | Hackathon & Event Kickoff                  |
|           | 3:30 - 5:00 pm   | Intro to Git, Open Source, and Unix / Bash |
|           |                  |                                            |
| Sun 12/27 | 1:00 - 2:00 pm   | Intro to Python                            |
|           | 2:30 - 3:30 pm   | Intro to Databases & SQL                   |
|           | 4:00 - 5:00 pm   | Intro to Web Dev                           |
|           | 5:15 - 6:15 pm   | Intro to Node.js & API servers             |
|           |                  |                                            |
| Mon 12/28 | 1:00 - 2:00 pm   | Intro to Java                              |
|           | 2:30 - 3:30 pm   | Intro to Go / Writing game servers         |
|           | 4:00 - 5:00 pm   | Using APIs / Web Scraping                  |
|           | 5:30 - 6:30 pm   | Writing Discord Bots                       |
|           |                  |                                            |
| Tue 12/29 | 10:00 - 11:00 am | <ins>Quantum Computing by Andrew Hacket from IBM</ins> |
|           | 2:00 - 3:00 pm   | Machine Learning & Neural Nets             |
|           | 3:30 - 4:30 pm   | Java GUI                                   |
|           | 5:00 - 6:00 pm   | Audio Processing & Making Synths           |
|           |                  |                                            |
| Wed 12/30 | 2:30 - 3:30 pm   | Hackathon check-in: share status           |
|           | 4:00 - 5:00 pm   | Making iOS Apps with Swift                 |
|           | 5:30 - 6:15 pm   | Real World Use: GPS Stuff                  |
|           |                  |                                            |
| Thu 12/31 | 2:00 - 2:30 pm   | Closing Keynote Talk                       |
|           | 2:30 - 4:30 pm   | Hackathon Presentations                    |
|           | 4:30 - 5:00 pm   | A fun activity 🎉                           |
|           | 5:00 - 5:20 pm   | Winners announced 🥳                        |
|           | 10:00 - 12:10 am | New Year Party 🎉                           |
{% endcomment %}

## FAQs

**Who is this for?**

Everyone! The events should be fun even if you’re not an experienced programmer. To participate, you only need to be interested in learning cool new stuff!

**How do I join?**

The hackathon will be hosted on Discord, in the CS Club Server. [**Click here to join the Discord server**](https://discord.com/invite/graRNeE), and ask for the @hacker role! Feel free to email [info@foothillcs.club](mailto:info@foothillcs.club) for assistance.

**How can I participate?**

Attend talks and workshops, earn activity points, and build a project for the hackathon! Not everything is required though - you can choose the things you would like to do.

**Do I have to attend everything?**

Absolutely not! You can pick and choose the talks, workshops, and activities that are interesting to you and attend those.

**Do I have to submit a project?**

No! If you’d only like to attend the workshops and events, that's ok. We do recommend building a project, however, even if it’s something small or simple. Feel free to reach out to one of the @mods to come up with an idea!

**I’m still not sure if I should join…**

No worries! Reach out to one of the @mods and have a chat with them to explore the things you may enjoy at the event. We're friendly, so don't hesitate at all. Have fun, and feel free to drop by anyways!
