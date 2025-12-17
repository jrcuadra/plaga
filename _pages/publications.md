---
title: "PLAGA - Publications"
layout: gridlay
excerpt: "PLAGA group -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

For a full list see [below](#full-list). For our most recent papers follow this [ADS link](https://ui.adsabs.harvard.edu/search/filter_database_fq_database=AND&filter_database_fq_database=database%3A%22astronomy%22&fq=%7B!type%3Daqp%20v%3D%24fq_database%7D&fq_database=(database%3A%22astronomy%22)&q=author%3A%22cuadra%2C%20jorge%22%20OR%20author%3A%22granda-mu%C3%B1oz%2C%20guido%22%20OR%20author%3A%22sandoval%2C%20astor%22%20%20%20year%3A2025-%20-%22HAWC%22&sort=date%20desc%2C%20bibcode%20desc&p_=0) (may contain false positives).


## Group highlights



{% assign number_printed = 0 %}
{% assign number_total = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% assign number_total = number_total | plus: 1 %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Full List
 (since 2015)
 <p> &nbsp; </p>

{% for publi in site.data.publist %}

{{ number_total }}.-  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
{% assign number_total = number_total | minus: 1 %}
{% endfor %}
