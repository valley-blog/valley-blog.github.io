---
layout: page
title: 标签
permalink: /tags/
---

<div class="tag-cloud">
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
    <a href="#{{ tag[0] | slugify }}" class="tag">#{{ tag[0] }}</a>
  {% endfor %}
</div>

<hr/>

{% for tag in tags %}
  <h2 id="{{ tag[0] | slugify }}">#{{ tag[0] }}</h2>
  <ul class="tag-posts">
    {% for post in tag[1] %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> <span class="post-meta">· {{ post.date | date: "%Y-%m-%d" }}</span></li>
    {% endfor %}
  </ul>
{% endfor %}