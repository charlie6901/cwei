---
title: Projects
# feature_text: |
  # A demo of Markdown and HTML includes
# feature_image: "https://picsum.photos/2560/600?image=873"
excerpt: "A demo of Markdown and HTML includes"
aside: false
layout: page
---


{% assign collectiondata = site.collections | where: "label", "projects" | first %}
<p>{{ collectiondata.description }}</p>

<ul>
  {% for post in site.projects %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>