---
layout: default
title: Researcher's wanderings
permalink: /researchers-wanderings/
nav: true
nav_order: 3
description: where I talk about my experience as a young researcher doing historical research
---

<div class="post">
  <header class="post-header">
    <h1 class="post-title">{{ page.title }}</h1>
    <p class="post-description">{{ page.description }}</p>
  </header>

  <div class="post-content">
    {% assign category_posts = site.categories["researchers-adventures"] %}
    {% for post in category_posts %}
      <article class="post-preview mb-4">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p class="text-muted">{{ post.date | date: "%B %-d, %Y" }}</p>
        {% if post.description %}<p>{{ post.description }}</p>{% endif %}
      </article>
    {% endfor %}
  </div>
</div>