---
layout: default
title: "Papers"
---

<style>
/* Styling ONLY for the Papers page */

.papers-page {
  max-width: 850px;
}

.papers-intro {
  margin-bottom: 38px;
}

.papers-intro h1 {
  font-size: 2.5rem;
  margin-bottom: 10px;
}

.papers-intro p {
  color: #626b73;
}

.papers-section-title {
  font-size: 1.35rem;
  margin-bottom: 22px;
  padding-bottom: 12px;
  border-bottom: 1px solid #d7dce2;
}

/* Publication cards */

.paper-card {
  background: #ffffff;
  border: 1px solid #e0e4e8;
  border-radius: 12px;
  padding: 25px;
  margin-bottom: 22px;
}

.paper-year {
  color: #697682;
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 0.05em;
  margin-bottom: 12px;
}

.paper-title {
  font-size: 1.2rem;
  font-weight: 700;
  line-height: 1.5;
  margin-bottom: 10px;
}

.paper-venue {
  font-size: 0.92rem;
  color: #616b75;
  line-height: 1.6;
  margin-bottom: 18px;
}

/* Abstract, PDF, and BIB buttons */

.paper-actions {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  gap: 9px;
}

.paper-actions summary,
.paper-actions .paper-link {
  display: inline-block;
  border: 1px solid #cbd5df;
  border-radius: 20px;
  background: #f7f9fc;
  padding: 6px 15px;
  font-size: 0.85rem;
  font-weight: 600;
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

/* Abstract panel */

.paper-detail {
  background: #f7f9fc;
  border-left: 3px solid #0947b4;
  padding: 16px;
  margin-top: 12px;
  margin-bottom: 8px;
  font-size: 0.92rem;
  line-height: 1.7;
}

/* BIB: code editor appearance */

.paper-detail.bib-panel {
  background: #192433;
  color: #d6e3f2;
  border-left: 3px solid #69c597;
  border-radius: 8px;
  padding: 20px;
}

/* Code editor header */

.bib-header {
  display: flex;
  align-items: center;
  gap: 7px;
  margin-bottom: 15px;
  padding-bottom: 13px;
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

/* Monospaced typewriter font */

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

/* BIB syntax highlighting */

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

<div class="papers-page">

  <header class="papers-intro">
    <h1>Papers</h1>
    <p>Publications, manuscripts, and edited volumes.</p>
  </header>

  <section>

    <h2 class="papers-section-title">
      Articles peer-reviewed by abstract
    </h2>

    <!-- FIRST PAPER -->

    <article class="paper-card">

      <div class="paper-year">2022</div>

      <h3 class="paper-title">
        The position of the Q-like particle
        <em>ki</em> in Turkish and consequences
        for sluicing
      </h3>

      <p class="paper-venue">
        In Marianne Huijsmans and Sander Nederveen
        (eds.), <em>Proceedings of the Northwest
        Linguistics Conference 37</em>.
        Vancouver, BC: UBCWPL.
      </p>

      <div class="paper-actions">

        <!-- ABSTRACT -->

        <details>
          <summary>Abstract</summary>

          <div class="paper-detail">
            <p>
              The paper revises the distribution of the so-called Q-like particle ki in Turkish and
              investigates the consequences of this revised distribution for embedded sluicing constructions.
              Contrary to the claim that ki appears only in matrix clauses (Ince, 2012; Zidani-Eroğlu, 2019), I
              show that it can also occur in embedded interrogative clauses when they are tensed. Based on this
              possibility, I propose an analysis of sluicing constructions in Turkish, where I argue that wh-
              remnants in embedded sluicing environments raise to the [Spec CP] position of the closest tensed
              clause (contra Ince, 2012)
            </p>
          </div>
        </details>

        <!-- PDF -->

        <a class="paper-link"
           href="https://lingpapers.sites.olt.ubc.ca/files/2022/01/NWLC37_Kiper_Final.pdf"
           target="_blank"
           rel="noopener noreferrer">
          PDF ↗
        </a>

        <!-- BIB -->

        <details>
          <summary>BIB</summary>

          <div class="paper-detail bib-panel">

            <div class="bib-header">
              <span class="bib-dot red"></span>
              <span class="bib-dot yellow"></span>
              <span class="bib-dot green"></span>
              <span class="bib-header-label">BIBTEX</span>
            </div>

<pre><span class="bib-type">@inproceedings</span>{<span class="bib-key">kiper2022</span>,
  <span class="bib-field">author</span> = {<span class="bib-value">Kiper, Yağmur</span>},
  <span class="bib-field">title</span> = {<span class="bib-value">The position of the Q-like particle {ki} in Turkish and consequences for sluicing</span>},
  <span class="bib-field">booktitle</span> = {<span class="bib-value">Proceedings of the Northwest Linguistics Conference 37</span>},
  <span class="bib-field">editor</span> = {<span class="bib-value">Huijsmans, Marianne and Nederveen, Sander</span>},
  <span class="bib-field">year</span> = {<span class="bib-value">2022</span>},
  <span class="bib-field">publisher</span> = {<span class="bib-value">UBCWPL</span>},
  <span class="bib-field">address</span> = {<span class="bib-value">Vancouver, BC</span>}
}</pre>

          </div>
        </details>

      </div>

    </article>

  </section>

</div>