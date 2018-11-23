---
bg: "travel.jpg"
layout: page
permalink: /travel/
title: "游记/travel"
crawlertitle: "travel articles"
summary: "曾经去过的那些有意思的地儿"
active: travel
---

<!-- {% for tag in site.tags %} -->
  <!-- {% assign t = tag | first %} -->
  <!-- {% assign posts = tag | last %} -->

  <!-- <h2 class="category-key" id="{{ t | downcase }}">{{ t | capitalize }}</h2> -->

  <ul class="year">
    {% for post in posts %}
      {% if post.tags contains 'travel' %}    
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
