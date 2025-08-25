---
layout: home
title: USC CSCI 444 Fall 2025 - NLP
nav_exclude: true
toc: true
seo:
  type: Course
  name: Natural Language Processing
---

# {{ site.tagline }}
{: .no_toc .mb-2 }
<!-- {{ site.description }} -->
🍂 Fall 2025 &nbsp; &nbsp; ⏰  Mon / Wed 10:00 - 11:50a  &nbsp; &nbsp; 📍 [WPH](https://maps.usc.edu/?id=1928&reference=WPH#!m/552624?s/) 106
{: .fs-6 .fw-300 }

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign cps = site.staffers | where: 'role', 'Grader' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% assign num_cps = cps | size %}

{% if num_teaching_assistants != 0 %}
{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}

{% if num_cps != 0 %}

{% for staffer in cps %}
{{ staffer }}
{% endfor %}
{% endif %}


## Announcements

<!-- See [Brightspace](https://brightspace.usc.edu/d2l/lms/news/main.d2l?ou=114109). -->

<!-- {% assign announcements = site.announcements | reverse %}
{% for announcement in announcements %}
{{ announcement }}
{% endfor %} -->

## Summary

Natural Language Processing (NLP) is an area of computing research and practice that aims to enable machines to reason over human text and speech. High profile technologies like ChatGPT brought NLP to the forefront of public discussion both inside and outside academia. But what underpins such technologies? This course will explore how natural language can serve as an interaction medium between users and machines with a focus on the history and development of language models (LMs). Students will become familiar with concepts and methods in NLP like distributional semantics, and see how those concepts feed into the architectural design of modern LMs trained using deep learning, and will get hands-on experience with building and evaluating small-scale LMs. The class will also explore details and variants of the real-world consequences of deploying large-scale LMs and NLP technologies more generally, such as the ethics and harms associated with them.


## Calendar + Syllabus

<table>
  <thead>
  <tr>
    <th width="5%">Week</th>
    <th width="5%">Date</th>
    <th width="30%">Class Topics</th>
    <th width="40%">Readings</th>
    <th width="13%">Work Due</th>
  </tr>
  </thead>
  <tbody>
  {% for week in site.data.calendar %}
    {% for day in week.days %}
      <tr>
        {% if forloop.index == 1 %}
        <td rowspan="{{week.size}}">{{week.week}}</td>
        {% endif %}
        <td>{{day.date}}</td>
        <!-- <td>{{day.theme}}</td> -->
        <td class="cal-content">
        {% if day.slides %}
          <a href="{{day.slides}}">{{day.theme}}</a>
        {% else %}
          {{day.theme}}
        {% endif %}
        {% if day.paper %}
          <span style="color:teal">{{day.paper}}</span>
        {% endif %}
        {% if day.projectpresentations %}
          <span style="color:blue">{{day.projectpresentations}}</span>
        {% endif %}
        {% if day.break %}
            <span style="color:green">{{day.break}}</span>
        {% endif %}
        </td>
        <td class="cal-content">
          {% if day.readingslink %}
            <a href="{{day.readingslink}}">{{day.readings}}</a>
          {% else if day.readings %}
            {{day.readings}}
          {% endif %}
          {% if day.additional %}
            {% if day.additionallink %}
              <a href="{{day.additionallink}}"><b>Additional:</b> {{day.additional}}</a>
            {% else %}
              <b>Additional:</b> {{day.additional}}
            {% endif %}
          {% endif %}
        </td>
        <td class="cal-content">
          {% if day.exam %}
            <span style="color:red">{{day.exam}}</span>
          {% endif %}
          {% if day.project %}
            <span style="color:blue">{{day.project}}; </span>
          {% endif %}
          {% if day.quiz %}
            <span style="color:fuchsia">{{day.quiz}}; </span>
          {% endif %}
          {% if day.due %}
              {{day.due}}
          {% endif %}
        </td>
      </tr>
    {% endfor %}
  {% endfor %}
  </tbody>
</table>


This calendar is subject to change. More details, e.g. lecture slides will be added as the semester continues. All work (except the project final report) is due on the specified date by **11:59 PM PT**{: .label .label-red }.
See [the syllabus](https://usc.simplesyllabus.com/en-US/doc/gs84ydm4d) for more details.

## Assignments and Grading

There will be three components to course grades:

* **Homeworks (30%).**
  * 10% X 3: There will be three coding homework assignments based on the topics of the class.
* **Quizzes (15%).**
  * 3% X 5: Multiple-Choice Questions and Short Answers. Missed quizzes will receive a zero grade, and there will be no make-up quizzes.
* **Class Projects (40%).**
  * Each student will do a group class project based on the topics covered in the class.  Students will propose their own project, do the research and build a proof-of-concept, create a video demonstration of the proof-of-concept, and present the project in their report.
  * Pitch: 5%
  * Proposal: 5%
  * Status Reports: 10%
  * Project Presentation: 10%
  * Final Write-up: 10%
* **Paper Presentations (10%).**
  * The project teams will present a scientific publication related to their project to the class.
  * All members of the team are expected to identify the central points of the research, and present that research to the class, as well as answer questions from the instructor, TAs and fellow students. <!-- * One member of team---randomly picked by the instructors a couple of hours before the presentation---will be the presenter, so please prepare accordingly! The presenter is responsible for the entire team’s grade, so please ensure both you and your teammates are prepared! The total time of each team's presentation is 5 minutes (3 min presentation + 2 min QA) - we will be very strict about this. If you are NOT presenting, you could participate in Q/A - bonus points will be awarded to folks who ask insightful questions (announce your name before you ask a question).  Each team will prepare 3 slides (via Google slides) to be shared with their assigned TAs by 11:59 PM the day before the presentation. Failure to share will cause a loss of grade.   * Content of the slides:     * Slide 1: Main Research Question in the paper,     * Slide 2: Main Results Summarized,     * Slide 3: How this influences your project. -->
* **Class Participation (5%)**
  * Each student’s engagements in course discussions during class and during project discussions.

Grading inquiries and questions about the grading of the homeworks and the quizzes can be asked (to the TA) within one week from the grading date (the date the grades are released). Grades will be available within 2-2.5 weeks after submission.

All written assignments related to the final project should use the standard [*ACL paper submission template](https://github.com/acl-org/acl-style-files).


## Late Days

Students are allowed a maximum of 6 late days total for all assignments (but NOT the quiz sheets). You may use up to 3 late days per assignment. Using one late day for a project assignment involves each of the teammates using a late day each. Partial late days are not permitted. For every extra late day beyond the allowed late days, the student / team will lose 20% of the grade for the assignment.

**Note:** Please familiarize yourself with the [academic policies](details/policies/#policies) and read the [note about student well-being](details/policies/#student-well-being).


## Pre-Requisites

Students are required to have either: 1) taken CSCI-270 Introduction to Algorithms and Theory of Computing (4.0 units) as well as one of: CSCI-360 Introduction to AI or CSCI-467 Introduction to Machine Learning; or 2) obtain explicit instructor approval.



## Similar Classes

- Graduate-level Applied NLP [Fall 2024 CSCI 544](https://swabhs.com/f24-csci544-appliednlp/)
- Undergraduate-level Special Topics: Language Models in NLP [Spring 2024 CSCI 499](https://swabhs.com/sp24-csci499-lm4nlp/)
  - See [previous class projects here](https://swabhs.com/sp24-csci499-lm4nlp/details/class-projects/).
- Undergraduate-level Special Topics: Language Models in NLP [Fall 2023 CSCI 499](https://swabhs.com/fall23-csci499-lm4nlp/)
  - See [previous class projects here](https://swabhs.com/fall23-csci499-lm4nlp/details/class-projects/).
