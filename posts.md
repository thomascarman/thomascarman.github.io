---
layout: default
---

# All Blog Posts

{% assign sorted_posts = site.posts | sort: 'date' | reverse %}
{% for post in sorted_posts %}

<div style="margin-bottom: 30px; border-bottom: 1px solid #333; padding-bottom: 20px;">
  <h2 style="margin-bottom: 5px;"><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <small style="color: #b5e853;">{{ post.date | date: "%B %d, %Y" }}</small>
  {% if post.tags %}
  <small style="color: #999;">
    {% for tag in post.tags %}
    <em>#{{ tag }}</em>{% unless forloop.last %}, {% endunless %}
    {% endfor %}
  </small>
  {% endif %}
  <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
  <a href="{{ post.url }}">Read more →</a>
</div>
{% endfor %}

{% if site.posts.size == 0 %}

<p>No posts yet. Check back soon!</p>
{% endif %}

---

[← Back to Home](/)
