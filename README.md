# Deep Research GTM Landscape Prompt Kit

Designed for repeatable market, customer and competitive landscape research for go-to-market (GTM) engagements.

Use this as **one context block + four research modules + one optional synthesis module**, rather than a single mega-prompt. The rationale is included at the end.

original author: Bryan Wong/EDB GV

---

# Step 0 — Engagement Context

Fill this variable block once per engagement. Paste the completed block at the top of every prompt below.

## ENGAGEMENT CONTEXT

* **Client:** [company name, or anonymised descriptor such as "a Series [X] startup"]
* **What they sell:** [product/service in one sentence]
* **Business model:** [SaaS subscription / usage-based / hardware + service / marketplace take-rate / professional services / etc.]
* **Buyer & user:** [economic buyer title / end-user title]
* **Current ACV / price point:** [Average Contract Value, e.g. USD 40–120k ACV]
* **Industry / category to research:** [primary category + 1–2 adjacent categories competing for the same demand or budget]
* **Geographies in scope:** Global overview, then [Priority Region], then [Priority Market]. Secondary focus: [Market A], [Market B], [Market C]
* **Named competitors already known:** [list 5–10, or "none known"]
* **Named target accounts / current customers:** [list, or "none disclosed"]
* **Decision this research supports:** [e.g. "which two segments to prioritise for outbound over the next 12 months"]
* **Time horizon:** [e.g. next 24 months]

### Optional geography variables

Use these where jurisdiction-specific research is required:

* **Priority Region:** [e.g. Southeast Asia / Europe / North America]
* **Priority Market:** [country]
* **Secondary Markets:** [countries]
* **Relevant statistical agencies:** [national statistical agencies]
* **Relevant industry/economic agencies:** [agencies]
* **Relevant sector regulators:** [regulators]
* **Relevant corporate registries:** [registries]
* **Relevant industry associations:** [associations]

---

# Step 1 — Standing Output and Evidence Rules

Paste this block at the end of every research prompt.

## OUTPUT & EVIDENCE RULES

### Sourcing

1. Attach an inline citation to every number, market share, growth rate, customer name and forward-looking claim. Where supported by the research platform, include:

   * publisher or broker;
   * document type;
   * publication date.

2. Use the following source hierarchy, highest priority first:

   1. broker and analyst research;
   2. expert-call transcripts and buyer interviews;
   3. company filings, investor presentations and earnings-call transcripts;
   4. regulators, government agencies, statistical agencies and corporate registries;
   5. industry associations and standards bodies;
   6. reputable trade and business press.

   Use vendor marketing materials and press releases only where stronger sources are unavailable. Tag material claims based solely on these sources as **[Vendor-sourced — unverified]**.

3. Prefer sources published within the last 24 months. Flag older sources with their publication date and explain briefly why they remain relevant.

4. End the report with a **Source Appendix**:

| Source | Publisher | Type | Date | Used for |
| ------ | --------- | ---- | ---- | -------- |

### Evidence discipline

5. If a data point is unavailable, write:

   **Not disclosed in available sources.**

   Do not silently estimate or fill gaps from general knowledge.

6. Where an estimate is necessary, label it **[Estimate]** and show the inputs, method and key assumptions immediately below it.

7. Label substantive analytical conclusions as:

   * **[Sourced]** where directly supported by evidence; or
   * **[Inference]** where derived from multiple facts or analytical judgement.

8. Where credible sources conflict, present the range and explain the likely reason for the difference, such as:

   * market definition;
   * geography;
   * currency;
   * customer scope;
   * forecast base year;
   * methodology.

   Do not average conflicting estimates into an artificial single figure.

9. Give each major section a confidence rating of **High / Medium / Low**, with a one-line explanation.

### Formatting

10. Use tables for comparisons. Keep column definitions consistent across related tables so outputs can be combined later.

11. Report monetary values in **USD** unless otherwise specified. Where the original source uses another currency, state:

* original currency;
* conversion date or period;
* FX assumption.

12. Where a chart would materially improve the analysis:

* specify the chart type and proposed title;
* provide the complete underlying data table;
* where a usable source exhibit already exists, cite the report and page/exhibit number.

13. Avoid general background unless it changes the GTM decision. Assume the reader understands basic business and market concepts.

Start each major section with a **2–3 sentence "So what"**, followed by the supporting evidence.

### Research gaps

14. Finish with **Top 10 Evidence Gaps**.

Rank the unanswered questions by their potential impact on the GTM decision.

