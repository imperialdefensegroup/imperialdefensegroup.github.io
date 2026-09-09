---
layout: default
title: "Imperial Defense Group | Análisis táctico, defensa y seguridad"
description: "Análisis sobre defensa, seguridad, equipamiento táctico y material policial. Entrevistas y artículos de Imperial Defense Group."
---

<style>
  body {
    max-width: 100%;
    margin: 0;
    padding: 0;
    background: #0b0e0d;
    color: #e8ece7;
  }

  body > header,
  body > footer {
    max-width: 1120px;
    margin-left: auto;
    margin-right: auto;
    padding-left: 24px;
    padding-right: 24px;
  }

  body > header {
    padding-top: 26px;
  }

  body > header .site-title {
    color: #fff;
    letter-spacing: .04em;
    text-transform: uppercase;
  }

  body > header p {
    color: #9ca99d;
  }

  body > header hr,
  body > footer + hr,
  body > footer hr {
    border-color: #28322b;
  }

  body > footer {
    color: #9ca99d;
    padding-bottom: 28px;
  }

  .articles-landing {
    max-width: 1120px;
    margin: 0 auto;
    padding: 20px 24px 56px;
  }

  .articles-landing a {
    word-break: normal;
  }

  .eyebrow {
    display: inline-flex;
    align-items: center;
    gap: 9px;
    color: #c9d4c4;
    font-size: 12px;
    font-weight: 800;
    letter-spacing: .14em;
    text-transform: uppercase;
  }

  .eyebrow::before {
    content: "";
    width: 8px;
    height: 8px;
    background: #c1121f;
    box-shadow: 0 0 0 4px rgba(193, 18, 31, .18);
  }

  .landing-hero {
    position: relative;
    overflow: hidden;
    min-height: 375px;
    padding: 54px;
    border: 1px solid #334038;
    background:
      linear-gradient(90deg, rgba(8, 12, 10, .96) 2%, rgba(8, 12, 10, .84) 48%, rgba(8, 12, 10, .25) 100%),
      url("{{ "/assets/img/cz-p10c-upgrades.jpg" | relative_url }}") center/cover;
    box-shadow: 0 22px 52px rgba(0, 0, 0, .32);
  }

  .landing-hero::after {
    content: "";
    position: absolute;
    inset: 0;
    pointer-events: none;
    background-image: linear-gradient(rgba(255,255,255,.035) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,.025) 1px, transparent 1px);
    background-size: 28px 28px;
    mix-blend-mode: screen;
  }

  .hero-content {
    position: relative;
    z-index: 1;
    max-width: 670px;
  }

  .hero-content h1 {
    margin: 15px 0;
    color: #fff;
    font-size: clamp(32px, 5vw, 56px);
    line-height: 1.02;
    letter-spacing: -.035em;
  }

  .hero-content p {
    max-width: 600px;
    margin: 0;
    color: #d6ded4;
    font-size: 18px;
  }

  .hero-meta {
    display: flex;
    flex-wrap: wrap;
    gap: 9px;
    margin: 24px 0 30px;
  }

  .hero-meta span,
  .card-date {
    border: 1px solid #536157;
    background: rgba(18, 26, 21, .78);
    color: #dae4d7;
    padding: 6px 9px;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: .04em;
    text-transform: uppercase;
  }

  .cta {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 13px 19px;
    border: 1px solid #e33843;
    background: #c1121f;
    color: #fff !important;
    font-weight: 800;
    text-decoration: none;
    transition: transform .18s ease, background .18s ease;
  }

  .cta:hover {
    transform: translateY(-2px);
    background: #e01b29;
  }

  .cta::after {
    content: "→";
    font-size: 18px;
  }

  .content-header {
    display: flex;
    justify-content: space-between;
    align-items: end;
    gap: 20px;
    margin: 58px 0 22px;
  }

  .content-header h2 {
    margin: 6px 0 0;
    color: #fff;
    font-size: 31px;
    line-height: 1.1;
    letter-spacing: -.02em;
  }

  .content-header p {
    max-width: 400px;
    margin: 0;
    color: #aeb9ae;
    text-align: right;
  }

  .article-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 18px;
  }

  .article-card {
    display: flex;
    flex-direction: column;
    overflow: hidden;
    min-height: 100%;
    border: 1px solid #303b33;
    background: #121814;
    transition: transform .18s ease, border-color .18s ease, box-shadow .18s ease;
  }

  .article-card:hover {
    transform: translateY(-4px);
    border-color: #788d7b;
    box-shadow: 0 16px 32px rgba(0, 0, 0, .26);
  }

  .article-card-image {
    display: block;
    height: 170px;
    overflow: hidden;
    background: #202b22;
  }

  .article-card-image img {
    display: block;
    width: 100%;
    height: 100%;
    border-radius: 0;
    object-fit: cover;
    transition: transform .35s ease;
  }

  .article-card:hover img {
    transform: scale(1.05);
  }

  .article-card-body {
    display: flex;
    flex: 1;
    flex-direction: column;
    padding: 21px;
  }

  .article-card h3 {
    margin: 14px 0 10px;
    color: #fff;
    font-size: 21px;
    line-height: 1.15;
  }

  .article-card h3 a {
    color: inherit;
    text-decoration: none;
  }

  .article-card h3 a:hover {
    color: #dfead9;
  }

  .article-card p {
    margin: 0 0 18px;
    color: #aeb9ae;
    font-size: 15px;
  }

  .card-link {
    margin-top: auto;
    color: #e8eee4;
    font-size: 14px;
    font-weight: 800;
    letter-spacing: .03em;
    text-decoration: none;
    text-transform: uppercase;
  }

  .card-link:hover {
    color: #f04d57;
  }

  .card-link::after {
    content: "  →";
  }

  .topic-strip {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1px;
    margin-top: 42px;
    border: 1px solid #303b33;
    background: #303b33;
  }

  .topic-strip div {
    padding: 24px;
    background: #101612;
  }

  .topic-strip strong {
    display: block;
    margin-bottom: 5px;
    color: #fff;
    font-size: 15px;
    letter-spacing: .05em;
    text-transform: uppercase;
  }

  .topic-strip span {
    color: #aeb9ae;
    font-size: 14px;
  }

  @media (max-width: 760px) {
    body > header,
    body > footer,
    .articles-landing {
      padding-left: 16px;
      padding-right: 16px;
    }

    .landing-hero {
      min-height: auto;
      padding: 34px 25px;
      background:
        linear-gradient(90deg, rgba(8, 12, 10, .95), rgba(8, 12, 10, .74)),
        url("{{ "/assets/img/cz-p10c-upgrades.jpg" | relative_url }}") center/cover;
    }

    .content-header {
      display: block;
      margin-top: 40px;
    }

    .content-header p {
      margin-top: 12px;
      text-align: left;
    }

    .article-grid,
    .topic-strip {
      grid-template-columns: 1fr;
    }

    .article-card-image {
      height: 190px;
    }
  }
