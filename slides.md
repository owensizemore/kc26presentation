---
theme: ./slidev-theme-cs390
title: Presentation Title
---

# GenAI-Powered Postsecondary Computer Science Education Tools
## A Systematic Literature Review

<div class="authors">
  <div class="author">
    <div class="author-name">Owen Sizemore</div>
    <img src="/logos/duke.png" alt="Duke" />
  </div>
  <div class="author">
    <div class="author-name">Seth Bernstein</div>
    <img src="/logos/michigan.png" alt="Michigan" />
  </div>
  <div class="author">
    <div class="author-name">Audrey Ostrom</div>
    <img src="/logos/santacruz.png" alt="Santa Cruz" />
  </div>
  <div class="author">
    <div class="author-name">Thomas Rexin</div>
    <img src="/logos/ncstate.png" alt="NC State" />
  </div>
  <div class="author">
    <div class="author-name">Kristin Stephens-Martinez</div>
    <img src="/logos/duke.png" alt="Duke" />
  </div>
</div>

<style>
.authors {
  display: flex;
  justify-content: space-evenly;
  align-items: flex-start;
  margin-top: 1.5rem;
}
.author {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.6rem;
  width: 18%;
}
.author-name {
  font-size: 0.95rem;
  font-weight: 500;
  line-height: 1.2;
  text-align: center;
}
.author img {
  width: 4.25rem;
  height: 4.25rem;
  object-fit: contain;
}   
</style>

---

# How do we regulate GenAI use in postsecondary CSEd?

- Ban it and AI-proof our classes
- Open the floodgates, encourage GenAI use from the introductory sequence onward
- <span v-mark.box.red="4">Guide students on how to use GenAI responsibly</span>

<!--
Consider replacing this with a spectrum, with option a on the left and option b on the right
-->
---

# What does this look like?
- Course interventions to learn new skills (prompting, evaluating GenAI output, etc.) 
- Assignments demonstrating the strengths/weaknesses of GenAI
- Student reflections to encourage thoughtful GenAI use
- <span v-mark.underline.blue="5">Tools with guardrails that scaffold learning and mitigate irresponsible GenAI use</span>

---

# Research Questions
1. **RQ1**: What approaches are currently used to build GenAI-powered postsecondary CSEd tools, and how are they motivated?
2. **RQ2**: What educational theories and framings inform the development of GenAI-powered postsecondary CSEd tools?
3. **RQ3**: What methods are used to empirically evaluate the effects of GenAI-powered postsecondary CSEd tools?

<!--Bold these-->
---

## Literature Review Methodology

<div class="w-full flex justify-center">

```mermaid {scale: 0.9}
%%{init: {"flowchart": {"wrappingWidth": 640, "minNodeWidth": 640, "rankSpacing": 32, "padding": 14, "useMaxWidth": false, "htmlLabels": true}}}%%
flowchart TD
    A[Create Inclusion/Exclusion Criteria based on seed papers] --> B["Search ACM DL, IEEE Xplore, Springer Link, and Scopus (n=1,834)"]
    B --> C["Apply IC/EC to titles/abstracts, remove duplicates (n=117)"]
    C --> D[Develop codebook with sample of papers, calculate IRR]
    D --> E["Apply IC/EC to full papers (n=72)"]
```

</div>

---

## Codebook

<div class="card-grid">

  <div class="info-card card-blue">
    <h3>Problem Space</h3>
    <p>Why is the tool being built?</p>
  </div>

  <div class="info-card card-green">
    <h3>Educational Framings</h3>
    <p>How does the tool support learning?</p>
  </div>

  <div class="info-card card-yellow">
    <h3>Pedagogical Features</h3>
    <p>How does the tool support learning?</p>
  </div>

  <div class="info-card card-purple">
    <h3>Delivery Method</h3>
    <p>How do students access the tool?</p>
  </div>

  <div class="info-card card-pink">
    <h3>Evaluation Goals</h3>
    <p>What do the authors want to understand about the tool?</p>
  </div>

  <div class="info-card card-teal">
    <h3>Evaluation Methods</h3>
    <p>How are the tools empirically evaluated?</p>
  </div>

</div>

<style>
.card-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  grid-template-rows: repeat(2, minmax(0, 1fr));
  gap: 12px;
  height: 390px;
  margin-top: 16px;
}

.info-card {
  box-sizing: border-box;
  min-height: 0;
  padding: 16px;
  border-radius: 12px;
  color: #263238;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.info-card h3 {
  margin: 0 0 8px;
  font-size: 1.15rem;
  font-weight: 600;
  text-align: center;
}

.info-card p {
  margin: 0;
  font-size: 0.95rem;
  line-height: 1.4;
  text-align: center;
}

