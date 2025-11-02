---
layout: default
title: Yi Wang · Research Assistant
description: Research assistant at Fudan University's Institute of Big Data focused on software security and AI-assisted defenses.
---

<section id="about" class="section">
  <div class="hero hero-condensed">
    <img src="{{ '/WangYi_Pic.jpg' | relative_url }}" alt="Portrait of Yi Wang" />
    <div>
      <h1>Yi Wang</h1>
      <p class="subtitle">Institute of Big Data, Fudan University</p>
      <p class="bio">
        Research assistant working on software security analysis, system emulation, and LLM-driven defenses for
        industrial and cloud-scale environments. B.S. &amp; Ph.D. in Computer Science, Nanjing University.
      </p>
      <div class="contact-links condensed">
        <a class="icon-link" href="mailto:yiwang_@fudan.edu.cn" aria-label="Email Yi Wang">yiwang_@fudan.edu.cn</a>
        <a class="icon-link" href="https://orcid.org/0009-0005-2866-7274" target="_blank" rel="noopener" aria-label="ORCID profile">
          <svg viewBox="0 0 256 256" role="img" aria-hidden="true" focusable="false">
            <circle cx="128" cy="128" r="128" fill="#A6CE39" />
            <path fill="#fff" d="M85.5 69.6v116.8h-20V69.6h20zm34.8 0c30.2 0 54.7 24.6 54.7 55s-24.5 55-54.7 55h-29.1v-110h29.1zm-.2 19.8h-8.9v70.3h8.9c19.2 0 33.9-15.7 33.9-35.2 0-19.6-14.7-35.1-33.9-35.1z" />
          </svg>
          ORCID
        </a>
        <span>📍 Handan Road #220, Shanghai</span>
      </div>
    </div>
  </div>
</section>

<section id="focus" class="section">
  <h2 class="section-title">Focus</h2>
  <ul class="pill-list">
    <li>Vulnerability discovery &amp; program analysis</li>
    <li>Firmware and cyber-physical system emulation</li>
    <li>LLM-assisted security engineering</li>
  </ul>
</section>

<section id="projects" class="section">
  <h2 class="section-title">Current Work</h2>
  <div class="card-grid">
    <article class="card">
      <h3>State Grid · PLC Code Security</h3>
      <span class="meta">2023–2025</span>
      <p>Scalable inspection pipeline for industrial PLC software with automated triage.</p>
    </article>
    <article class="card">
      <h3>SNPAS · Module Risk Evaluation</h3>
      <span class="meta">2023–2025</span>
      <p>Risk scoring for critical nuclear automation components and supply-chain dependencies.</p>
    </article>
    <article class="card">
      <h3>Dewu · LLM-Assisted API Hardening</h3>
      <span class="meta">2024–2025</span>
      <p>Combine taint tracking with LLM reasoning to flag exploitable API behaviors.</p>
    </article>
    <article class="card">
      <h3>Huawei · Autonomous Security Agents</h3>
      <span class="meta">2024–present</span>
      <p>Agent workflows that continuously harden large-scale cloud infrastructure.</p>
    </article>
  </div>
</section>

<section id="publications" class="section">
  <h2 class="section-title">Selected Publications</h2>
  {% assign publications = site.data.publications | sort: 'year' | reverse %}
  <div class="card-grid">
    {% for pub in publications %}
    <article class="card publication-card compact">
      <p class="publication-title">{{ pub.title }}</p>
      <p class="publication-meta">
        {{ pub.authors | join: ', ' }} · {{ pub.venue }} {{ pub.year }}{% if pub.volume %}, {{ pub.volume }}{% if pub.issue %}({{ pub.issue }}){% endif %}{% endif %}{% if pub.pages %}, {{ pub.pages }}{% endif %}
      </p>
      <div class="publication-links">
        {% if pub.doi %}
        <a class="link-tag" href="https://doi.org/{{ pub.doi }}" target="_blank" rel="noopener">DOI</a>
        {% endif %}
        {% if pub.url %}
        <a class="link-tag" href="{{ pub.url }}" target="_blank" rel="noopener">Full text</a>
        {% endif %}
      </div>
      {% if pub.bibtex %}
      <details>
        <summary>BibTeX</summary>
        <pre>{{ pub.bibtex | escape_once }}</pre>
      </details>
      {% endif %}
    </article>
    {% endfor %}
  </div>
</section>
