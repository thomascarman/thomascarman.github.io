---
layout: default
---

# ThomasCarman.github.io

I'm hosted with Github Pages.

## Hello Github

Hi, so... I'm keep neglecting this repo and feel like I need to take a rehash at making this github pages.

## My Blog Posts

{% for tag in site.tags %}

  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

Copyright &copy; Thomas Carman 2022

[Jekyll Hacker Theme](https://github.com/pages-themes/hacker)
