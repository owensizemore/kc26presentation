---
theme: ./slidev-theme-cs390
title: Presentation Title
class: title-slide
---

# GenAI-Powered Postsecondary Computer Science Education Tools
## A Systematic Literature Review

<div class="authors">
  <div class="author">
    <div class="author-name"><strong>Owen Sizemore</strong></div>
    <div class="author-photo-wrap">
      <div class="author-photo wide-shot">
        <img src="/authors/owen.jpg" alt="Owen Sizemore" />
      </div>
      <div class="author-badge">
        <img src="/logos-square/duke.png" alt="Duke" />
      </div>
    </div>
  </div>
  <div class="author">
    <div class="author-name">Seth Bernstein</div>
    <div class="author-photo-wrap">
      <div class="author-photo">
        <img src="/authors/seth.png" alt="Seth Bernstein" />
      </div>
      <div class="author-badge">
        <img src="/logos-square/michigan.png" alt="Michigan" />
      </div>
    </div>
  </div>
  <div class="author">
    <div class="author-name">Audrey Ostrom</div>
    <div class="author-photo-wrap">
      <div class="author-photo">
        <img src="/authors/audrey.png" alt="Audrey Ostrom" />
      </div>
      <div class="author-badge badge-ucsc">
        <img src="/logos-square/santacruz.jpg" alt="UCSC" />
      </div>
    </div>
  </div>
  <div class="author">
    <div class="author-name">Thomas Rexin</div>
    <div class="author-photo-wrap">
      <div class="author-photo">
        <img src="/authors/thomas.jpg" alt="Thomas Rexin" />
      </div>
      <div class="author-badge badge-ncstate">
        <img src="/logos-square/ncstate.png" alt="NC State" />
      </div>
    </div>
  </div>
  <div class="author">
    <div class="author-name">Kristin Stephens-Martinez</div>
    <div class="author-photo-wrap">
      <div class="author-photo">
        <img src="/authors/kristin.jpg" alt="Kristin Stephens-Martinez" />
      </div>
      <div class="author-badge">
        <img src="/logos-square/duke.png" alt="Duke" />
      </div>
    </div>
  </div>
</div>

<style>
.authors {
  display: grid;
  grid-template-columns: repeat(5, max-content);
  justify-content: center;
  column-gap: 3.5rem;
  margin-top: 1.5rem;
  margin-left: -2.5rem;
  margin-right: -2.5rem;
  align-items: start;
}
.author {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.55rem;
}
.author-name {
  font-size: 0.9rem;
  font-weight: 500;
  line-height: 1.2;
  text-align: center;
  white-space: nowrap;
}
.author-photo-wrap {
  position: relative;
  width: 6rem;
  height: 6rem;
  flex-shrink: 0;
}
.author-photo {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  overflow: hidden;
}
.author-photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center 22%;
}
.author-photo.wide-shot img {
  object-position: center 12%;
  transform: scale(1.65);
  transform-origin: center 18%;
}
.author-badge {
  position: absolute;
  right: -0.15rem;
  bottom: -0.15rem;
  width: 2.05rem;
  height: 2.05rem;
  border-radius: 50%;
  overflow: hidden;
  border: 2.5px solid #fff;
  background: #fff;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.28);
}
.author-badge img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.author-badge.badge-ucsc img {
  transform: scale(1.22);
}
.author-badge.badge-ncstate {
  background: #cc0000;
}
.author-badge.badge-ncstate img {
  object-fit: contain;
  transform: scale(1.28);
}
</style>

<!--
Hello all! My name is Owen Sizemore, and I am a second-year Computer Science PhD student at Duke University. It is an immense privilege to be able to present our work here at Koli, and an even greater privilege to be the first presenter of the conference. 

This work is a collaboration with other PhD students across the United States, and I'm very excited to share with you our findings on GenAI-powered Postsecondary Computer Science Education tools. 

Before I get into the weeds of the scope of our paper, though, I want to contextualize why we felt this topic was important and our strategy for conducting our literature review. Our work is part of a larger question that many CS educators and researchers have been grappling with over the past couple of years, which is...
-->
---

# How do we regulate GenAI use in postsecondary CSEd?

