---
layout: default
pagename: 記事の一覧
---
{% for post in site.posts %}
<div class="post_link">
    <div class="post_title">
    <a href="{{site.url}}{{ post.url }}">{{ post.pagename }}</a>
    </div>
{{ post.date | date: "%Y/%m/%d"}} {{ post.tags }}
</div>
{% endfor %}
