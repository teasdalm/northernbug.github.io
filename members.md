---
layout: page
title: Members
permalink: /members/
---

## Steering Committee

<table>
{% for member in site.data.members %}

    {% capture modulo %}{{ forloop.index | modulo: 3 }}{% endcapture %}
    {% if modulo == '1' %}
      <tr>
    {% endif %}
    <td align="center">
      {% if member.github %}
        {% avatar user=member.github size=100 %}<br>
      {% else %}
        <img src="/assets/no-github.png"><br>
      {% endif %}
      <strong>{{ member.name }}</strong>
      <p class="post-meta">{{ member.interests }}</p>
      {{ member.institute }}<br>
      {{ member.email }}<br>
      {% if member.twitter %}
        <a href="{{member.website}}">web</a> | <a href="https://twitter.com/{{member.twitter}}">twitter</a>
      {% else %}
        <a href="{{member.website}}">web</a>
      {% endif %}
    </td>
    {% if modulo == '0' or forloop.last %}
      </tr>
      {% endif %}
{% endfor %}
</table>

- Jess Buddle, University of Sheffield
- Alastair Droop, University of York
- Helen Hipperson, University of Sheffield
- Emily Johnson, University of Liverpool
- Khaled Jumah, University of Bradford
- Andrew Mason, University of York
- Freddie Mercer, Univeristy of Leeds
- Rachel Queen, Univeristy of Newcastle
- Jamie Soul, University of Liverpool

<!---
To Add yourself to the members table:
in the data directory you need to add yourself to the members.yml file:

- github: markdunning
  name: Mark Dunning
  institute: Sheffield University Bioinformatics Core
  email: m.j.dunning@sheffield.ac.uk


-->


## Alumini

<table>
{% for member in site.data.alumni %}
  {% capture modulo %}{{ forloop.index | modulo: 3 }}{% endcapture %}
    {% if modulo == '1' %}
      <tr>
    {% endif %}
    <td align="center">
      {% if member.github %}
        {% avatar user=member.github size=100 %}<br>
        {% else %}
        <img src="/assets/no-github.png"><br>
      {% endif %}
      <strong>{{ member.name }}</strong><br>
      {{ member.institute }}<br>
      {{ member.email }}<br>
      <a href="{{member.website}}">{{member.website}}</a>
     </td>
    {% if modulo == '0' or forloop.last %}
    </tr>
    {% endif %}
{% endfor %}
</table>