<SpectrumArrow />

<!--
I don't need to remind you all of the challenges that have been presented by the proliferation of GenAI in postsecondary CS classrooms, which span concerns about overreliance, impacts on critical thinking and problem-solving skills, and ensuring that students are prepared for advanced work and careers in computer science.

What I do want to discuss though is how we categorize strategies from instructors to address these challenges. We can think of it as a spectrum where on one side we are encouraging less AI use and on the other more AI use. Some responses by instructors have been very heavy-handed, such as by attempting to ban the use of GenAI in classrooms entirely, or allowing unbridled use without any restrictions or guardrails. 

Both of these approaches come with risks, so we want to consider a more nuanced set of strategies where we are guiding students toward responsible AI use, acknowledging that students have access to tools like ChatGPT and Claude but also encouraging them to use the tools in a way that supports their learning.
-->
---

# What does this look like?
- Course interventions to learn new skills (prompting, evaluating GenAI output, etc.) 
- Assignments demonstrating the strengths/weaknesses of GenAI
- Student reflections to encourage thoughtful GenAI use
- <span v-mark.underline.green="5">Custom tools with guardrails to scaffold learning and mitigate irresponsible GenAI use</span>

<!--
So what are some examples of strategies to support responsible AI use? There are many approaches

We wanted to explore one specific approach, which is the use of custom tools that offer an alternative to commercial tools like ChatGPT. I have a software engineering background, and I was particularly interested in what motivated educators to build custom tools and how they distinguished themselves from commercial tools.
-->
---
class: tool-flow-slide
---

<h1 class="tool-flow-title">Tool Flow</h1>

<div class="tool-flow">

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 10, "rankSpacing": 4, "padding": 8, "htmlLabels": true, "useMaxWidth": true}, "themeVariables": {"fontSize": "22px"}}}%%
flowchart LR
    subgraph c1[" "]
      direction TB
      SP["<img src='/public/icons/person.png' width='72' height='72' style='width:72px;height:72px;object-fit:contain;aspect-ratio:1/1' /> <strong>Student prompt</strong>"]
      CTX["<img src='/public/icons/text.png' width='72' height='72' style='width:72px;height:72px;object-fit:contain;aspect-ratio:1/1' />Context"]
    end
    subgraph c2[" "]
      direction TB
      IC["<img src='/public/icons/filter.png' width='72' height='72' style='width:72px;height:72px;object-fit:contain;aspect-ratio:1/1' />Input filtering"]
      SYS["<img src='/public/icons/guide.png' width='72' height='72' style='width:72px;height:72px;object-fit:contain;aspect-ratio:1/1' /> <strong>System prompts</strong>"]
      KB["<img src='/public/icons/database.png' width='72' height='72' style='width:72px;height:72px;object-fit:contain;aspect-ratio:1/1' />Knowledge base"]
    end
    subgraph c3[" "]
      LLM["<img src='/public/icons/chatgpt.png' width='72' height='72' style='width:72px;height:72px;object-fit:contain;aspect-ratio:1/1' /> <strong>LLM Endpoint</strong>"]
    end
    subgraph c4[" "]
      RC["<img src='/public/icons/checks.png' width='72' height='72' style='width:72px;height:72px;object-fit:contain;aspect-ratio:1/1' />Response checks"]
    end
    subgraph c5[" "]
      OUT["<img src='/public/icons/reply.png' width='72' height='72' style='width:72px;height:72px;object-fit:contain;aspect-ratio:1/1' /> <strong>Response delivered to student</strong>"]
    end

    SP --> IC
    CTX --> IC

    IC --> LLM
    SYS --> LLM
    KB --> LLM

    LLM --> RC
    RC --> OUT

    classDef col1 fill:#e3efff,stroke:#6ea8dc,color:#000,stroke-width:1px
    classDef col1Bold fill:#e3efff,stroke:#3d7ab8,color:#000,stroke-width:12px,font-weight:bold
    classDef col2 fill:#e2f4e8,stroke:#6bb57c,color:#000,stroke-width:1px
    classDef col2Bold fill:#e2f4e8,stroke:#2e7d3a,color:#000,stroke-width:12px,font-weight:bold
    classDef col3 fill:#fff3cd,stroke:#d4b44a,color:#000,stroke-width:1px
    classDef col3Bold fill:#fff3cd,stroke:#b89620,color:#000,stroke-width:12px,font-weight:bold
    classDef col4 fill:#eee5ff,stroke:#a78bdb,color:#000,stroke-width:1px
    classDef col5 fill:#ddf5f2,stroke:#5aaaa0,color:#000,stroke-width:1px
    classDef col5Bold fill:#ddf5f2,stroke:#2d8a80,color:#000,stroke-width:12px,font-weight:bold
    class SP col1Bold
    class CTX col1
    class IC,KB col2
    class SYS col2Bold
    class LLM col3Bold
    class RC col4
    class OUT col5Bold
    style c1 fill:none,stroke:none,color:transparent
    style c2 fill:none,stroke:none,color:transparent
    style c3 fill:none,stroke:none,color:transparent
    style c4 fill:none,stroke:none,color:transparent
    style c5 fill:none,stroke:none,color:transparent
