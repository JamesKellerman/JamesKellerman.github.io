---
title: Projects
layout: page
order: 2
---

{% for project in site.data.projectsList %}
  {% if project.break %}
  <h2 class="no-border">{{project.name}}</h2>
  {% else %}
  <div class="project-grid">
  <div class="pure-g">
  <div class="pure-u-1 pure-u-md-1-2">
  <h3><a href="{{project.link}}">{{project.name}}</a></h3>
  <p>{{project.description}}</p>
  <p><b>Position</b>: {{project.position}}</p>
  </div>
  <div class="pure-u-1 pure-u-md-1-2">
    {% if project.image %}
      <img class="pure-img" src="{{project.image}}" alt="{{project.image}}">
    {% endif %}
  </div>
  </div>
  </div>
  {% endif %}
{% endfor %}
