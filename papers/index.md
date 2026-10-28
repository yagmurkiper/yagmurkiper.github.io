---
layout: default
title: "Papers"
---
<style>

/* ======================================
   GENERAL PAGE STYLING
   ====================================== */

.papers-page {
  max-width: 850px;
}

.papers-intro {
  margin-bottom: 26px;
}

.papers-intro h1 {
  font-size: 2.5rem;
  margin-bottom: 8px;
}

.papers-intro p {
  color: #626b73;
}

.papers-section-title {
  font-size: 1.3rem;
  line-height: 1.4;
  margin: 0 0 14px;
  padding-bottom: 8px;
  border-bottom: 1px solid #d7dce2;
}

.papers-page section {
  margin-bottom: 30px;
}


/* ======================================
   PUBLICATION CARDS — COMPACT
   ====================================== */

.paper-card {
  background: #ffffff;
  border: 1px solid #e0e4e8;
  border-radius: 10px;
  padding: 16px 20px;
  margin-bottom: 12px;
}

.paper-year {
  color: #697682;
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.04em;
  margin: 0 0 5px;
  line-height: 1.3;
}

.paper-title {
  font-size: 1.12rem;
  font-weight: 700;
  line-height: 1.35;
  margin: 0 0 6px;
}

.paper-venue {
  font-size: 0.88rem;
  color: #616b75;
  line-height: 1.45;
  margin: 0 0 12px;
}


/* ======================================
   ABSTRACT / PDF / BIB BUTTONS
   ====================================== */

.paper-actions {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  gap: 7px;
}

.paper-actions summary,
.paper-actions .paper-link {
  display: inline-block;
  border: 1px solid #cbd5df;
  border-radius: 20px;
  background: #f7f9fc;
  padding: 4px 12px;
  font-size: 0.8rem;
  font-weight: 600;
  line-height: 1.5;
  cursor: pointer;
  list-style: none;
  color: #0947b4;
  text-decoration: none;
}

.paper-actions summary::-webkit-details-marker {
  display: none;
}

.paper-actions summary:hover,
.paper-actions .paper-link:hover {
  background: #eaf0f8;
}

.paper-actions details[open] {
  width: 100%;
}


/* ======================================
   ABSTRACT PANEL
   ====================================== */

.paper-detail {
  background: #f7f9fc;
  border-left: 3px solid #0947b4;
  padding: 14px 16px;
  margin-top: 10px;
  margin-bottom: 6px;
  font-size: 0.92rem;
  line-height: 1.7;
}

.paper-detail p {
  margin-top: 0;
  margin-bottom: 0;
}


/* ======================================
   BIB CODE EDITOR
   ====================================== */

.paper-detail.bib-panel {
  background: #192433;
  color: #d6e3f2;
  border-left: 3px solid #69c597;
  border-radius: 8px;
  padding: 16px;
}

/* Editor header */

.bib-header {
  display: flex;
  align-items: center;
  gap: 7px;
  margin-bottom: 12px;
  padding-bottom: 10px;
  border-bottom: 1px solid #364456;
}

.bib-dot {
  width: 9px;
  height: 9px;
  border-radius: 50%;
  display: inline-block;
}

.bib-dot.red {
  background: #ef7973;
}

.bib-dot.yellow {
  background: #e5bb66;
}

.bib-dot.green {
  background: #69c597;
}

.bib-header-label {
  margin-left: auto;
  font-family: monospace;
  font-size: 0.7rem;
  letter-spacing: 0.08em;
  color: #93a4b9;
}

/* Monospaced code */

.paper-detail.bib-panel pre {
  font-family: "SFMono-Regular", Consolas,
               "Liberation Mono", Menlo, monospace;
  font-size: 0.84rem;
  line-height: 1.8;
  white-space: pre-wrap;
  overflow-wrap: anywhere;
  color: #d6e3f2;
  background: transparent;
  border: none;
  padding: 0;
  margin: 0;
}

/* Syntax highlighting */

.bib-type {
  color: #ffbd8a;
}

.bib-key {
  color: #e9d48c;
}

.bib-field {
  color: #8cc8ff;
}

.bib-value {
  color: #a9e4b1;
}

</style>


<!-- ======================================
     PAPERS PAGE
     Content comes from _data/papers.yml
     ====================================== -->

<div class="papers-page">
  <!-- Loop through publication sections -->

  {% for section in site.data.papers.sections %}

  <section>

    <h2 class="papers-section-title">
      {{ section.title | escape }}
    </h2>


    <!-- Loop through papers in this section -->

    {% for paper in section.papers %}

    <article class="paper-card">

      <!-- YEAR -->

      <div class="paper-year">
        {{ paper.year | upcase | escape }}
      </div>


      <!-- TITLE -->

      <h3 class="paper-title">
        {{ paper.title }}
      </h3>


      <!-- PUBLICATION INFORMATION -->

      <p class="paper-venue">
        {{ paper.venue }}
      </p>


      <!-- ACTION BUTTONS -->

      <div class="paper-actions">


        <!-- ABSTRACT -->

        {% if paper.abstract %}

        <details>

          <summary>
            {{ paper.abstract_label | default: "Abstract" }}
          </summary>

          <div class="paper-detail">

            <p>{{ paper.abstract }}</p>

            {% if paper.abstract_note %}
            <small>
              {{ paper.abstract_note | escape }}
            </small>
            {% endif %}

          </div>

        </details>

        {% endif %}


        <!-- PDF AND EXTERNAL LINKS -->

        {% for link in paper.links %}

        <a class="paper-link"
           href="{{ link.url | escape }}"
           target="_blank"
           rel="noopener noreferrer">
          {{ link.label | escape }} ↗
        </a>

        {% endfor %}


        <!-- DOI (IF AVAILABLE) -->

        {% if paper.doi %}

        <a class="paper-link"
           href="https://doi.org/{{ paper.doi | escape }}"
           target="_blank"
           rel="noopener noreferrer">
          DOI ↗
        </a>

        {% endif %}


        <!-- BIB -->

        {% if paper.bib %}

        <details>

          <summary>BIB</summary>

          <div class="paper-detail bib-panel">

            <!-- Code editor header -->

            <div class="bib-header">
              <span class="bib-dot red"></span>
              <span class="bib-dot yellow"></span>
              <span class="bib-dot green"></span>
              <span class="bib-header-label">BIBTEX</span>
            </div>


            <!-- Syntax-highlighted citation -->

<pre><span class="bib-type">@{{ paper.bib.type | escape }}</span>{<span class="bib-key">{{ paper.bib.key | escape }}</span>,
{% for field in paper.bib.fields %}  <span class="bib-field">{{ field.name | escape }}</span> = {<span class="bib-value">{{ field.value | escape }}</span>}{% unless forloop.last %},{% endunless %}
{% endfor %}}</pre>

          </div>

        </details>

        {% endif %}


      </div>

    </article>

    {% endfor %}

  </section>

  {% endfor %}

</div>
