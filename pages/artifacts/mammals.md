---
title: Mammals
layout: page
permalink: /artifacts/mammals.html
---

{% assign filtered_items = site.data.artifacts | where_exp: "item", "item.subject contains 'Mammal'" %}

<div class="row">
  {% for item in filtered_items %}
  <div class="col-md-4 mb-3">
    <div class="card">
      {% if item.image_thumb %}
      <img src="{{ item.image_thumb | relative_url }}" class="card-img-top" alt="{{ item.title }}">
      {% endif %}
      <div class="card-body">
        <h5 class="card-title">{{ item.title }}</h5>
        <p class="card-text">{{ item.commonname }}</p>
        <a href="{{ '/items/' | relative_url }}{{ item.objectid }}.html" class="btn btn-primary">View Item</a>
      </div>
    </div>
  </div>
  {% endfor %}
</div>