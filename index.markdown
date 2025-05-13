---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home 
---
<section class="blog-tiles">
 <h1>Latest Posts</h1>
  <div class="tile-grid">
    {% for post in site.posts %}
      <div class="blog-tile">
        <a href="{{ post.url }}">
          <img src="{{ post.image }}" alt="{{ post.title }}">
        </a>
        <div class="tile-content">
          <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
          <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
          <p class="post-description">
            {{ post.description | default: post.excerpt }}
          </p>
        </div>
      </div>
    {% endfor %}
  </div>
</section>