```

</div>

<style>
.tool-flow-title {
  position: absolute;
  top: 2rem;
  right: 4rem;
  margin: 0;
  text-align: right;
  z-index: 5;
  pointer-events: none;
}
.tool-flow {
  box-sizing: border-box;
  width: 100%;
  padding: 0 1rem;
  margin: 0 auto;
}
.tool-flow :deep(.mermaid) {
  display: block;
  width: 100%;
}
.mermaid img {
  width: 72px !important;
  height: 72px !important;
  max-width: 72px !important;
  object-fit: contain !important;
  aspect-ratio: 1 / 1;
}
</style>

<!--
Within our literature review we observed a wide range of tool designs and architectures, but the most common was a text-based interface similar to ChatGPT or Claude, but with some additional components and guardrails added on the back end.

The blocks with bold text and a thicker outline are core components that were found in most tools, while the other blocks were components that were sometimes added for additional functionality.

Begins with student prompt, might be additional context as well. Inputs could be filtered to avoid off-topic responses, and the sanitized input is combined with system prompts and a knowledge base and fed to the LLM endpoint, such as the OpenAI API. From there, a response was returned from the endpoint, which could be checked to ensure it addresses the students' query, and then delivered back to the student on the frontend.
-->
---
autoClicks: false
---

# Research Questions
1. **RQ1**: What approaches are currently used to build GenAI-powered postsecondary CSEd tools, and how are they motivated?
2. **RQ2**: What educational theories and framings inform the development of GenAI-powered postsecondary CSEd tools?
3. **RQ3**: What methods are used to empirically evaluate the effects of GenAI-powered postsecondary CSEd tools?

<!--
To better understand GenAI-powered postsecondary CSEd tools, we asked the following research questions:
-->
---

## Literature Review Methodology 
<p class="text-center">(Kitchenham & Charters, PRISMA)</p>

<div class="w-full flex justify-center">

```mermaid {scale: 0.72}
%%{init: {"flowchart": {"wrappingWidth": 640, "minNodeWidth": 640, "rankSpacing": 24, "padding": 10, "useMaxWidth": false, "htmlLabels": true}}}%%
flowchart TD
    A[Create Inclusion/Exclusion Criteria based on seed papers] --> B["Search ACM DL, IEEE Xplore, Springer Link, and Scopus (n=1,834)"]
    B --> C["Apply IC/EC to titles/abstracts, remove duplicates (n=117)"]
    C --> D[Develop codebook with sample of papers, calculate IRR]
    D --> E["Apply IC/EC to full papers (n=72)"]
