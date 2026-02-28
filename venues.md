---
layout: default
title: Venues
---

<h1>Après-Ski Venues in Davos Platz</h1>

<div class="grid">
    {% for venue in site.venues %}
    <div class="card">
        <div class="card-image">
            {% if venue.image %}
            <img src="{{ venue.image }}" alt="{{ venue.name }}">
            {% endif %}
        </div>
        <div class="card-body">
            <h2 class="card-title">{{ venue.name }}</h2>
            <div class="card-meta">
                <span>{{ venue.type }}</span>
            </div>
            <p class="card-description">{{ venue.teaser | default: venue.content | strip_html | truncatewords: 20 }}</p>
            <div class="card-footer">
                <a href="{{ venue.url }}" class="cta">Mehr Erfahren →</a>
            </div>
        </div>
    </div>
    {% endfor %}
</div>