For each gap, specify the most appropriate way to close it:

| Rank | Evidence gap | Why it matters | Best way to close |
| ---- | ------------ | -------------- | ----------------- |

Potential methods include:

* expert call;
* customer interview;
* channel check;
* primary survey;
* paid syndicated research;
* regulatory clarification;
* corporate registry research.

---

# Prompt 1 — Industry Landscape, Market Sizing and Ecosystem

**Target length:** 12–18 pages.

[PASTE ENGAGEMENT CONTEXT]

Act as a market intelligence analyst producing the industry baseline for a go-to-market strategy engagement.

Produce a structured report covering the following.

## 1. CATEGORY DEFINITION

Define the market as a practitioner would rather than simply adopting one research firm's definition.

State explicitly:

* what is in scope;
* what is out of scope;
* alternative names used for the category;
* adjacent categories competing for the same customer need or budget;
* where analysts draw category boundaries differently.

Identify any boundary disagreement that materially changes the estimated market size.

## 2. INDUSTRY OVERVIEW — GLOBAL

Assess:

* value-chain structure;
* how money flows through the value chain;
* underlying demand drivers;
* typical commercial and unit-economic models;
* regulatory and standards environment;
* three to five structural forces most likely to reshape the industry over the next 24 months.

Focus on factors that affect customer acquisition, pricing, distribution, product requirements or competitive advantage.

## 3. INDUSTRY OVERVIEW — PRIORITY REGION AND PRIORITY MARKET

Treat **[Priority Region]** and **[Priority Market]** as separate sections.

### Priority Region

Identify:

* markets growing fastest and why;
* major demand centres;
* where procurement and technology decisions are made;
* where regional headquarters are located;
* where budgets are actually controlled;
* major differences between markets in regulation, procurement and distribution.

Do not assume that regional headquarters location and budget ownership are the same.

### Priority Market

Assess:

* market maturity;
* relevant regulation;
* government programmes;
* public-sector or state-linked demand where material;
* private-sector demand;
* major local buyers;
* local channel structure;
* whether the market primarily functions as a standalone demand pool, regional hub, reference market, or combination of these.

Be explicit where market-specific evidence is thin.

## 4. MARKET SIZING

Provide three separate views.

### A. TAM — Total Addressable Market

Estimate TAM for:

* Global;
* [Priority Region];
* [Priority Market].

Show available analyst estimates side by side:

| Source | Market definition | Geography | Base year | Base value | CAGR | Forecast year | Forecast value |
| ------ | ----------------- | --------- | --------: | ---------: | ---: | ------------: | -------------: |

Do not collapse materially different market definitions into one number.

### B. SAM — Serviceable Addressable Market

Estimate the subset addressable by a company with the client's:

* product;
* business model;
* price point;
* buyer;
* deployment requirements;
* geographic reach.

Show explicitly how each filter reduces TAM to SAM.

### C. Bottom-Up SOM — Serviceable Obtainable Market

Build a bottom-up view using addressable account counts.

For **[Priority Market]** and the two largest relevant markets in **[Priority Region]**:

1. identify qualifying organisations by target segment;
2. establish the number of accounts using registries, statistical agencies or industry bodies;
3. apply a realistic ACV;
4. show the resulting revenue pool.

Use:

**Addressable accounts × realistic ACV = indicative revenue pool**

Cite the source of every account count.

Where top-down and bottom-up estimates differ by more than **2x**, diagnose the likely reason.

## 5. ECOSYSTEM MAP

Map the relevant ecosystem across:

* incumbent vendors;
* challengers;
* systems integrators;
* implementation partners;
* distributors and resellers;
* technology providers;
* data providers;
* industry bodies;
* standards organisations;
* regulators;
* relevant investors;
* major platforms or infrastructure providers that influence distribution.

Use:

| Organisation | Role | Geography | Why it matters | Partner / Gatekeeper / Competitor | Evidence |
| ------------ | ---- | --------- | -------------- | --------------------------------- | -------- |

Identify the **two or three relationships most likely to determine a new entrant's ability to reach buyers** in [Priority Market] and [Priority Region].

[PASTE OUTPUT & EVIDENCE RULES]

---

# Prompt 2 — Customer Segmentation and Buying Behaviour

[PASTE ENGAGEMENT CONTEXT]

Continue the GTM research on **[category]**.

Build a customer segmentation for the client's core business grounded in observed buying behaviour rather than conventional industry segmentation.

Prioritise expert-call transcripts, customer commentary and buyer-side evidence over vendor-published segmentation.

