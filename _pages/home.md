---
layout: splash
permalink: /
hidden: true
title: " "
header:
    # overlay_image: assets/images/home-cover-img.jpg
    # caption: "credit: [**Unsplash**](https://unsplash.com/photos/blue-sky-with-clouds-viNPa2F7fnw)"
    overlay_color: "#34495e"
    actions:
        - label: "<i class='fas fa-bolt'></i> My roadmap"
          url: "/roadmap/"
tagline: >
    \" It may seem difficult at first, <br>
    but <strong style='color:#fa9b39;'>everything is difficult at first.</strong>\" <br><br>
    --- Miyamoto Musashi ---
# feature_row:
#   - image_path: assets/images/home-cover-img.jpg
#     alt: "customizable"
#     title: "Career"
#     excerpt: "All about programming that i use for work."
#     url: "#"
#     btn_class: "btn--primary"
#     btn_label: "Coming soon..."
#   - image_path: assets/images/home-cover-img.jpg
#     alt: "customizable"
#     title: "Interest"
#     excerpt: "Programming tools or topics that i currently interested in."
#     url: "#"
#     btn_class: "btn--primary"
#     btn_label: "Coming soon..."
#   - image_path: assets/images/home-cover-img.jpg
#     alt: "customizable"
#     title: "Hobby"
#     excerpt: "All of my hobbies that i'm doing at a time."
#     url: "#"
#     btn_class: "btn--primary"
#     btn_label: "Coming soon..."
# {% include feature_row id="feature_row" %}
# {% include video id="Z1mlyfza9i8" provider="youtube" %}
# {% include video id="fcvHgr9Nb7Q" provider="youtube" %}
reminder:
    - excerpt: "FORTIS FORTUNA ADIUVAT"
---

<div class="feature__wrapper">
  <div class="feature__item">
    <div class="archive__item">
      <div class="archive__item-body">
        <h2 class="archive__item-title" style="color: #fa9b39;">Recent Blog</h2>
        <div class="archive__item-excerpt">
          {% for post in site.posts limit:1 %}
            <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            {% if post.excerpt %}
              <p class="archive__item-excerpt" itemprop="description">
                {{ post.excerpt | markdownify | strip_html | truncate: 160 }}
              </p>
            {% endif %}
          {% endfor %}
        </div>
      </div>
    </div>
    <br>
  </div>

  <div class="feature__item">
    <div class="archive__item">
      <div class="archive__item-body">
        <h2 class="archive__item-title" style="color: #fa9b39;">Recent Book Summary</h2>
        <div class="archive__item-excerpt">
          {% assign latest_book = site.book | sort: 'date' | last %}
          <h3><a href="{{ latest_book.url | relative_url }}">{{ latest_book.title }}</a></h3>
          <p>{{ latest_book.description }}</p>
        </div>
      </div>
    </div>
    <br>
  </div>

  <div class="feature__item">
    <div class="archive__item">
      <div class="archive__item-body">
        <h2 class="archive__item-title" style="color: #fa9b39;">Recent Video Summary</h2>
        <div class="archive__item-excerpt">
          {% assign latest_video = site.video | sort: 'date' | last %}
          <h3><a href="{{ latest_video.url | relative_url }}">{{ latest_video.title }}</a></h3>
          <p>{{ latest_video.description }}</p>
        </div>
      </div>
    </div>
    <br>
  </div>
</div>

{% include feature_row id="reminder" type="center" %}
