---
layout: default
title: Predictions
permalink: /predictions/
---

# Predictions

{% assign posts = site.categories.predictions %}
{% if posts and posts.size > 0 %}
  {% assign posts_sorted = posts | sort: "date" | reverse %}
  {% for post in posts_sorted %}
- <a class="post-link" href="{{ post.url | relative_url }}">{{ post.date | date: "%Y-%m-%d" }} — {{ post.title }}</a>
  {% endfor %}
{% else %}
<p class="muted">No predictions yet.</p>
{% endif %}
