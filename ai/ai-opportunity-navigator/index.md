---
layout: ai-case-study
title: AI Opportunity Navigator
subtitle: Enterprise AI opportunity assessment, governance, and portfolio decisioning
card_subtitle: Enterprise AI Portfolio & Governance
description: An independent applied AI project connecting structured assessment, transparent portfolio rules, governance, and human decision authority.
summary: A working platform for assessing, governing, prioritizing, and managing AI opportunities from business intake through lifecycle execution.
permalink: /ai/ai-opportunity-navigator/
ai_case_study: true
featured: true
display_order: 1
thumbnail: /assets/images/ai/ai-opportunity-navigator/portfolio-card.webp
thumbnail_alt: AI Opportunity Portfolio with summary metrics, filters, and the operating portfolio table
hero_image:
  src: /assets/images/ai/ai-opportunity-navigator/opportunity-portfolio.webp
  alt: AI Opportunity Portfolio showing 15 opportunities, assessment and governance metrics, and separate application recommendations and human decisions
  width: 2344
  height: 2805
  caption: The operating portfolio brings assessment, governance, human decisions, and next actions into one view.
methodology_image:
  src: /assets/images/ai/ai-opportunity-navigator/product-methodology.webp
  alt: Product Methodology showing the operating framework and separate boundaries for opportunity scoring, governance, and human authority
  width: 2344
  height: 1880
  caption: The product methodology makes the boundaries between model input, deterministic rules, and human authority explicit.
operating_record_image:
  src: /assets/images/ai/ai-opportunity-navigator/policy-operating-record.webp
  alt: Customer Support Policy Knowledge Assistant operating record showing score 79, Moderate governance, Validate Further recommendation, Approve Pilot human decision, and lifecycle and decision histories
  width: 2416
  height: 5006
  caption: The application recommends Validate Further while the recorded human decision is Approve Pilot. Ownership, next actions, and lifecycle history make that decision operational.
assessment_image:
  src: /assets/images/ai/ai-opportunity-navigator/policy-assessment.webp
  alt: Customer support policy assessment recommending RAG and a knowledge assistant, with an opportunity score of 79 and a Validate Further recommendation
  width: 2344
  height: 1810
  caption: The assessment recommends retrieval grounded in approved policy information, with permission-aware access and representative review.
executive_image:
  src: /assets/images/ai/ai-opportunity-navigator/portfolio-intelligence.webp
  alt: Portfolio Intelligence dashboard separating lifecycle stage, governance, application recommendation, score bands, and human portfolio decisions
  width: 2344
  height: 2825
  caption: Executive reporting keeps portfolio value, governance constraints, and human decisions visible as distinct dimensions.
project_role: Product strategy, operating-model design, governance framework, decision architecture, solution design, implementation, testing, and deployment
technology: Next.js · TypeScript · Supabase/PostgreSQL · OpenAI Structured Outputs · Vercel
project_status: Production deployment
demonstrates:
  - AI opportunity evaluation
  - Solution-pattern selection
  - Deterministic scoring
  - AI governance
  - Human decision authority
  - Portfolio operating models
  - Executive reporting
---
<nav class="case-contents" aria-label="Case study contents">
  <p class="eyebrow">In this case study</p>
  <ol>
    <li><a href="#overview">Overview</a></li>
    <li><a href="#business-problem">Business Problem</a></li>
    <li><a href="#operating-model">Operating Model</a></li>
    <li><a href="#decision-architecture">Decision Architecture</a></li>
    <li><a href="#solution-selection">Solution Selection</a></li>
    <li><a href="#rag">RAG</a></li>
    <li><a href="#portfolio-management">Portfolio Management</a></li>
    <li><a href="#production">Production</a></li>
    <li><a href="#technology">Technology</a></li>
    <li><a href="#demonstrates">What It Demonstrates</a></li>
  </ol>
</nav>

<section class="case-section" aria-labelledby="overview">
  <p class="eyebrow section-number">01 / Overview</p>
  <h2 id="overview" tabindex="-1">Overview</h2>
  <p>AI initiatives often enter organizations as loosely defined ideas: an executive request, a promising use case, or a proposed technology solution. What is frequently missing is a consistent way to determine whether the opportunity is valuable, whether AI is actually the right solution, what risks it introduces, and whether it should advance.</p>
  <p>I designed and built AI Opportunity Navigator as an independent portfolio project to explore that problem.</p>
  <p>The result is a working enterprise operating model and production application for moving AI opportunities from initial business intake through assessment, governance, portfolio decisioning, and lifecycle execution.</p>
  <blockquote class="principle"><p>AI provides structured judgment. Application logic applies transparent portfolio rules. Humans retain decision authority.</p></blockquote>
</section>

