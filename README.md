---
layout: default
---

# Bin.Liang's sharing space.

<nav>
<ul>
    {% for page in site.header_pages %}
        <li><a href="{{ page }}">{{ page | remove: '_pages/header/' | remove: '.html' }}</a></li>
    {% endfor %}
</ul>
</nav>

## 最新文章

{% for paper in site.pages %}
    {% if paper.path contains 'papers' %}
        <div>
            ### [{{ paper.title }}]({{ paper.url }})
            {{ paper.excerpt }}
        </div>
    {% endif %}
{% endfor %}
