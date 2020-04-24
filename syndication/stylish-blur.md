---
layout: default
permalink: /blog/stylish-blur
pagination:
  enabled: true
  category: stylish-blur
title: Stylish Blur
---

# Stylish Blur

{% if paginator.page > 1 %}
  ## Page {{ paginator.page }}
{% endif %}

---

### Syndication
This is the full syndication of the blog: [Stylish Blur](https://stylishblur.tumblr.com), which was orignally posted on [Tumblr](https://tumblr.com).

---

iPhoneography of [jden redden](https://instagram.com/jden). Shot, edited and uploaded from an iPhone 4.

---

<p>Filter the archive by: <a href="{{ site.baseurl }}/archive">year</a>, <a href="{{ site.baseurl }}/archive/category">category</a>, or by <a href="{{ site.baseurl }}/archive/tag">tag</a>.</p>

<hr>

<div class="posts">
    
  {% for post in paginator.posts %}
  <article class="post">
    <h1 class="post-title">
      {% if post.external_url %}
        <a class="external-link" href="{{ post.external_url }}" onclick="captureOutboundLink(this); return false;">{{ post.title }}</a>&nbsp;
        <a href="{{ post.url }}">&#8734;</a>
      {% else %}
      <a href="{{ post.url }}">{{ post.title }}</a>
      {% endif %}
    </h1>

    <a class="post-date" href="{{ site.baseurl }}/archive/{{ post.date | date: '%Y/%m/%d' }}"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%A %-d %B %Y" }}</time></a>

    {{ post.content }}
    <hr>
  </article>
  {% endfor %}
</div>

<div class="pagination">
  {% if paginator.total_pages > 1 %}
      {% if paginator.next_page %}
        <a class="pagination-item older" href="{{ paginator.next_page_path }}">Older</a>
      {% else %}
        <span class="pagination-item older">Older</span>
      {% endif %}
      {% if paginator.previous_page %}
        <a class="pagination-item newer" href="{{ paginator.previous_page_path }}">Newer</a>
      {% else %}
        <span class="pagination-item newer">Newer</span>
      {% endif %}
  {% endif %}
</div>