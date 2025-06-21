---
title: Publications
permalink: /Publications/
layout: splash
---

<style>
.publication-grid {
  display: flex;
  flex-direction: column;
  gap: 1.5em;
  margin-top: 2em;
}

.pub-card {
  display: flex;
  background: #fff;
  padding: 1em;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.05);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.pub-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 12px rgba(0,0,0,0.1);
}

.pub-thumbnail {
  width: 120px;
  height: auto;
  margin-right: 1.5em;
  border-radius: 4px;
  flex-shrink: 0;
  cursor: pointer;
}

.pub-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.pub-title {
  font-weight: bold;
  font-size: 1.2em;
  margin-bottom: 0.3em;
}

.pub-description {
  margin-bottom: 0.5em;
  line-height: 1.4;
}
</style>

<div class="publication-grid">
  {% for pub in site.data.publications %}
    <div class="pub-card">
      <a href="{{ pub.url }}" target="_blank">
        <img src="{{ pub.image }}" alt="{{ pub.short_title }}" class="pub-thumbnail">
      </a>
      <div class="pub-text">
        <div class="pub-title">{{ pub.short_title }}</div>
        <div class="pub-description">{{ pub.description }}</div>
      </div>
    </div>
  {% endfor %}
</div>