</style>

{% assign featured_url = "/entrevista-luis-casanas-parte-2/" %}

<section class="articles-landing">
  {% for post in site.posts %}
    {% if post.url == featured_url %}
    <section class="landing-hero" aria-labelledby="featured-title">
      <div class="hero-content">
        <span class="eyebrow">Entrevista destacada</span>
        <h1 id="featured-title">{{ post.title }}</h1>
        <p>{{ post.description }}</p>
        <div class="hero-meta">
          <span>Entrevista</span>
          <span>Policía y Guardia Civil</span>
          <span>{{ post.date | date: "%d.%m.%Y" }}</span>
        </div>
        <a class="cta" href="{{ post.url | relative_url }}">Leer entrevista</a>
      </div>
    </section>
    {% endif %}
  {% endfor %}

  <div class="content-header">
    <div>
      <span class="eyebrow">Archivo editorial</span>
      <h2>Análisis y entrevistas</h2>
    </div>
    <p>Defensa, seguridad y equipamiento táctico con un enfoque técnico y operativo.</p>
  </div>

  <section class="article-grid" aria-label="Todos los artículos">
    {% for post in site.posts %}
      {% unless post.url == featured_url %}
      <article class="article-card">
        <a class="article-card-image" href="{{ post.url | relative_url }}" aria-label="Leer {{ post.title }}">
          {% assign card_image = post.thumbnail | default: post.image %}
          {% if card_image %}
          <img src="{{ card_image | relative_url }}" alt="" loading="lazy">
          {% endif %}
        </a>
        <div class="article-card-body">
          <span class="card-date">{{ post.date | date: "%d.%m.%Y" }}</span>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p>{{ post.description | default: post.excerpt | strip_html | truncate: 160 }}</p>
          <a class="card-link" href="{{ post.url | relative_url }}">Abrir artículo</a>
        </div>
      </article>
      {% endunless %}
    {% endfor %}
  </section>

  <section class="topic-strip" aria-label="Temáticas">
    <div>
      <strong>Defensa y seguridad</strong>
      <span>Actualidad, capacidades y análisis de interés profesional.</span>
    </div>
    <div>
      <strong>Equipamiento táctico</strong>
      <span>Armas, protección, óptica y soluciones para operadores.</span>
    </div>
  </section>
</section>
