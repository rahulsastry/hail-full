---
title: "HAIL/ACCA - Publications"
layout: gridlay
excerpt: "HAIL/ACCA - Publications."
sitemap: false
permalink: /publications/
---


# Publications

## News

- Srinivas D, Anilkumar A. *[After the crash: The race to care](https://www.deccanherald.com/opinion/after-the-crash-the-race-to-care-3874592).* Deccan Herald. January 25, 2026. Accessed July 8, 2026.

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

## Peer-Reviewed Publications

- Ansari MF, Boopalan D, Inbaraj G, et al. Impact of a training program for community health officers on neurological disorders: insights from the Karnataka brain health initiative. *BMC Health Serv Res.* 2025;25(1):924. [doi:10.1186/s12913-025-12549-4](https://pubmed.ncbi.nlm.nih.gov/?term=10.1186%2Fs12913-025-12549-4)

- Mailankody P, Parthasarathy R, Randeep D, et al. Effectiveness of a training program in improving knowledge and skills about selected common neurological disorders among primary healthcare doctors: The Karnataka Brain Health Initiative (KaBHI) in India. *J Family Med Prim Care.* 2024;13(9):3719-3729. [doi:10.4103/jfmpc.jfmpc_1984_23](https://pubmed.ncbi.nlm.nih.gov/?term=10.4103%2Fjfmpc.jfmpc_1984_23)

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
