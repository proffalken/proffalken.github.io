---
title: Other Projects
permalink: /projects/
icon: nc-spaceship
order: 2
---
Over the years I've been lucky enough to take part in or run a myriad of projects outside of my career, all with varying degrees of success!

This page lists a few of those projects with links to the website where available.

{% for item in site.data.projects %}

  {% capture modulo %}{{ forloop.index | modulo: 3 }}{% endcapture %}

  {% if modulo == '1' %}
<div class="row">
  <div class="col">
    <div class="card-deck">
  {% endif %}
    <div class="card card-stats">
      <div class="card-header">
        <h3 class="card-title">{{ item.name }}</h3>
      </div>
      <div class="card-body">
        <p class="card-text">{{ item.description | newline_to_br }}</p>
      </div>
      <div class="card-footer">
      <hr />
      <div class="icon-big text-center icon-warning">
      {% if item.website %}
        <a class="card-link" href="{{ item.website }}" alt="A link to the {{ item.name }} website"><i class="nc-icon nc-globe"></i></a>
      {% endif %}
      {% if item.twitter %}
        <a class="card-link" href="https://twitter.com/{{ item.twitter }}" alt="A link to the {{ item.name }} twitter account"><i class="fab fa-twitter"></i></a>
      {% endif %}
      </div>
      </div>
    </div>
  {% if modulo == '0' or forloop.last %}
    </div>
  </div>
</div>
  {% endif %}

{% endfor %}`
