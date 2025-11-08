---
layout: default
title: Predictions
permalink: /predictions/
---

# Predictions

{% assign posts = site.posts | where_exp: "p", "p.tags contains 'prediction' or p.tags contains 'predictions' or p.title contains 'Prediction' or p.title contains 'Predictions' or p.title contains 'prediction' or p.title contains 'predictions' or p.categories contains 'predictions'" %}
{% if posts and posts.size > 0 %}
  {% assign posts_sorted = posts | sort: "date" | reverse %}
  <ul>
  {% for post in posts_sorted %}
    <li><a class="post-link" href="{{ post.url | relative_url }}">{{ post.date | date: "%Y-%m-%d" }} — {{ post.title }}</a></li>
  {% endfor %}
  </ul>
{% else %}
  <p class="muted">No predictions yet.</p>
{% endif %}
