---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can also find a list of all my publications on my <a href="https://scholar.google.com/citations?user=fQNDQNcAAAAJ" target="_blank">Google Scholar</a> profile.

<br>

{% include base_path %}

{% capture current_year %}'None'{% endcapture %}
{% for post in site.publications reversed %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != current_year %}
<h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
    {% capture current_year %}{{ year }}{% endcapture %}
  {% endif %}

{% include archive-single-publication.html %}
{% endfor %}
