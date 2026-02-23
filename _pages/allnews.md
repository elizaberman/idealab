---
title: "News"
layout: textlay
excerpt: "IDEA Lab at NYU"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
{{ article.date }}
{{ article.headline | markdownify}}
{% endfor %}
