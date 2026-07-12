---
layout: default
title: Concept map
permalink: /concept-map/
nav: true
nav_order: 2
description: where I talk about a concept I like and use, and explain why it is interesting to understand the world, and make-up tiny-funny metaphors to explain them
---

<div class="post">
  <header class="post-header">
    <h1 class="post-title">{{ page.title }}</h1>
    <p class="post-description">{{ page.description }}</p>
  </header>

  <div class="post-content">
    {% assign category_posts = site.categories["concept-map"] %}
    {% for post in category_posts %}
      <article class="post-preview mb-4">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p class="text-muted">{{ post.date | date: "%B %-d, %Y" }}</p>
        {% if post.description %}<p>{{ post.description }}</p>{% endif %}
      </article>
    {% endfor %}
  </div>
</div>