---
permalink: /dokumente/
title: "Dokumente"
---

{% assign image_files = site.static_files%}
{% for myimage in image_files %}
  {% if myimage.path contains '/dokumente/top/' %}
<a href="{{ myimage.path | relative_url }}">{{myimage.basename}}</a>
  {% endif %}
{% endfor %}



{% for i in (2008..2030) reversed %}
  {% assign year = 0 %}
  {% assign filterpath = '/dokumente/'| append: i %}
  {% for myimage in image_files %}
    {% if myimage.path contains filterpath %}
      {% assign year = 1 %}
    {% endif %}
  {% endfor %}

  {% if year == 1 %}
<b>{{i}}</b>
  {% endif %}

  {% for myimage in image_files %}

    {% if myimage.path contains filterpath %}

<a href="{{ myimage.path | relative_url}}">{{myimage.basename}}</a>

    {% endif %}


  {% endfor %}


{% endfor %}


