---
layout: page
title: Posts
permalink: /posts/
background: '/assets/background.jpg'
---

<!-- Home Post List -->
{% for post in site.posts limit : 5 %}

<article class="post-preview">
  <a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">
    <h2 class="post-title">{{ post.title }}</h2>
    {% if post.subtitle %}
    <h3 class="post-subtitle">{{ post.subtitle }}</h3>
    {% else %}
    <h3 class="post-subtitle">{{ post.excerpt | strip_html | truncatewords: 15 }}</h3>
    {% endif %}
  </a>
  <p class="post-meta">Posted on {{ post.date | date: '%B %d, %Y' }}</p>
</article>

<hr>

{% endfor %}

