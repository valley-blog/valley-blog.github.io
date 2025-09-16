<!--
 * @Author: error: error: git config user.name & please set dead value or install git && error: git config user.email & please set dead value or install git & please set dead value or install git
 * @Date: 2025-09-16 14:56:28
 * @LastEditors: error: error: git config user.name & please set dead value or install git && error: git config user.email & please set dead value or install git & please set dead value or install git
 * @LastEditTime: 2025-09-16 15:43:31
 * @FilePath: /valley-blog.github.io/tags.md
 * 
 * Copyright (c) 2025 by error: git config user.email & please set dead value or install git, All Rights Reserved. 
-->
---
layout: default
title: 标签
permalink: /tags/
---
<h1>标签</h1>
<div class="tag-cloud">
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
    <a href="#{{ tag[0] | uri_escape }}" class="tag">#{{ tag[0] }}</a>
  {% endfor %}
</div>
<hr/>
{% for tag in tags %}
  <h2 id="{{ tag[0] | uri_escape }}">#{{ tag[0] }}</h2>
  <ul class="tag-posts">
    {% for post in tag[1] %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> <span class="post-meta">· {{ post.date | date: "%Y-%m-%d" }}</span></li>
    {% endfor %}
  </ul>
{% endfor %} 
