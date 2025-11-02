layout: default
title: Yi Wang · Research Assistant
description: Yi Wang is a research assistant at Fudan University's Institute of Big Data specializing in software security, system simulation, and AI-assisted security.

<section id="about" class="section">
  <div class="hero">
    <img src="{{ '/WangYi_Pic.jpg' | relative_url }}" alt="Portrait of Yi Wang" />
    <div>
      <h1>Yi Wang</h1>
      <p class="subtitle">Research Assistant · Institute of Big Data, Fudan University</p>
      <p>
        I focus on security-oriented program analysis, system simulation, and the deployment of
        AI-assisted defenses. My work bridges foundational methods and production-scale systems to
        deliver resilient solutions for academic collaborators and industry partners.
      </p>
      <div class="contact-links">
        <span>📍 Handan Road #220, Shanghai</span>
        <a href="mailto:yiwang_@fudan.edu.cn">yiwang_@fudan.edu.cn</a>
        <a href="{{ '/WangYi_Resume.md' | relative_url }}">Résumé (Markdown)</a>
      </div>
    </div>
  </div>
</section>

<section id="research" class="section">
  <h2 class="section-title">Research Interests</h2>
  <p>
    I explore practical techniques that make complex systems measurable and defensible. My recent efforts concentrate on
    building automated pipelines that combine symbolic reasoning, dynamic emulation, and LLM-based analyses for faster security insight.
  </p>
  <ul class="pill-list">
    <li>Program analysis &amp; vulnerability discovery</li>
    <li>Advanced fuzzing and testing orchestration</li>
    <li>Firmware and cyber-physical system emulation</li>
    <li>AI-assisted security for cloud and blockchain ecosystems</li>
  </ul>
</section>

<section id="projects" class="section">
  <h2 class="section-title">Active Industry Projects</h2>
  <div class="card-grid">
    <article class="card">
      <h3>Source Code Security Scan for PLC Systems</h3>
      <span class="meta">State Grid · 2023–2025</span>
      <p>
        End-to-end security review of industrial PLC codebases, combining static program slicing and intelligent triage to surface exploitable weaknesses early.
      </p>
    </article>
    <article class="card">
      <h3>Module Risk Evaluation Platform</h3>
      <span class="meta">SNPAS (State Nuclear Power Automation System Engineering Company) · 2023–2025</span>
      <p>
        Risk scoring engine that quantifies software supply-chain exposure for critical automation modules powering nuclear infrastructure.
      </p>
    </article>
    <article class="card">
      <h3>LLM-Assisted API Vulnerability Detection</h3>
      <span class="meta">Dewu · 2024–2025</span>
      <p>
        Hybrid analysis framework where LLM reasoning augments taint tracking and symbolic execution to validate API misconfigurations.
      </p>
    </article>
    <article class="card">
      <h3>AI Agent Driven Security Enhancement Framework</h3>
      <span class="meta">Huawei · 2024–present</span>
      <p>
        Autonomous guardrails that orchestrate agentic workflows for continuous hardening of large-scale cloud services and infrastructure.
      </p>
    </article>
  </div>
</section>

<section id="publications" class="section">
  <h2 class="section-title">Selected Publications</h2>
  {% assign publications = site.data.publications | sort: 'year' | reverse %}
  <div class="card-grid">
    {% for pub in publications %}
    <article class="card publication-card">
      <p class="publication-title">{{ pub.title }}</p>
      <p class="publication-meta">
        {{ pub.authors | join: ', ' }} · {{ pub.venue }} · {{ pub.year }}
        {% if pub.volume %} · Vol. {{ pub.volume }}{% endif %}
        {% if pub.issue %}({{ pub.issue }}){% endif %}
        {% if pub.pages %} · pp. {{ pub.pages }}{% endif %}
      </p>
      <div class="publication-links">
        {% if pub.doi %}
        <a class="link-tag" href="https://doi.org/{{ pub.doi }}" target="_blank" rel="noopener">DOI: {{ pub.doi }}</a>
        {% endif %}
        {% if pub.url %}
        <a class="link-tag" href="{{ pub.url }}" target="_blank" rel="noopener">Full text</a>
        {% endif %}
      </div>
      {% if pub.publisher %}
      <p class="publication-publisher">{{ pub.publisher }}</p>
      {% endif %}
      {% if pub.abstract %}
      <p>{{ pub.abstract }}</p>
      {% endif %}
      {% if pub.bibtex %}
      <details>
        <summary>BibTeX</summary>
        <pre>{{ pub.bibtex | escape_once }}</pre>
      </details>
      {% endif %}
    </article>
    {% endfor %}
  </div>
  <p style="margin-top: 1.5rem;">
    Download all entries as a single file:
    <a class="link-tag" href="{{ '/assets/publications.bib' | relative_url }}">publications.bib</a>
  </p>
</section>

<section id="background" class="section">
  <h2 class="section-title">Background</h2>
  <p>
    I received both my B.S. and Ph.D. in Computer Science and Technology from Nanjing University.
    Across academia and industry collaborations I have led efforts in binary hardening, secure system prototyping,
    and the deployment of LLM-driven security services that operate at production scale.
  </p>
</section>
