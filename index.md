---
layout: default
---

# Welcome to My Portfolio

Hi, I'm Thomas Carman — a passionate software engineer with expertise in full-stack development, DevOps, and cloud infrastructure. I love building scalable solutions and exploring cutting-edge technologies.

## What I Do

- **Full-Stack Development**: Building modern web applications with React, Node.js, and cloud-native architectures
- **DevOps & CI/CD**: Automating workflows, implementing robust testing pipelines, and ensuring code quality
- **Cloud Infrastructure**: Designing and deploying scalable solutions on cloud platforms
- **AI/ML Integration**: Leveraging AI technologies to enhance developer productivity and code quality

## Recent Blog Posts

{% assign sorted_posts = site.posts | sort: 'date' | reverse %}
{% for post in sorted_posts limit:5 %}
<div style="margin-bottom: 20px;">
  <h3 style="margin-bottom: 5px;"><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <small style="color: #b5e853;">{{ post.date | date: "%B %d, %Y" }}</small>
  {% if post.tags %}
  <small style="color: #999;">
    {% for tag in post.tags %}
    <em>#{{ tag }}</em>{% unless forloop.last %}, {% endunless %}
    {% endfor %}
  </small>
  {% endif %}
  <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
</div>
{% endfor %}

[View All Posts →](/posts.html)

---

## Connect With Me

- [GitHub](https://github.com/thomascarman)
- [View My Repositories](https://github.com/thomascarman?tab=repositories)

<small>Copyright &copy; Thomas Carman 2026 | Powered by [Jekyll Hacker Theme](https://github.com/pages-themes/hacker)</small>