## 1. SEGMENTATION

Test at least the following segmentation dimensions:

* organisation size by revenue;
* organisation size by headcount;
* sub-industry or nature of business;
* operating-model complexity;
* regulatory exposure;
* existing technology estate;
* incumbent vendor;
* procurement maturity;
* geography.

Determine which dimensions appear most predictive of:

* willingness to pay;
* purchase urgency;
* sales-cycle duration;
* probability of switching;
* implementation complexity.

Identify commonly used segmentation variables that appear weakly predictive.

## 2. SEGMENT PROFILES

Develop approximately **4–6 segments**.

Use the same profile for each:

| Attribute                        | Segment |
| -------------------------------- | ------- |
| Account count — Priority Market  |         |
| Account count — Priority Region  |         |
| Account count — Global           |         |
| Core job to be done              |         |
| Current alternatives/workarounds |         |
| Economic buyer                   |         |
| Primary user                     |         |
| Typical budget range             |         |
| Budget line                      |         |
| Buying committee                 |         |
| Typical sales cycle              |         |
| Procurement requirements         |         |
| Security/compliance requirements |         |
| Switching costs                  |         |
| Existing lock-ins                |         |
| Purchase trigger events          |         |

Where a field cannot be evidenced, mark it **Not disclosed in available sources**.

## 3. SEGMENT ATTRACTIVENESS

Score each segment on:

* size;
* growth;
* pain intensity;
* ability to pay;
* ease of reach;
* sales-cycle length;
* competitive intensity;
* fit with the client's current product;
* fit with the client's current business model.

State the scoring rubric before applying it.

Present all segments in one comparison table.

Rank the segments and identify the **top two potential beachhead segments** for:

* [Priority Market];
* [Priority Region].

For each recommendation, state:

1. why it ranks highly;
2. the evidence supporting the ranking;
3. the single assumption that would most change the result if wrong.

## 4. REGIONAL DIFFERENCES

Identify where buying behaviour in [Priority Market] and [Priority Region] differs materially from global norms.

Assess:

* procurement practices;
* localisation requirements;
* data-residency requirements;
* price sensitivity;
* preference for local versus global vendors;
* direct versus channel-led purchasing;
* public-sector procurement where relevant;
* security and compliance expectations;
* expected proof-of-value requirements.

[PASTE OUTPUT & EVIDENCE RULES]

---

# Prompt 3 — Competitive Benchmarking

[PASTE ENGAGEMENT CONTEXT]

Continue the GTM research on **[category]**.

Produce a competitive benchmark focused on factors that materially influence buyer choice.

## 1. COMPETITIVE SET

Identify **10–15 relevant competitors or alternatives**, grouped into:

* global incumbents;
* global challengers;
* regional or local players;
* adjacent-category entrants;
* in-house alternatives;
* manual alternatives;
* "do nothing" option.

Start with the named competitors in the engagement context, but do not limit the research to them.

For every additional player, explain briefly why it belongs in the competitive set.

Where evidence permits, estimate the prevalence of the **build internally / manual / do nothing** alternatives.

## 2. BENCHMARK TABLE

Use one row per competitor and identical columns throughout:

| Field                | Required information                              |
| -------------------- | ------------------------------------------------- |
| Company              | Name                                              |
| HQ                   | Headquarters                                      |
| Founded              | Year                                              |
| Ownership            | Public / PE / VC-backed / bootstrapped / other    |
| Latest funding       | Round, amount, date, lead investor                |
| Latest valuation     | Disclosed valuation and date                      |
| Revenue / ARR        | Latest disclosed figure, source and date          |
| Revenue growth       | Latest disclosed growth                           |
| Headcount            | Latest figure and trend                           |
| Target segment       | Primary customer segment                          |
| Pricing              | Model and disclosed price points                  |
| Geographic presence  | Global / Priority Region / Priority Market        |
| Local presence       | Entity / team / partner-only / none identified    |
| Market share         | Estimate and basis                                |
| Stated UVP           | Company's own positioning                         |
| Buyer-validated UVP  | Supported or contradicted by buyer-side evidence  |
| Lighthouse customers | Named customers with evidence                     |
| Partnerships         | Major channel/platform/technology relationships   |
| Recent moves         | M&A, launches, pricing changes, market entry/exit |
| Weaknesses           | Customer- or analyst-cited weaknesses             |

For private companies, expect information gaps.

Mark missing data **Not disclosed** rather than estimating it.

Market share may be estimated only where there is a defensible methodology. Label it **[Estimate]** and show the method.

