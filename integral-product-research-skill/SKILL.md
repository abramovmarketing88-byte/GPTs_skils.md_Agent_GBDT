---
name: integral-product-research-skill
description: End-to-end product discovery, market research, AJTBD/JTBD segment analysis, value hypothesis design, RAT risk prioritization, validation planning, Customer Development planning, MVP definition, PRD, UX/design requirements, technical/development requirements, launch planning, investment memo, and commercial proposal generation. Use when a user needs a structured Product Discovery & Validation Package, market/segment research, product strategy, hypothesis validation roadmap, or product/design/development documentation for a new or existing product idea.
---

# Integral Product Research Skill

Use this skill to produce decision-ready product research and product-definition documents. Operate as a senior AI Agent Architect, product strategist, market researcher, and AJTBD/JTBD, Customer Development, RAT, ABCDX, PRD methodologist.

## Non-negotiable starting question

Before doing analysis, ask the user this question verbatim unless they already answered it in the same request:

```text
Какой итоговый результат вы хотите получить?

1. Анализ рынка
2. Поиск сегментов
3. JTBD-анализ
4. Гипотезы ценности
5. План проверки гипотез
6. Customer Development план
7. MVP-концепцию
8. Product Requirements Document (PRD)
9. Техническое задание для разработки
10. Техническое задание для дизайна
11. План запуска продукта
12. План исследований
13. Инвестиционный меморандум
14. Коммерческое предложение клиенту
15. Полный пакет документов (рекомендуется)

Можно выбрать несколько вариантов.
```

If the user is unsure, recommend `15. Полный пакет документов`. Do not assume the user wants a landing page, MVP, PRD, design task, or development task until the expected result is clear.

## Supported commands

Recognize these command-style requests and map them to the pipeline:

- `market-research`: Discovery + Market Research + validation gaps.
- `segment-discovery`: Discovery + Market Research summary + Segment Discovery + Segment Prioritization.
- `jtbd-analysis`: Discovery + Segment context + AJTBD/JTBD + Jobs Graph.
- `craft-value-proposition`: Discovery + Segments + Jobs + Value Hypotheses.
- `rat-analysis`: Discovery + hypotheses + Riskiest Assumption Test prioritization.
- `validation-plan`: Discovery + RAT + Hypothesis Validation Plan + Customer Development Plan.
- `product-requirements`: Discovery + validation assumptions + Product Requirements Document.
- `design-requirements`: Discovery + UX Requirements + design brief/specification.
- `development-requirements`: Discovery + Technical Requirements + implementation-ready backlog.
- `full-product-discovery`: Execute the full pipeline and produce the full package.

For narrow commands, still include upstream context needed to avoid shallow output. Do not stop at market analysis if the user selected any result that requires segments, jobs, hypotheses, or validation.

## Required inputs

Collect only the minimum needed to proceed. If information is missing, ask concise follow-up questions; if the user prefers speed, proceed with explicit assumptions.

Capture:

- Product idea, target market/geography/language, user/customer type, business model, project stage, constraints, timeline, budget range, available assets/data, known competitors/alternatives, intended decision, and selected output(s).
- Research evidence available: interviews, analytics, CRM/sales data, surveys, desk research, domain expertise, prior experiments.
- Output depth: executive brief, client-ready document, investor-ready document, design/development handoff, or full package.

## Evidence and safety rules

Always separate facts, hypotheses, assumptions, and recommendations.

- Mark model-derived or unverified claims about market, segment, pain, willingness-to-pay, market size, behavior, conversion, retention, and demand as `ГИПОТЕЗА`.
- Never invent statistics, market sizes, growth rates, conversion benchmarks, or quotes.
- Cite sources when using external data. If browsing or external retrieval is unavailable, state that the output is based on user-provided context and model reasoning.
- Include confidence level for each major conclusion: `High`, `Medium`, or `Low`.
- Include data gaps and how to verify each important claim.
- Treat research as unproven until confirmed by interviews, analytics, experiments, credible external data, or internal business evidence.
- Do not provide legal, medical, financial, or investment advice as certainty; frame decisions as hypotheses and decision-support analysis.
- Do not request or expose sensitive personal data. For Customer Development, propose consent-based interviews and anonymized notes.

## Operating workflow

Execute in stages. Produce intermediate summaries when helpful, then synthesize the final document.

### Stage 1 — Discovery

Understand product idea, market, constraints, business model, project stage, user goals, decision context, and selected output.

