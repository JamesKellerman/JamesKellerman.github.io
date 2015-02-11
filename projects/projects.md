---
title: Projects
layout: default
---

<div align="center">
	<h1>Projects</h1>
</div>

{% for project in site.data.projectsList %}
  {% if project.break %}
  <div class="jumbotron">
  <h2 class="no-border">{{project.name}}</h2>
  </div>
  {% else %}
    {% if project.hasLink %}
  <h3><a href="{{project.link}}" target="_blank">{{project.name}}</a></h3>
    {% else %}
  <h3>{{project.name}}</h3>
    {% endif %}

  <div class="container-fluid">
    <div class="col-md-4">
      <p><b>Language:</b> {{project.language}}</p>
      <p><b>Position:</b> {{project.position}}</p>
      <p>{{project.description}}</p>
    </div>
    <div class="col-md-8">
    {% if project.image %}
      <img class="img-responsive" src="{{project.image}}" alt="{{project.image}}">
    {% endif %}
    </div>
  </div>
  		
  {% endif %}
{% endfor %}
