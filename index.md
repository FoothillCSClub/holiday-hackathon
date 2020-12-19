---
title: Holiday Hackathon
cards:
  - title: Explore CS through talks and workshops
    description: Attend events and participate in the workshops to further your coding skills, earn points, and win cool prizes! You’ll learn a lot about software engineering, and the top contestants will win a prize as a bonus.
  - title: Build a project for the hackathon
    description: Start, build, and present a project with a team of 1 - 4 people. Compete against other teams at the hackathon for a Grand Prize and more!
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
      - title: Keynote Talk
        time: 2:00 - 2:15 pm
        tags: ["everyone"]
      - title: Hackathon & Event Kickoff
        time: 2:15 - 3:00 pm
        tags: ["everyone"]
      - title: Intro to Git, Open Source, and Unix / Bash
        time: 3:30 - 5:00 pm
        tags: ["beginner"]
  - day: Sunday, December 27
    events:
      - title: Intro to Python
        time: 1:00 - 2:00 pm
        tags: ["beginner"]
      - title: Intro to Databases & SQL
        time: 2:30 - 3:30 pm
        tags: ["beginner"]
      - title: Intro to Web Dev
        time: 4:00 - 5:00 pm
        tags: ["beginner"]
      - title: Intro to Node.js & API servers
        time: 5:15 - 6:15 pm
        tags: ["beginner"]
  - day: Monday, December 28
    events:
      - title: Intro to Java
        time: 1:00 - 2:00 pm
        tags: ["beginner"]
      - title: Intro to Go / Writing game servers
        time: 2:30 - 3:30 pm
        tags: ["beginner"]
      - title: Using APIs / Web Scraping
        time: 4:00 - 5:00 pm
        tags: ["intermediate"]
      - title: Writing Discord Bots in Python
        time: 5:30 - 6:30 pm
        tags: ["beginner"]
  - day: Tuesday, December 29
    events:
      - title: <ins>Quantum Computing by Andrew Hacket from IBM</ins>
        time: 10 am - 11 am
        tags: ["everyone"]
      - title: Machine Learning & Neural Nets
        time: 2:00 - 3:00 pm
        tags: ["beginner"]
      - title: Java GUI
        time: 3:30 - 4:30 pm
        tags: ["intermediate"]
      - title: Audio Processing & Making Synths
        time: 5:00 - 6:00 pm
        tags: ["intermediate"]
  - day: Wednesday, December 30
    events:
      - title: "Hackathon check-in: share status"
        time: 2:30 - 3:30 pm
        tags: ["everyone"]
      - title: Making iOS Apps with Swift
        time: 4:00 - 5:00 pm
        tags: ["beginner"]
      - title: "Real World Use: GPS Stuff"
        time: 5:30 - 6:15 pm
        tags: ["intermediate"]
  - day: Thursday, December 31
    events:
      - title: Closing Keynote Talk
        time: 2:00 - 2:30 pm
        tags: ["everyone"]
      - title: Hackathon Presentations
        time: 2:30 - 4:30 pm
        tags: ["everyone"]
      - title: "Break: A fun activity 🎉"
        time: 4:30 - 5:00 pm
        tags: ["everyone"]
      - title: Winners announced 🥳
        time: 5:00 - 5:15 pm
        tags: ["everyone"]
---

## The Hackathon

Hackathon Qualifications:
- Final projects have to be able to run without crashing.
- Projects have to be presented to the judges on Thursday, January 31

## Activity Competition

This competition is meant for all people, especially those who may not be experienced programmers! You earn points for doing activities, and the most active attendees of the event will win a prize. Here's how you get points:

| Activity                     | Points            |
|------------------------------|-------------------|
| Attend a talk / workshop     | 10 points         |
| Do an activity in a workshop | 10 points         |
| Complete a Challenge         | 20 points         |
| Refer a friend               | 5 points / person |
| Hackathon Project            | 50 points         |


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

Everyone! No prior knowledge of code is required - this event should be fun even if you’re not an experienced programmer. To participate in the event, you are only required to be interested in CS and learning more about that.

**How can I participate?**

Attend talks and workshops, earn points, and submit a project for the hackathon! Not everything is required though - you can choose the things you would like to do.

**Do I have to attend everything?**

Absolutely not! You can and should pick and choose the workshops that are interesting to you and attend those.

**Do I have to submit a project?**

No! If you’d only like to attend the workshops and events, that is fine too. We do recommend trying to build a project however, even if it’s something simple. Feel free to reach out to one of the mods for coming up with an idea!

**I’m still not sure if I should join...**

No worries! Reach out to one of the mods, like @Zachary or @Madhav, and have a chat with them to see what stuff you might enjoy at the event. Have fun, and feel free to drop by!