```

</div>

<!--
To structure our literature review, we followed the practices outlined by Kitchenham and Charters as well as the PRISMA 2020 guidelines.

The full details can be found in the paper itself, but I'll summarize with two key points. The first was that we started with just over 1,800 search results from various digital libraries, and finished with 72 papers that we fully analyzed. The second is that we scoped our literature review to focus specifically on postsecondary CSEd (no K-12), tools that used modern LLMs (not older ITSes and things like that), and the tools had to be student-facing, so no autograders or instructor tools
-->
---

## Codebook Categories

<div class="card-grid">

  <div class="info-card card-blue">
    <span class="rq-label">RQ1</span>
    <h3>Problem Space</h3>
    <p>Why is the tool being built?</p>
  </div>

  <div class="info-card card-blue">
    <span class="rq-label">RQ1</span>
    <h3>Pedagogical Features</h3>
    <p>How does the tool support learning?</p>
  </div>

  <div class="info-card card-blue">
    <span class="rq-label">RQ1</span>
    <h3>Delivery Method</h3>
    <p>How do students access the tool?</p>
  </div>

  <div class="info-card card-pink">
    <span class="rq-label">RQ2</span>
    <h3>Educational Framings</h3>
    <p>What research is the tool based on?</p>
  </div>

  <div class="info-card card-green">
    <span class="rq-label">RQ3</span>
    <h3>Evaluation Goals</h3>
    <p>What do the authors want to understand about the tool?</p>
  </div>

  <div class="info-card card-green">
    <span class="rq-label">RQ3</span>
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
  height: 290px;
  margin-top: 16px;
}

.info-card {
  position: relative;
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
.rq-label {
  position: absolute;
  top: 0.4rem;
  left: 0.55rem;
  font-size: 0.9rem;
  font-weight: 700;
  letter-spacing: 0.02em;
  line-height: 1;
  opacity: 0.7;
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

<!--
We divided our codebook into 6 categories. Codes within categories were not mutually exclusive; for example, we coded for 8 different pedagogical features, and a tool could theoretically have all 8 or none of them

The top 3 addressed RQ1, educational framings addresses RQ2, and the last two address RQ3
-->

---
autoClicks: false
---

# Motivations for building tools (RQ1)

- Desire to provide personalized, context-aware support to students
- Concern that unrestricted GenAI use can lead to overreliance
- Lack of scalable help-seeking in CS classrooms

<!--
Two most commonly identified motivations were desire to provide personalized support and concern that LLMs lead to overreliance

These two themes overlap with each other, as ChatGPT and other tools can offer that personalized support, but doesn't always do so in a way that supports learning. Further, we observed instructors desiring a tool whose responses are tailored to their specific course context, based on concerns that commercial tools don't know what prior knowledge a student has and what they're learning in class

We also observed some instructors responding to high enrollment intro-sequence CS courses. There was an acknowledgement that the limited number of course staff can't provide 1 on 1 support to everyone, so providing that support in an automated way through a GenAI-powered tool was a promising alternative
-->
---
autoClicks: false
---

# Tool features and approaches (RQ1)

<div>

**Features**

</div>

- Scaffold feedback so the tool doesn’t give away answers
- Adapt feedback to students’ prior interactions
- Ground responses in curated learning material

**Delivery method**
- Majority of tools delivered via a standalone web app, others embedded in course platforms or packaged as IDE extensions

<!--
You're going to be hearing the term scaffolding a lot here, but this concept is very much present in how the tools function. 
Scaffolding presents itself in different ways: system prompts telling the LLM to structure its response to not give answers, post-response checks to make sure the output doesn't include lines of code, etc.

Adaptive feedback relates to this idea and is similar to how students interact with commercial tools: sometimes explicit (student makes specific request and LLM adjusts to it), other times implicit (tool holds on to conversation history and that informs future interactions)

Third bullet refers to the use of RAG or databases to provide richer context to the tool. One example: text transcriptions of lectures given to LLM along with instructions to reference the lectures when delivering responses. Helps the tool's responses stay relevant to the student and the course

With delivery method, most often saw tools being accessed from standalone websites just like ChatGPT or Claude, but a few of them embedded int a course forum or LMS and fewer still were integrated closely into a coding environment through IDE extension or command-line tool

81% scaff
57% adapt
25% RAG-data
63% standalone web app
-->
---
autoClicks: false
---

# Educational Framings (RQ2)

- Most frequent mentions: Scaffolding, Cognitive Load Theory, metacognition, Self-regulated learning
  - High co-occurrence between all these
- No clear trend for when or how framings were used
  - Median of 3 framings mentioned
  - Some papers did not include any coded framings, but still built on prior work
- Still need to understand connections between cited research and tool features

<!--
Potentially split this into 2 slides
Remove percentages here, but scaffolding still useful
"Disproved" is technically not true, should remove this bullet

We looked for mentions of 13 different terms pertaining to the literature in CSEd - scaffolding, self-efficacy, self-regulated learning, etc.

Four framings we observed most often, and I'm using the term "framing" because these terms weren't always qualified with citations - hard to pin down something like "scaffolding", which is very broad

We didn't identify any overarching trends about when or how these framings were used, but generally the use of them was quite diverse. We came in with a slightly cynical assumption that papers wouldn't have thorough framings

Papers with lots of buzzwords and references are more likely to be published

scaff 63%
clt 36%
meta 36%
SRL 23%
-->
---
autoClicks: false
---

# Evaluation Goals (RQ3)

- Understand student perceptions
- Understand student usage patterns
- Measure impact on learning outcomes
  - Many examples: 
    - Post-intervention test performance
    - Changes between pre- and post-test scores
    - Measurements of students' affective state (self-efficacy, nervousness, etc.)

<!--
Good number of papers had more than one goal

Sometimes depended on maturity of the tool: pilot stage (understand what students think) vs. longer-term analysis (will this help students learn CS)
-->

---
autoClicks: false
---

# Evaluation Methods (RQ3)

- Post-surveys and logging usage data both common and frequently done together (also relatively easy to perform)
- 38% of papers that included post-surveys also included pre-surveys
  - Less emphasis on measuring changes, just want to understand how students felt about the tool
- Multiple evaluation methods were common
  - 69% of papers used between 2 and 4 methods
  - Just 2 papers had no evaluations at all

<!--
Interesting to consider low-hanging fruit on part of researchers
-->
---

# Recommendations

<div class="rec-grid">

  <div class="info-card card-blue" v-click.fade-in>
    <ph-question class="rec-icon" />
    <h3>Start with the problem, not the tool</h3>
  </div>

  <div class="info-card card-green" v-click.fade-in>
    <ph-lego class="rec-icon" />
    <h3>Build on what the field already knows</h3>
  </div>

  <div class="info-card card-yellow" v-click.fade-in>
    <ph-magnifying-glass class="rec-icon" />
    <h3>Investigate the gaps</h3>
  </div>

  <div class="info-card card-purple" v-click.fade-in>
    <ph-arrows-split class="rec-icon" />
    <h3>Consider that students have alternatives</h3>
  </div>

</div>

<style>
.rec-grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 12px;
  height: 255px;
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
.rec-grid :deep(.slidev-vclick-target) {
  transition: opacity 0.45s ease !important;
}
</style>

<!--
Start with the problem, not the tool
- Resist the urge to build a solution that doesn’t address a specific problem 
- Don't integrate GenAI tools into your course without a meaningful justification 
- Apply principles from learner-centered design, HCI, & needsfinding

Build on what the field already knows
- Understand what other tools have gotten right and wrong already
- Meet the minimum standards for a quality custom tool (prompt engineering, filtering out bad responses, minimizing hallucinations, etc.)
- Make meaningful connections to prior research in CSEd, learning science, cognitive science, and other fields

Investigate the gaps
- This SLR suggests a skew toward introductory programming
- Tools with lots of scaffolding might be great for a CS1/CS2 environment, but unclear how this would fare with other students
- Expand the scope of tools to include more students and more competencies (software engineering, system design, AI-assisted programming, etc.)

Consider that students have alternatives
- "If you build it, they will come" doesn’t apply to a student with plenty of GenAI tools to choose from
- Students will always have access to commercial tools in unsupervised settings
- Make thoughtful design decisions to give students a good reason to use your tool
  - Use RAG/databases to leverage course content
  - Embed tools in existing course platforms
  - Make regular improvements in response to feedback
-->
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
  <p class="qr-email"><a href="mailto:owen.sizemore@duke.edu">owen.sizemore@duke.edu</a></p>
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
.qr-email a {
  color: inherit;
  text-decoration: underline;
}
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

# Other Trends

- Model choice reasoning remains unclear
    - Most used OpenAI models, but future tools will need to consider institutional compliance and data privacy
- Tools predominantly targeted introductory CS students
- Control groups were seldom used in evaluations

<!--
Backup slide
-->
---