## 3. POSITIONING ANALYSIS

### A. Positioning map

Identify the **two dimensions that most strongly differentiate buyer decisions** in this category.

Derive the axes from evidence rather than selecting generic variables such as "price vs quality".

Explain why the axes matter.

### B. Head-to-head dynamics

Where credible evidence exists, identify:

* who competes directly with whom;
* typical win/loss patterns;
* reasons buyers choose one over another.

Do not infer win/loss claims from vendor marketing alone.

### C. White space

Identify potentially under-served:

* customer segments;
* geographies;
* use cases;
* deployment models;
* price points.

For each white-space hypothesis, show evidence that unmet demand exists.

### D. Competitive risk

Identify the competitor or alternative most likely to threaten the client's position in [Priority Market] and [Priority Region] over the next 24 months.

Specify the early-warning signals that would indicate the threat is increasing.

## 4. CHART SPECIFICATIONS

Provide complete underlying data tables and specifications for:

1. competitive positioning map;
2. funding and valuation comparison;
3. geographic coverage matrix;
4. revenue growth comparison for players with disclosed data.

Do not manufacture values solely to make charts complete.

[PASTE OUTPUT & EVIDENCE RULES]

---

# Prompt 4 — Emerging Trends and Forward View

[PASTE ENGAGEMENT CONTEXT]

Continue the GTM research on **[category]**.

Produce a forward-looking analysis covering the next **24 months**.

Use the same structure for every trend:

| Field              | Requirement                |
| ------------------ | -------------------------- |
| What is changing   | Description                |
| Evidence           | Sourced evidence           |
| Beneficiaries      | Who gains                  |
| Exposed players    | Who loses or faces risk    |
| Leading indicators | Signals to monitor         |
| GTM implication    | Implication for the client |
| Likelihood         | High / Medium / Low        |
| Client impact      | High / Medium / Low        |

Cover five categories separately.

## 1. MARKET

Assess:

* demand shifts;
* spending patterns;
* budget reallocation;
* consolidation;
* emerging demand pools;
* macroeconomic effects;
* policy effects;
* [Priority Region] and [Priority Market] developments.

## 2. COMPETITIVE

Assess:

* business-model shifts;
* pricing changes;
* packaging changes;
* M&A and consolidation;
* new entrants;
* large-platform entry;
* changes in sales and distribution models.

## 3. TECHNOLOGY

Assess:

* capability shifts affecting product requirements;
* capabilities becoming commoditised;
* standards;
* interoperability;
* infrastructure dependencies;
* technology capable of weakening or eliminating the client's current differentiation.

Separate genuine technology adoption from announcements and demonstrations.

## 4. CUSTOMER

Assess changes in:

* buying behaviour;
* buying-committee composition;
* procurement;
* compliance;
* security requirements;
* proof-of-value expectations;
* vendor discovery;
* vendor evaluation;
* purchasing authority.

## 5. ECOSYSTEM

Assess:

* channel economics;
* partner economics;
* platform dynamics;
* marketplace dynamics;
* regulatory changes affecting intermediaries;
* new gatekeepers or distribution channels.

## SCENARIOS

Develop three scenarios for the next 24 months:

| Scenario | Description | Trigger conditions | GTM implications |
| -------- | ----------- | ------------------ | ---------------- |
| Base     |             |                    |                  |
| Bull     |             |                    |                  |
| Bear     |             |                    |                  |

For each scenario, identify what the client would need to change in its GTM approach.

Do not present the scenarios as forecasts. They are decision frameworks.

## MONTHLY MONITORING

Identify the **five indicators a GTM team should monitor monthly**.

For each:

| Indicator | Why it matters | Signal/source | Threshold or change to watch |
| --------- | -------------- | ------------- | ---------------------------- |

Use specific observable signals rather than generic instructions such as "monitor competitors".

[PASTE OUTPUT & EVIDENCE RULES]

---

# Optional Prompt 5 — GTM Implications Synthesis

Run this after Prompts 1–4.

This module relies more heavily on synthesis and judgement than retrieval. Treat its output as a decision-support draft rather than an evidence source.

[PASTE ENGAGEMENT CONTEXT]

Using the evidence established in this research thread, produce a **3–5 page GTM implications memo** for the client.

Do not repeat the preceding research. Convert it into choices.

## 1. POSITIONING

Identify the **two or three most defensible positioning options** available.

For each:

