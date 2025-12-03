---
title: "Projects"
description: "A selection of prototypes, shipped games, and technical explorations."
---

<div class="hero-intro">
  <h2 class="hero-title">GAME & SYSTEMS DESIGNER</h2>
  <p class="hero-subtitle">
    I design and build games and prototypes that explore systems, interaction, and player learning.
  </p>
</div>

<div class="project-list">
  {% assign projects = site.projects | sort: "year" | reverse %}
  {% for project in projects %}
  <article class="project-card">
    <h3 class="project-card-title">
      <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
    </h3>
    {% if project.short %}
      <p class="project-card-text">{{ project.short }}</p>
    {% endif %}
    <div class="project-meta">
      {% if project.year %}<span>{{ project.year }}</span>{% endif %}
      {% if project.engine %}<span>{{ project.engine }}</span>{% endif %}
    </div>
    <p class="project-card-link">
      <a href="{{ project.url | relative_url }}">View project →</a>
    </p>
  </article>
  {% endfor %}
</div>
