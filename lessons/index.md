---
 layout: default
 title: Clases - index
 weight: 3
---

<h2>{{ site.data.lectures.lecture_title }}</h2>
<ul>
  {% assign leclist = site.data.lectures.lectures %}
  {% for lecitem in leclist %}
    <li>
      <a href="{{ lecitem.url | prepend:site.baseurl }}">{{ lecitem.title }}</a>
    </li>
        {% if lecitem.subitems[0] %}
        <ul>
          {% for subitem in lecitem.subitems %}
              <li><a href="{{ subitem.url | prepend:site.baseurl }}">{{ subitem.title }}</a></li>
          {% endfor %}
        </ul>
     {% endif %}
  {% endfor %}
</ul>