* target buyer;
* customer problem;
* differentiation;
* evidence supporting it;
* competitive alternative displaced;
* what must be true about the client's product for the position to hold;
* principal weakness.

## 2. BEACHHEAD AND GEOGRAPHY SEQUENCE

Recommend a segment and geography sequence for the next 24 months.

For each proposed market/segment:

* why now;
* evidence;
* entry logic;
* sequencing dependency;
* disqualifying condition.

Explicitly distinguish between:

* markets attractive for revenue;
* markets attractive for reference customers;
* markets attractive as regional operating hubs;
* markets attractive for partnerships or ecosystem access.

Do not treat these as equivalent.

## 3. CHANNEL STRATEGY

Recommend:

* direct;
* partner-led;
* hybrid;

based on the ecosystem and buying behaviour identified.

Specify:

* what the client should own directly;
* what partners can accelerate;
* where partners introduce margin loss or customer-access risk;
* which gatekeeper relationships matter most.

## 4. PRICING AND PACKAGING

Draw implications from:

* competitor pricing;
* customer ability to pay;
* procurement behaviour;
* current ACV;
* switching costs;
* implementation requirements.

Distinguish evidence-backed observations from recommendations.

## 5. CRITICAL ASSUMPTIONS

Identify the **five assumptions on which the GTM recommendation depends most heavily**.

Rank them by the damage caused if the assumption is wrong.

| Rank | Assumption | Evidence today | Consequence if wrong | Cheapest 30-day test |
| ---- | ---------- | -------------- | -------------------- | -------------------- |

Prioritise tests that can be completed through:

* customer interviews;
* outbound experiments;
* pricing tests;
* channel conversations;
* expert calls;
* procurement discussions;
* product telemetry;
* targeted desk research.

## FINAL DECISION SUMMARY

End with:

**Recommended beachhead:** [segment + geography]

**Primary positioning:** [one sentence]

**Route to market:** [direct / partner / hybrid]

**Indicative ACV:** [range, or evidence gap]

**Three things to validate before scaling:**

1. [...]
2. [...]
3. [...]

Separate clearly:

* **Evidence-backed findings**
* **Analytical inference**
* **Recommendation**

---

# Notes on Using This Kit

## Why use multiple prompts instead of one mega-prompt?

Deep-research systems typically build an iterative retrieval plan from the initial prompt.

Combining market sizing, segmentation, competition, customer behaviour, ecosystem analysis and forward trends into one request can spread the available research effort too thinly. Competitive benchmarking and customer segmentation are particularly retrieval-intensive because individual claims often require separate evidence.

A modular workflow also allows strong industry-level research to be reused across multiple company or GTM assessments without repeating the entire research process.

Recommended sequence:

**Industry baseline → Customer segmentation → Competition → Forward view → GTM synthesis**

## Configure source filters before running

Where the research platform allows source filters for:

* document type;
* publication date;
* geography;
* company;
* industry;

configure these directly in the interface.

Prompt-level sourcing instructions are useful but may not be applied consistently by every research platform.

## Expected evidence gaps

Coverage is often strongest for:

* public companies;
* broker and analyst research;
* regulatory filings;
* earnings transcripts;
* expert calls;
* larger markets.

Expect weaker coverage for:

* private-company revenue;
* private-company valuation;
* startup market share;
* small regional competitors;
* narrow country-level market sizing;
* customer-level pricing;
* actual win/loss data.

Do not hide these gaps with unsupported estimates.

The purpose of the evidence rules is to make uncertainty visible.

## Charts

Research systems are generally more reliable at producing **structured data and chart specifications** than presentation-ready graphics.

For each required visual:

1. obtain the underlying data;
2. retain the citations;
3. identify existing source exhibits where available;
4. build the final chart separately in the preferred presentation or spreadsheet tool.

Do not create artificial datapoints simply to complete a visual.

## Verify before external attribution

Treat generated research as a research accelerator rather than a final authority.

Before using a claim externally, spot-check:

* important market-size figures;
* customer names;
* competitor revenue;
* funding and valuation;
* regulatory claims;
* market-share estimates;
* forward-looking claims.

Verify them against the cited source document wherever possible.

## Repository customisation

For reuse across projects, maintain the generic version in the repository and populate only the variable block for each engagement.

Avoid committing:

* client names where confidentiality applies;
* customer lists;
* internal account information;
* non-public pricing;
* proprietary market estimates;
* interview notes;
* credentials or access details;
* confidential source documents.

Where examples are useful, use synthetic company names, generic market descriptors and illustrative figures clearly marked as examples.
