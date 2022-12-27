---
layout: default
pagename: 記事の一覧
---

{% for tag in site.tags %}

  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.pagename }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

{% for post in site.posts %}

<div class="post_link">
    <div class="post_title">
    <a href="{{site.url}}{{ post.url }}"><img src="{{site.url}}/assets/images/{{ post.image }}"></a>
    <a href="{{site.url}}{{ post.url }}">{{ post.pagename }}</a>
    {{ post.date | date: "%Y/%m/%d"}} {{ post.tags }}
    </div>

</div>
{% endfor %}
