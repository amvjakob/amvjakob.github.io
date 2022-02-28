---
layout: archive
title: "Posts by category"
permalink: /categories/
author_profile: true
---

{% include base_path %}
{% include group-by-array collection=site.publications field="categories" %}

<div>
{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ category | slugify }}" class="archive__subtitle">{{ category }}</h2>
  {% for post in posts %}
    {% include archive-single-publication.html %}
  {% endfor %}
{% endfor %}
</div>