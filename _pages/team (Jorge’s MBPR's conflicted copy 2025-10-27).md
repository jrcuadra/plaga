---
title: "Plaga - Team"
layout: gridlay
excerpt: "Plaga: Team members"
sitemap: false
permalink: /team/
---

# Group Members


Jump to [faculty and postdocs](#faculty-and-postdocs), [students](#students), [alumni](#alumni).

## Faculty and Postdocs
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  {% if member.haswww == 1 %}
 <h4>[{{ member.name }}]({{ member.webpage }}){:target="_blank"}</h4>
  {% endif %}
  {% if member.haswww == 0 %}
 <h4>{{ member.name }}</h4>
  {% endif %}
<{{ member.email }}> <br>
 <i>{{ member.role }}</i><br>	
 <i> {{ member.education }}</i><br>
  {{member.area}}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}




## Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  {% if member.haswww == 1 %}
 <h4>[{{ member.name }}]({{ member.webpage }}){:target="_blank"}</h4>
  {% endif %}
  {% if member.haswww == 0 %}
 <h4>{{ member.name }}</h4>
  {% endif %}
<{{ member.email }}> <br>
 <i>{{ member.role }}</i><br>	
 <i> {{ member.education }}</i><br>
  {{member.area}}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  {% if member.haswww == 1 %}
 <h4>[{{ member.name }}]({{ member.webpage }}){:target="_blank"}</h4>
  {% endif %}
  {% if member.haswww == 0 %}
 <h4>{{ member.name }}</h4>
  {% endif %}
  <i>{{ member.duration }} <br></i>
  {{ member.info }}
  <ul style="overflow: hidden">

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Former visitors, part-time or Summer students
(not including students who later did their thesis with us)

<div class="row">

<div class="col-sm-4 clearfix">
<h4>Long-term visitors</h4>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Graduate students</h4>
{% for member in site.data.alumni_msc %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Undergrads</h4>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>

</div>

