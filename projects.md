---
title: Projects
layout: default
categories: navbar
priority: 0
---
{% assign projects = site.pages | where_exp: "page", "page.categories contains 'projects'" | sort: "priority", "last" %}
{% for project in projects %}
- [{{ project.title }}]({{ project.url }})
<br />{{ project.description }}
{% endfor %}
