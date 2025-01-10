---
title: "La Riviere Lab - Publications"
layout: gridlay
excerpt: "La Riviere Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

For a full list of publications and patents see [below](#full-list-of-publications) or go to [Google Scholar](https://scholar.google.com/citations?user=C2h_QC8AAAAJ).

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
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Patents
<em>D Modgil, P La Rivière, Y Liu, Z Yu</em><br />Method and apparatus for spectral computed tomography (CT) with multi-material decomposition into three or more material components<br /> <a href="https://patents.google.com/patent/US11238585B2/en">US11238585B2 (2022)</a>

<em>H Shroff, Y Wu, X Han, P La Rivière</em><br />Systems and methods for producing isotropic in-plane super-resolution images from line-scanning confocal microscopy<br /> <a href="https://patents.google.com/patent/WO2022150506A1/en">WO2022150506A1 (2022)</a>

<em>H Frisch, E Angelico, P La Rivière, B Adams, E Spieglan, J Shida, A Elagin, K Domurat-Sousa</em><br />Positron emission tomography systems based on ionization-activated organic fluor molecules, planar pixelated photodetectors, or both<br /> <a href="https://patents.google.com/patent/WO2022093732A1/en">WO2022093732A1 (2022)</a>

See <a href="https://patents.google.com/?inventor=Patrick+La+Riviere&num=25&sort=new&dups=language">more patents</a>


## List of publications since 2022
 *Last updated: July 2024*


{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
