---
layout: page
title: Team
permalink: /team/
---

*The Vor AI Safety lab is currently being established. This page will be updated as soon as new members join.*

{% for member in site.team %}
{% if member.image and member.image != "" %}
<div style="max-width: 256px">
<img src="{{ member.image }}" alt="{{ member.name }}" style="width: 256px; height: 256px; object-fit: cover;"/>
{% if member.photocredit and member.photocredit != "" %}
<div style="text-align: center; font-weight: 200; "><small><i>
{% if member.photocredit_url and member.photocredit_url != "" %}
Photo: <a href=" {{ member.photocredit_url }}"> {{ member.photocredit }}</a>
{% else %}
Photo: {{ member.photocredit }}
{% endif %}
</i></small></div>
{% endif %}
</div>
{% endif %}
<h2>{{ member.name }}</h2>
<i>{{member.role }}</i>
<p class="prose">{{ member.content | markdownify }}</p>
{% endfor %}
