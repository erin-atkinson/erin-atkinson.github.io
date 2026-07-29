---
layout: page
title: Publications
---
{% assign publications = site.publications | sort: "year" | reverse %}
{% for publication in publications %}
{% assign authors = publication.authors | split: ", " %}
{% for author in authors %} {% if author == "Erin Atkinson" %} **{{ author }}**, {% else %} {{ author }}, {% endif %} {% endfor %} ({{ publication.year }}) "{{ publication.title }}" *{{ publication.journal }}* [DOI]({{ publication.doi }}) [PDF](/pdfs/{{ publication.pdf }}.pdf)
    <small>{{ publication.contributions }}</small>
{% endfor %}
