---
layout: default
---

<div class="four columns">
![HiganWorks LLC](/assets/images/hw_logo_400.png)
</div>

<div class="eight columns offset-by-four">
# HiganWorks LLC
{: id="title" .remove-bottom }

##### put tagline here.
{: id="tagline" }
</div>

<div class="sixteen columns">
<hr />
</div>

<div class="one-third columns" style="float: right">
## Github Repositories
</div>

<div id="gitrepos" class="two-thirds columns" style="text-align: right">
{% for github in site.data.githubs %}
- [{{ github.desc }}]({{ github.url }})
{% endfor %}
</div>

<div class="sixteen columns">
<hr />
</div>


<div class="one-third columns">
## Member
</div>

<div class="two-thirds columns memberbox">

{% for member in site.data.members %}

<h3>{{ member.name }}({{ member.yomi }})</h3>
<a href="https://github.com/{{ member.github }}" target="_blank">
  <img src="{{ member.image_url }}" alt="{{ member.yomi }}">
</a>

##### {{ member.role }}
{: style="padding: 0 0 10px 0;" }

<p style="padding: 0 0 0 1em;">
{% for p_line in member.profile %}
{{ p_line }}<br />
{% endfor %}
</p>

<ul>
  <li>About {{ member.yomi }}
    <ul>
    {% for link in member.links %}
      <li><a href="{{ link[1] }}" target="_blank">{{ link[0] }}</a></li>
    {% endfor %}
    </ul>
  </li>
  <li>Contribs.
    <ul>
    {% for contrib in member.contribs %}
      <li><a href="{{ contrib[1] }}" target="_blank">{{ contrib[0] }}</a></li>
    {% endfor %}
    </ul>
  </li>
</ul>
<hr />
{% endfor %}

</div>

<div class="sixteen columns">
<hr />
</div>

<div class="one-third columns" style="float: right">
## Activities
</div>

<div id="acts" class="two-thirds columns">
{% for act in site.data.activities %}
<div class="ten columns">
### {{ act.name }}
<p class="actsdesc">{{ act.desc }}</p>

[{{ act.url }}]({{ act.url }})
<hr />
</div>
{% endfor %}
</div>


<div class="sixteen columns">
<hr />
</div>

<div id="footer" class="sixteen columns">
<p>© 2011-2014 HiganWorks LLC</p>
</div>
