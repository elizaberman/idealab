---
title: "IDEA Lab - Publications"
layout: gridlay
excerpt: "IDEA Lab — Publications"
sitemap: false
permalink: /publications/
---

# Publications

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  {% if publi.image and publi.image != "" %}
  <img src="{{ '/images/pubpic/' | relative_url }}{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  {% endif %}
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  {% if publi.news1 and publi.news1 != "" %}
  <p class="text-danger"><strong>{{ publi.news1 }}</strong></p>
  {% endif %}
  {% if publi.news2 and publi.news2 != "" %}
  <p>{{ publi.news2 }}</p>
  {% endif %}
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p>&nbsp;</p>


