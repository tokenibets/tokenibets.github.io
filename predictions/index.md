---
layout: default
title: Predictions
---

# Predictions

{% assign posts_sorted = site.categories.predictions | sort: "date" | reverse %}
{% if posts_sorted and posts_sorted.size > 0 %}
  {% for post in posts_sorted %}
- <a class="post-link" href="{{ post.url | relative_url }}">{{ post.date | date: "%Y-%m-%d" }} — {{ post.title }}</a>
  {% endfor %}
{% else %}
<p class="muted">No predictions yet.</p>
{% endif %}