<section class="case-section" aria-labelledby="business-problem">
  <p class="eyebrow section-number">02 / The Business Problem</p>
  <h2 id="business-problem" tabindex="-1">The Business Problem</h2>
  <p>Organizations increasingly have more potential AI use cases than they can responsibly pursue.</p>
  <p>The challenge is not simply identifying ideas. Leadership needs to answer a more difficult set of questions:</p>
  <p>Which opportunities create meaningful business value? Is AI actually appropriate for the problem? Is the data and technology environment ready? What organizational change would be required? What governance concerns could constrain advancement? And who should ultimately decide whether an opportunity proceeds?</p>
  <p>I wanted to design a system that addressed those questions without treating the AI model itself as the decision-maker.</p>
</section>

<section class="case-section" aria-labelledby="operating-model">
  <p class="eyebrow section-number">03 / Operating Model</p>
  <h2 id="operating-model" tabindex="-1">From AI assessment to enterprise operating model</h2>
  <p>Business users first provide structured evidence about the opportunity, including the problem, desired outcomes, current process, data environment, technology constraints, organizational readiness, and risk.</p>
  <ol class="authority-chain" aria-label="Decision authority chain">
    <li><span>01</span>Business Intake</li>
    <li><span>02</span>AI Assessment</li>
    <li><span>03</span>Human Effective Inputs</li>
    <li><span>04</span>Deterministic Calculation</li>
    <li><span>05</span>Application Recommendation</li>
    <li><span>06</span>Human Portfolio Decision</li>
    <li><span>07</span>Lifecycle Execution</li>
  </ol>
  <p>AI then provides a structured assessment of that evidence. The application—not the model—applies deterministic scoring and governance rules.</p>
  <p>Human reviewers can challenge model inputs, provide rationale, make portfolio decisions, and explicitly move opportunities through the lifecycle.</p>
  <p>This separation makes it possible to understand not only the final result, but also how and why the result was reached.</p>
  {% if page.methodology_image %}{% include ai-screenshot.html image=page.methodology_image %}{% endif %}
</section>

<section class="case-section" aria-labelledby="decision-architecture">
  <p class="eyebrow section-number">04 / Decision Architecture</p>
  <h2 id="decision-architecture" tabindex="-1">Decision Architecture</h2>
  <h3>Opportunity value is not governance</h3>
  <p>The application calculates an opportunity score across six weighted dimensions:</p>
  <ul class="dimension-list">
    <li>Business Value</li><li>Strategic Alignment</li><li>AI Suitability</li>
    <li>Technical Feasibility</li><li>Data Readiness</li><li>Operating &amp; Adoption Readiness</li>
  </ul>
  <p>Governance is evaluated independently across ten risk areas. A high-value opportunity should not be able to mathematically offset a serious governance concern. A strong opportunity can therefore still require additional governance review—or be prevented from advancing in its current form.</p>
  <h3>AI recommendation is not human decision</h3>
  <p>The application recommendation and the human portfolio decision are deliberately separate. The system might recommend <strong>Validate Further</strong> while an authorized reviewer chooses to <strong>Approve Pilot</strong>, provided that decision is recorded explicitly.</p>
  <p>Leadership can also decide not to advance an opportunity even when the application considers it promising.</p>
  <h3>Original AI output remains intact</h3>
  <p>Human reviewers can override assessment inputs with documented rationale, but the original AI-generated assessment remains immutable. The system creates a new deterministic calculation revision rather than rewriting the original model output.</p>
  <aside class="audit-chain" aria-label="Audit trail">
    <p class="eyebrow">An inspectable decision trail</p>
    <p>What the AI assessed → what a human changed → what the rules calculated → what leadership decided</p>
  </aside>
  {% if page.operating_record_image %}{% include ai-screenshot.html image=page.operating_record_image %}{% endif %}
</section>

<section class="case-section" aria-labelledby="solution-selection">
  <p class="eyebrow section-number">05 / Solution Selection</p>
  <h2 id="solution-selection" tabindex="-1">AI should not always be the answer</h2>
  <p>Another deliberate design choice was to avoid assuming that every opportunity should become a generative-AI solution.</p>
  <p>The assessment considers multiple solution patterns, including:</p>
  <ul class="solution-patterns">
    <li>Process redesign</li><li>Traditional automation</li><li>Analytics / BI</li><li>Predictive ML</li>
    <li>AI extraction and classification</li><li>Generative AI transformation</li><li>Generative AI generation</li>
    <li>RAG knowledge assistants</li><li>AI copilots</li><li>Agentic workflows</li>
  </ul>
  <blockquote class="principle"><p>The simplest viable solution should win.</p></blockquote>
  <p>The system can conclude that an opportunity is better solved through conventional automation or process redesign.</p>
  <p>In one test case, additional business evidence increased the system's confidence that traditional automation, rather than AI, was the appropriate solution. That behavior was intentional.</p>
</section>

