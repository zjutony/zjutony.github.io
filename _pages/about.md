---
permalink: /
title: "About me"
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---

<div class="home-hero">
  <div class="home-hero__content">
    <p class="home-hero__eyebrow">Personal Homepage</p>
    <h1>{{ site.author.name }}</h1>
    <p class="home-hero__lead">Master's student in Mechanical Engineering at Zhejiang University, working on robot learning, computer vision, and autonomous systems.</p>
    <p class="home-hero__body">Robot learning is the future. I focus on manipulation, perception, and practical systems, while also exploring startup ideas and product thinking.</p>
    <div class="home-hero__links">
      {% if site.author.email %}<a class="home-hero__icon-link" href="mailto:{{ site.author.email }}" aria-label="Email" title="Email"><i class="fas fa-envelope" aria-hidden="true"></i><span class="sr-only">Email</span></a>{% endif %}
      {% if site.author.github %}<a class="home-hero__icon-link" href="https://github.com/{{ site.author.github }}" aria-label="GitHub" title="GitHub"><i class="fab fa-github" aria-hidden="true"></i><span class="sr-only">GitHub</span></a>{% endif %}
      {% if site.author.linkedin %}<a class="home-hero__icon-link" href="https://www.linkedin.com/in/{{ site.author.linkedin }}" aria-label="LinkedIn" title="LinkedIn"><i class="fab fa-linkedin" aria-hidden="true"></i><span class="sr-only">LinkedIn</span></a>{% endif %}
      {% if site.author.orcid %}<a class="home-hero__icon-link" href="{{ site.author.orcid }}" aria-label="ORCID" title="ORCID"><i class="fab fa-orcid" aria-hidden="true"></i><span class="sr-only">ORCID</span></a>{% endif %}
      {% if site.author.youtube %}<a class="home-hero__icon-link" href="https://www.youtube.com/@{{ site.author.youtube }}" aria-label="YouTube" title="YouTube"><i class="fab fa-youtube" aria-hidden="true"></i><span class="sr-only">YouTube</span></a>{% endif %}
    </div>
    <div class="home-hero__nav">
      <a href="#research">Research</a>
      <a href="#education">Education</a>
      <a href="#experience">Working Experience</a>
      <a href="#projects">Personal Projects</a>
    </div>
  </div>

  <div class="home-hero__portrait">
    <img src="/images/{{ site.author.avatar }}" alt="{{ site.author.name }}">
    <div class="home-hero__note">Based in Hangzhou · Zhejiang University</div>
  </div>
</div>

<section class="home-section" id="research">
  <div class="home-section__head">
    <h2>Research</h2>
    <p>Robot learning is the future.</p>
  </div>
  <div class="home-list home-list--research home-list--compact">
    {% assign pubs = site.publications | sort: 'date' | reverse %}
    {% for p in pubs limit:5 %}
    <article class="home-card home-card--pub">
      <h3><a href="{{ p.url }}">{{ p.title }}</a></h3>
      {% if p.date %}<p class="home-card__meta">{{ p.date | date: "%Y" }}{% if p.venue %} · {{ p.venue }}{% endif %}</p>{% endif %}
      {% if p.authors %}<p class="home-card__authors">{{ p.authors }}</p>{% endif %}
    </article>
    {% endfor %}
  </div>
</section>

<section class="home-section" id="education">
  <div class="home-section__head">
    <h2>Education</h2>
  </div>
  <div class="home-timeline">
    <div class="home-timeline__item">
      <span class="home-timeline__date">2025 - Present</span>
      <div>
        <h3>Zhejiang University</h3>
        <p>Master's student in Mechanical Engineering.</p>
      </div>
    </div>
    <div class="home-timeline__item">
      <span class="home-timeline__date">2021 - 2025</span>
      <div>
        <h3>Zhejiang University</h3>
        <p>B.Eng. in Biosystems Engineering, with a minor in Innovation and Entrepreneurship Management.</p>
      </div>
    </div>
  </div>
</section>

<section class="home-section" id="experience">
  <div class="home-section__head">
    <h2>Working Experience</h2>
  </div>
  <div class="home-timeline">
    <div class="home-timeline__item">
      <span class="home-timeline__date">2026</span>
      <div>
        <h3>Robot learning intern</h3>
        <p>Internship experience in robotics research and engineering.</p>
      </div>
    </div>
    <div class="home-timeline__item">
      <span class="home-timeline__date">2025</span>
      <div>
        <h3>Research intern</h3>
        <p>Contributed to applied research in biomedical and robotic systems.</p>
      </div>
    </div>
  </div>
</section>

<section class="home-section" id="projects">
  <div class="home-section__head">
    <h2>Personal Projects</h2>
  </div>
  <div class="home-list home-list--projects">
    <article class="home-card home-card--accent">
      <h3>Autonomous robot manipulation demos</h3>
      <p>Prototype systems and experiments that connect perception, control, and learning for dexterous tasks.</p>
    </article>
    <article class="home-card home-card--accent">
      <h3>Technical writing and reading notes</h3>
      <p>Selected reflections on books, papers, and practical engineering topics, kept as a running archive.</p>
    </article>
  </div>
</section>

<section class="home-section home-section--footer">
  <p>If you want to collaborate on robotics, machine learning, or product ideas, feel free to reach out.</p>
</section>
