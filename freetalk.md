---
bg: "wzm.jpg"
layout: page
permalink: /freetalk/
title: "想啥说啥/Free Talk"
crawlertitle: "free talk"
summary: "我们随便说点什么吧"
active: free talk
---

<!-- {% for tag in site.tags %} -->
  <!-- {% assign t = tag | first %} -->
  <!-- {% assign posts = tag | last %} -->

  <!-- <h2 class="category-key" id="{{ t | downcase }}">{{ t | capitalize }}</h2> -->

  <ul class="year">
    {% for post in posts %}
      {% if post.tags contains 'free talk' %}    
      <!-- if post.tags contains t -->
        <li>
          {% if post.lastmod %}
            <a href="{{ post.url | relative_url}}">{{ post.title }}</a>
            <span class="date">{{ post.lastmod | date: "%d-%m-%Y"  }}</span>
          {% else %}
            <a href="{{ post.url | relative_url}}">{{ post.title }}</a>
            <span class="date">{{ post.date | date: "%d-%m-%Y"  }}</span>
          {% endif %}
        </li>
      {% endif %}
    {% endfor %}
  </ul>

<!-- {% endfor %} -->