.card-blue   { background: #e3efff; }
.card-green  { background: #e2f4e8; }
.card-yellow { background: #fff3cd; }
.card-purple { background: #eee5ff; }
.card-pink   { background: #ffe5ec; }
.card-teal   { background: #ddf5f2; }
</style>

---

# Motivations for building tools (RQ1)

- 60%: Desire to provide personalized, context-aware support to students
- 57%: Concern that unrestricted GenAI use can lead to overreliance
- 38%: Lack of scalable help-seeking in CS classrooms

---

# Tool features and approaches (RQ1)

- 81%: Scaffolded feedback so the tool doesn’t give away answers
- 57%: Adapt feedback to students’ prior interactions
- 25%: Ground responses in curated learning material

- 63% of tools delivered via a standalone web app, others embedded in course platforms or packaged as IDE extensions

<!--
Some of these bullets need qualifying examples
Is there a way to make the (RQ1) text smaller?
-->
---

# Educational Framings (RQ2)

- Most frequent mentions: Scaffolding (63%), Cognitive Load Theory (36%), metacognition (36%), Self-regulated learning (23%)
  - High co-occurrence between all these
- No clear trend for when or how framings were used
  - Median of 3 framings mentioned
  - 13% of papers did not include any coded framings, but still built on prior work
  - Disproved our assumption that tools would be built without considering existing research
- Still need to understand connections between cited research and tool features

<!--
Potentially split this into 2 slides
-->
---

# Evaluation Goals (RQ3)

- 79%: Understand student perceptions
- 61%: Understand student usage patterns
- 33%: Measure impact on learning outcomes
  - Many examples: 
    - Post-intervention test performance
    - Changes between pre- and post-test scores
    - Measurements of affective state (self-efficacy, nervousness, etc.)

<!--
Include references?
-->
---

# Evaluation Methods (RQ3)

- Post-surveys and logging usage data both common and frequently done together (also relatively easy to perform)
- 38% of papers that included post-surveys also included pre-surveys
  - Less emphasis on measuring changes, just want to understand how students like the tool
- Multiple evaluation methods were common
  - 69% of papers used between 2 and 4 methods
  - 42 distinct combinations of evaluation methods
  - Just 2 papers had no evaluations at all

---

# Other Trends

- Model choice reasoning remains unclear
  - Most used OpenAI models, but future tools will need to consider institutional compliance and data privacy
- Tools predominantly targeted introductory CS students
- Control groups were seldom used in evaluations

---

# Recommendations

<div class="rec-grid">

  <div class="info-card card-blue">
    <ph-question class="rec-icon" />
    <h3>Start with the problem, not the tool</h3>
  </div>

  <div class="info-card card-green">
    <ph-books class="rec-icon" />
    <h3>Build on what the field already knows</h3>
  </div>

  <div class="info-card card-yellow">
    <ph-binoculars class="rec-icon" />
    <h3>Investigate the gaps</h3>
  </div>

  <div class="info-card card-purple">
    <ph-arrows-split class="rec-icon" />
    <h3>Consider that students have alternatives</h3>
  </div>

</div>

<style>
.rec-grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 12px;
  height: 320px;
  margin-top: 16px;
}
.info-card {
  box-sizing: border-box;
  min-height: 0;
  padding: 16px;
  border-radius: 12px;
  color: #263238;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.info-card h3 {
  margin: 0;
  font-size: 1.05rem;
  font-weight: 600;
  line-height: 1.35;
  text-align: center;
}
.rec-icon {
  width: 2.75rem;
  height: 2.75rem;
  margin-bottom: 0.85rem;
  flex-shrink: 0;
}
.card-blue   { background: #e3efff; }
.card-green  { background: #e2f4e8; }
.card-yellow { background: #fff3cd; }
.card-purple { background: #eee5ff; }
</style>

---

# Start with the problem, not the tool

- Resist the urge to build a solution that doesn’t address a specific problem 
- Don't integrate GenAI tools into your course without a meaningful justification 
- Apply principles from learner-centered design, HCI, & needsfinding

---

# Build on what the field already knows

- Understand what other tools have gotten right and wrong already
- Meet the minimum standards for a quality custom tool (prompt engineering, filtering out bad responses, minimizing hallucinations, etc.)
- Make meaningful connections to prior research in CSEd, learning science, cognitive science, and other fields

---

# Investigate the gaps

- This SLR suggests a skew toward introductory programming
- Tools with lots of scaffolding might be great for a CS1/CS2 environment, but unclear how this would fare with other students
- Expand the scope of tools to include more students and more competencies (software engineering, system design, AI-assisted programming, etc.)

---

# Consider that students have alternatives

- "If you build it, they will come" doesn’t apply to a student with plenty of GenAI tools to choose from
- Students will always have access to commercial tools in unsupervised settings
- Make thoughtful design decisions to give students a good reason to use your tool
  - Use RAG/databases to leverage course content
  - Embed tools in existing course platforms
  - Make regular improvements in response to feedback

---
layout: two-cols-header
autoClicks: false
---

# Summary

::left::

<div class="summary-bullets">

- GenAI-powered postsecondary CSEd tools are one of many strategies to regulate GenAI use
- Tools integrate pedagogical features to promote learning and limit the pitfalls of commercial GenAI
- Tools are contextualized by a wide range of educational framings and many evaluation strategies
- Consider the problem at hand, prior research, and student alternatives when making the decision to develop a tool

</div>

::right::

<div class="qr-panel">
  <p class="qr-caption">GenAI-Powered Postsecondary Computer Science Education Tools: A Systematic Literature Review</p>
  <div class="qr-placeholder">QR code</div>
  <p class="qr-email">owen.sizemore@duke.edu</p>
</div>

<style>
.summary-bullets {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.summary-bullets ul {
  margin: 0;
}
.qr-panel {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.qr-caption {
  margin: 0;
  padding: 0 1.5rem 1.25rem;
  text-align: center;
  font-size: 1.05rem;
  line-height: 1.35;
}
.qr-placeholder {
  width: 11rem;
  height: 11rem;
  border: 2px dashed #9aa5b1;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #9aa5b1;
  font-size: 0.95rem;
}
.qr-email {
  margin: 0.85rem 0 0;
  text-align: center;
  font-size: 1.05rem;
}
</style>