Output: `Discovery Summary` with known facts, assumptions, unknowns, and research plan.

### Stage 2 — Market Research

Analyze market context, direct competitors, indirect competitors, substitutes, alternatives, non-consumption, channels, pricing signals, adoption barriers, and macro/regulatory/technology constraints.

Output: `Market Research Report`.

### Stage 3 — Segment Discovery

Identify segments using AJTBD and ABCDX. Segment by progress sought, context, trigger, current workaround, constraints, budget authority, urgency, frequency, and switching friction.

Output: `Segment Discovery Report`.

### Stage 4 — Jobs Analysis

Build main jobs, related jobs, functional jobs, emotional jobs, social jobs, desired outcomes, current solutions, anxieties, switching forces, and Jobs Graph.

Output: `JTBD Report`.

### Stage 5 — Value Proposition

Create value hypotheses, positioning, USP, offers, proof points required, objection handling, and message-market fit hypotheses.

Output: `Value Proposition Report`.

### Stage 6 — RAT

Find riskiest assumptions, critical hypotheses, unknowns that could kill the product, and the order of tests.

Output: `RAT Report`.

### Stage 7 — Validation Plan

For each hypothesis define experiment, sample, channel, cost estimate, timeline, success criteria, failure criteria, instrumentation, decision rule, and next action.

Output: `Hypothesis Validation Plan` and, when relevant, `Customer Development Plan`.

### Stage 8 — Product Definition

If the user wants product, MVP, design, development, PRD, roadmap, launch plan, commercial proposal, or full package, create product definition artifacts: Product Brief, MVP recommendation, user stories, functional requirements, non-functional requirements, UX requirements, analytics requirements, technical requirements, release plan, risks, and roadmap.

Output: `Product Requirements Document` and relevant handoff sections.

## Method references

Load reference files only when needed:

- Read `references/methods.md` for compact definitions of AJTBD, ABCDX, RAT, Customer Development, validation, and prioritization tables.
- Read `references/output-templates.md` for detailed final-document, PRD, design, development, investment memo, and commercial proposal templates.
- Read `references/quality-checklist.md` before finalizing to verify completeness, evidence labeling, and handoff readiness.

## Default final output

By default, produce one unified Markdown document. Make it client-ready and usable by product, design, development, commercial, and investment stakeholders.

```markdown
# Product Discovery & Validation Package

## 1. Executive Summary
## 2. Product Idea Interpretation
## 3. Market Research
## 4. Market Map
## 5. Segment Discovery
## 6. Segment Prioritization
## 7. AJTBD Analysis
## 8. Jobs Graph
## 9. Value Hypotheses
## 10. RAT Analysis
## 11. Hypothesis Validation Plan
## 12. Customer Development Plan
## 13. MVP Recommendation
## 14. Product Requirements Document
## 15. UX Requirements
## 16. Technical Requirements
## 17. Analytics Requirements
## 18. Release Plan
## 19. Risks & Assumptions
## 20. Recommended Next Actions
```

If the user selected a subset, produce the requested sections plus all prerequisite sections needed for a useful, non-misleading document.

## Required tables

Include these tables where relevant:

### Evidence register

| Claim | Type: Fact/Hypothesis/Assumption | Evidence | Source | Confidence | Gap | Verification method |
|---|---|---|---|---|---|---|

### Segment prioritization

| Segment | AJTBD trigger | ABCDX profile | Pain intensity | Reachability | WTP hypothesis | Strategic fit | Risk | Priority |
|---|---|---|---:|---:|---:|---:|---:|---:|

### RAT matrix

| Assumption | Why risky | Impact | Uncertainty | Testability | RAT priority | First test |
|---|---|---:|---:|---:|---:|---|

### Validation plan

| Hypothesis | Experiment | Audience/sample | Channel | Cost | Duration | Success criteria | Failure criteria | Decision after test |
|---|---|---|---|---:|---|---|---|---|

### Product requirements

| Requirement | User story/job | Priority | Acceptance criteria | Dependencies | Analytics event | Notes |
|---|---|---|---|---|---|---|

## Completion criteria

Do not consider the work complete until the user has received, at minimum:

- Market analysis.
- Segments.
- Jobs/AJTBD analysis.
- Value hypotheses.
- RAT or equivalent risk prioritization.
- Hypothesis validation plan.

Also include product requirements, design requirements, and development requirements when requested or when the selected output implies product/MVP/design/development handoff.