<section class="case-section" aria-labelledby="rag">
  <p class="eyebrow section-number">06 / Applying RAG Appropriately</p>
  <h2 id="rag" tabindex="-1">Applying RAG Appropriately</h2>
  <p>For the Customer Support Policy Knowledge Assistant opportunity, the platform identified RAG—Retrieval-Augmented Generation—as the appropriate solution pattern because the problem involved helping employees answer questions from an authoritative and changing body of policy information.</p>
  <p>The objective was not unrestricted generation. The more appropriate architecture would retrieve relevant approved information and use that evidence to ground model responses.</p>
  <p>That choice brings enterprise design requirements into focus:</p>
  <ul class="enterprise-considerations">
    <li><strong>Source authority:</strong> establish which policies are approved and who owns them.</li>
    <li><strong>Information freshness:</strong> keep retrieval aligned with current policy and retire superseded material.</li>
    <li><strong>Access control:</strong> retrieve only information the requesting employee is authorized to access.</li>
    <li><strong>Retrieval quality:</strong> evaluate whether the system finds the evidence needed to answer the question.</li>
    <li><strong>Provenance:</strong> make the source of an answer visible and traceable.</li>
    <li><strong>Answer faithfulness:</strong> check that responses accurately reflect the retrieved evidence.</li>
    <li><strong>Appropriate abstention:</strong> decline to answer when sufficient evidence cannot be found.</li>
  </ul>
  <p><strong>AI Opportunity Navigator itself is not implemented as a RAG application.</strong> RAG is one of the solution architectures the assessment framework can recommend when the characteristics of the business problem justify it.</p>
  <blockquote class="principle"><p>The goal is technology selection, not technology advocacy.</p></blockquote>
  {% if page.assessment_image %}{% include ai-screenshot.html image=page.assessment_image %}{% endif %}
</section>

<section class="case-section" aria-labelledby="portfolio-management">
  <p class="eyebrow section-number">07 / Portfolio Management</p>
  <h2 id="portfolio-management" tabindex="-1">From individual opportunity to portfolio management</h2>
  <p>The product expanded beyond individual assessment because enterprise transformation does not stop when a use case receives a score. An assessment needs to connect to accountable ownership, decisions, and the work that follows.</p>
  <p>Each opportunity can have:</p>
  <ul class="dimension-list">
    <li>Lifecycle stage</li><li>Portfolio owner</li><li>Next action</li><li>Next-action owner</li>
    <li>Due date</li><li>Human portfolio decisions</li><li>Assessment/calculation history</li><li>Lifecycle history</li>
  </ul>
  <p>The operating portfolio adds filters and work queues so reviewers can find opportunities that need attention and connect each assessment to its next action. Portfolio Intelligence provides an executive view across the opportunity set, supporting prioritization and oversight.</p>
  <div class="portfolio-shift">
    <p><span>Individual assessment</span>“Is this one opportunity good?”</p>
    <p><span>Portfolio management</span>“What does our overall AI opportunity portfolio look like?”</p>
  </div>
  {% if page.executive_image %}{% include ai-screenshot.html image=page.executive_image %}{% endif %}
</section>

<section class="case-section" aria-labelledby="production">
  <p class="eyebrow section-number">08 / Production</p>
  <h2 id="production" tabindex="-1">Security and production readiness</h2>
  <p>Supabase Row Level Security separates user-owned data while keeping synthetic demonstration data visible. Authenticated server-side access, cross-user isolation, and guarded database operations establish the application’s data-access boundaries.</p>
  <p>Production-safe error handling, security headers, and regression coverage around session handling support reliable operation. Production testing uncovered an intermittent SSR authentication/JWT propagation race; the final implementation stabilized authentication at the middleware boundary before protected portfolio queries execute.</p>
</section>

<section class="case-section" aria-labelledby="technology">
  <p class="eyebrow section-number">09 / Technology</p>
  <h2 id="technology" tabindex="-1">Technology as an enabler</h2>
  <p>The platform uses Next.js and TypeScript, Supabase and PostgreSQL, OpenAI Structured Outputs, and Vercel. These choices support the operating model: the model supplies structured assessment input, while the application owns scoring rules, governance rules, application recommendations, human overrides, and lifecycle authority.</p>
  <blockquote class="principle"><p>Use AI where judgment is useful, deterministic logic where consistency is required, and humans where organizational authority belongs.</p></blockquote>
</section>

<section class="case-section" aria-labelledby="demonstrates">
  <p class="eyebrow section-number">10 / What This Project Demonstrates</p>
  <h2 id="demonstrates" tabindex="-1">What This Project Demonstrates</h2>
  <p>AI Opportunity Navigator demonstrates my work at the intersection of technology enablement, digital transformation, strategy, governance, and execution. Its emphasis is on integrating business and technology decisions into a practical operating model, rather than positioning me primarily as an AI or software engineer.</p>
  <p>The project required turning an ambiguous emerging-technology problem into a practical operating system:</p>
  <ul>
    <li>Define the business problem.</li><li>Establish decision rights.</li><li>Create governance boundaries.</li>
    <li>Develop transparent portfolio rules.</li><li>Design the user experience.</li><li>Make technology choices.</li>
    <li>Carry the concept through implementation.</li>
  </ul>
  <p class="closing-statement">Turn complex business and technology problems into practical solutions that improve how organizations operate.</p>
</section>
