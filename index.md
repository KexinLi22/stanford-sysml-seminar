---
layout: default
---

# Stanford MLSys Seminar Series

Machine learning is driving exciting changes and progress in computing.
What does the ubiquity of machine learning mean for how people build and deploy
systems and applications?
What challenges does industry face when deploying machine learning systems in
the real world, and how can academia rise to meet those challenges?

In this seminar series, we want to take a look at the frontier of machine
learning systems, and how machine learning changes the modern programming
stack.
Our goal is to help curate a curriculum of awesome work in ML systems to help
drive research focus to interesting questions.

Starting in Fall 2020, we'll be livestreaming each talk in this seminar series
Thursdays 3-4 PT on [YouTube](https://www.youtube.com/channel/UCzz6ructab1U44QPI3HpZEQ),
and taking questions from the live chat, and videos of the talks will be
available on YouTube afterwards as well.
Give our channel a follow, and tune in every week for an exciting discussion!

{% for category in site.data.talks %}
# {{ category.type }}
<div class="talk-list">
  {% for talk in category.members %}
  <div class="talk list-group-item">
  <div class="talk-date">{{ talk.date }}</div>
  <div class="talk-presenter">{{ talk.speaker }}</div>
  {% if talk.title %}
  <div><span>{{ talk.title }}</span></div>
  {% endif %}
  {% if talk.abstract %}
    <details>
    <summary>Abstract</summary>
    {{ talk.abstract }}
    </details>
  {% endif %}
  {% if talk.recording %}
    <a href="{{ talk.recording }}">Recording</a>
  {% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}

<!--
<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.content }}
      </div>
    </article>
  {% endfor %}
</div>
-->