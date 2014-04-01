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

<div class="sixteen columns">
[HiganWorks LLC Github Repos.](https://github.com/orgs/higanworks "HiganWorks LLC")
</div>

<div class="sixteen columns">
<hr />
</div>


<div class="one-third columns">
## Members
</div>

<div class="two-thirds columns">

{% for member in site.data.members %}

<h3>{{ member.name }}({{ member.yomi }})</h3>
<a href="https://github.com/{{ member.github }}" target="_blank">
  <img src="{{ member.image_url }}" alt="{{ member.yomi }}">
</a>
<h5>{{ member.role }}</h5>

<ul>
  <li>About {{ member.yomi }}
    <ul>
    {% for link in member.links %}
      <li><a href="{{ link[1] }}" target="_blank">{{ link[0] }}</a></li>
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

<div id="footer" class="sixteen columns">
<p>© 2011-2014 HiganWorks LLC</p>
</div>