# Agent-Track Topic Scoring: A1-A9 Framework

## Scoring Criteria Reference
- **A1 (Autonomy)**: Can agent execute fully autonomously? Y/N/B (B=Partial)
- **A2 (Complexity)**: Task complexity for agent (1-3)
- **A3 (Data Access)**: What data/APIs does it need? (1-3)
- **A4 (Output)**: Output format/complexity (1-3)
- **A5 (Error Handling)**: Error recovery complexity (1-3)
- **A6 (Market Size)**: Estimated market potential (1-3)
- **A7 (Demand Signal)**: Direct demand validation via web search (1-3)
- **A8 (Differentiation)**: Differentiation from existing solutions (1-3)
- **A9 (Margin)**: Business model/margin potential (1-3)

---

## Topic 1: Automated Scholarship Application Tracker

**Description**: Agent tracks scholarship deadlines, notifies students, helps prepare applications.

### A1-A9 Scores

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| A1 (Autonomy) | **Y** | Agent can fully autonomously: (1) scrape/web-search for scholarship listings, (2) maintain deadline calendar, (3) send reminder notifications, (4) help draft application materials using LLM, (5) track submission status. All steps are automatable. |
| A2 (Complexity) | **2** | Medium complexity. Multiple data sources (scholarship databases, university sites), natural language generation for application help, calendar/schedule management. Not trivially simple but well within agent capabilities. |
| A3 (Data Access) | **2** | Needs: scholarship databases (web scraping or APIs), email/notification system, document storage, user profile data. No highly restricted APIs required. |
| A4 (Output) | **2** | Multi-modal outputs: calendar events, email notifications, draft application documents, status tracking dashboards. Each is straightforward to generate. |
| A5 (Error Handling) | **2** | Moderate. Deadline changes, scholarship cancellations, email delivery failures — all have clear recovery paths (retry, user notification). |
| A6 (Market Size) | **3** | Large market. ~20M US college students, millions internationally, plus parents. Education expense is a major pain point. |
| A7 (Demand Signal) | **3** | **Strong demand validated**: GitHub issue documents "Students can't track multiple scholarship application statuses and deadlines in one place" as a documented problem. |
| A8 (Differentiation) | **2** | Some existing tools (ScholarshipTracker apps) but none with full agentic automation. Differentiation via autonomous deadline monitoring, proactive outreach, LLM-powered application drafting. |
| A9 (Margin) | **2** | Freemium model viable (students), B2B potential via universities/aid offices. Recurring revenue possible. |

### Market Validation (M6)

- **M6a (Existing Products)**: Limited dedicated scholarship tracker agents found. No major agentic solutions.
- **M6b (People Asking)**: Yes — GitHub issue: "Students can't track multiple scholarship application statuses and deadlines in one place" (muaddibco/RealWorldProblems#886) — https://github.com/muaddibco/RealWorldProblems/issues/886
- **M6c (Competitor Count)**: Low-Medium. Few direct competitors in agentic scholarship tracking space.
- **M6d (Willingness to Pay)**: Students are price-sensitive but education/tools have precedent. Universities pay for student success tools.

### Summary
```
TOPIC: Automated scholarship application tracker
A1-A9: Y-2-2-2-2-3-3-2-2
TOTAL: 18/27
STATUS: KEEP
ONE-LINE: Strong autonomous agent fit with validated pain point; large student market with low competition in agentic space.
```

---

## Topic 2: Automated Competitive Intelligence Report for E-Commerce

**Description**: Agent monitors competitor product listings, pricing, reviews, generates weekly PDF reports.

### A1-A9 Scores

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| A1 (Autonomy) | **Y** | Agent can fully autonomously: (1) scrape competitor sites/APIs, (2) track price/title changes, (3) aggregate review sentiment, (4) compile into PDF reports, (5) email distribute. Well-established automation patterns. |
| A2 (Complexity) | **2** | Medium complexity. Web scraping, data aggregation, report generation. PDF generation is standard. |
| A3 (Data Access) | **2** | E-commerce sites (public scraping), optional: Amazon API, competitor APIs. Reasonable access. |
| A4 (Output) | **2** | Structured reports: PDF with charts, price history, sentiment summaries. Standard agent output. |
| A5 (Error Handling) | **2** | Site structure changes, API rate limits, missing data — all have standard mitigation (retry, fallback sources). |
| A6 (Market Size) | **3** | Massive. All e-commerce sellers (Amazon, Shopify, DTC) need competitive intelligence. |
| A7 (Demand Signal) | **3** | **Very strong demand validated**: Multiple GitHub repos building this: ecom-agent, ecommerce-ops-suite, n8n-ai-price-monitor, SAGE agent, bigman-engine competitive reports, Lamatic Intelligent Watchdog, amazon-seller-autopilot EPIC. |
| A8 (Differentiation) | **1** | **High competition**. Many existing solutions: Prisync, Competera, WebKoll, plus numerous open-source tools. Differentiation needed via agent-native architecture, autonomous decision-making. |
| A9 (Margin) | **3** | B2B SaaS model with strong willingness to pay. E-commerce sellers routinely pay $100-500+/month for intel tools. |

### Market Validation (M6)

- **M6a (Existing Products)**:
  - ecom-agent - https://github.com/yoligehude14753/ecom-agent
  - ecommerce-ops-suite - https://github.com/jian1929/ecommerce-ops-suite
  - n8n-ai-price-monitor - https://github.com/gsavla6-hue/n8n-ai-price-monitor
  - Lamatic Intelligent Watchdog - https://github.com/Lamatic/AgentKit (PR #109)
  - SAGE Competitor Intelligence Agent - https://github.com/TommyNationPol1984/ovenos-pos (Issue #52)
  - bigman-engine market intel - https://github.com/HMHY10/bigman-engine
  - amazon-seller-autopilot EPIC - https://github.com/adaptative/amazon-seller-autopilot (Issue #28)

- **M6b (People Asking)**: Extensive GitHub activity showing active development of this exact agent type.

- **M6c (Competitor Count)**: High. Many players including Prisync, Competera, Bevy, Sellzone, Helium 10, etc.

- **M6d (Willingness to Pay)**: Very high. E-commerce sellers pay premium for competitive advantage. $100-1000+/month common.

### Summary
```
TOPIC: Automated competitive intelligence report for e-commerce
A1-A9: Y-2-2-2-2-3-3-1-3
TOTAL: 18/27
STATUS: KEEP (with differentiation caveat)
ONE-LINE: Highly autonomous and demanded but crowded market — needs unique angle (agent-native, specific vertical, or superior UX).
```

---

## Topic 3: Automated Podcast Guest Matching Service

**Description**: Agent matches podcast hosts with potential guests based on topic expertise, automates outreach.

### A1-A9 Scores

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| A1 (Autonomy) | **Y** | Agent can fully autonomously: (1) discover podcasts by topic/niche, (2) identify potential guests via LinkedIn/social, (3) score match quality, (4) generate personalized outreach, (5) send emails. |
| A2 (Complexity) | **2** | Medium complexity. Topic matching requires NLP/embedding similarity, outreach personalization needs LLM, email sending is standard. |
| A3 (Data Access) | **2** | Needs: podcast databases (Apple, Spotify APIs), LinkedIn/Twitter for guest discovery, email delivery. All reasonably accessible. |
| A4 (Output) | **2** | Matched guest lists with scores, personalized email templates, outreach tracking. Standard outputs. |
| A5 (Error Handling) | **2** | Guest unavailable, email bounces, podcast changed focus — all standard recovery paths. |
| A6 (Market Size) | **2** | Medium. ~2.5M podcasts, many hosts seek guests. Growing with podcast popularity. |
| A7 (Demand Signal) | **3** | **Strong demand validated**: Multiple GitHub repos building this: podcast-outreach, N8N-outreach, podcast guest finder, Podcast Strategist agent. |
| A8 (Differentiation) | **2** | Existing platforms (PodMatch, MatchMaker.fm, PodcastGuests) but none agent-native/autonomous. Differentiation via full automation, continuous monitoring, LLM-powered personalization. |
| A9 (Margin) | **2** | Subscription model viable ($29-99/mo range). B2C podcasters + B2B podcast networks. |

### Market Validation (M6)

- **M6a (Existing Products)**:
  - podcast-outreach - https://github.com/marcuswest-lab/podcast-outreach
  - N8N-outreach - https://github.com/mzmalik22/N8N-outreach
  - Podcast guest finder - https://github.com/cassandramjaime/BrandManager (PR #7)
  - Podcast Strategist - https://github.com/msitarzewski/agency-agents (PR #140)
  - Existing platforms: PodMatch.com, MatchMaker.fm, PodcastGuests.co

- **M6b (People Asking)**: Yes — multiple GitHub repos explicitly building podcast guest automation.

- **M6c (Competitor Count)**: Medium. Few agent-native solutions. PodMatch/MatchMaker are marketplace models, not autonomous agents.

- **M6d (Willingness to Pay)**: Moderate-High. Podcasters willing to pay for audience growth. $20-100/mo range acceptable.

### Summary
```
TOPIC: Automated podcast guest matching service
A1-A9: Y-2-2-2-2-2-3-2-2
TOTAL: 17/27
STATUS: KEEP
ONE-LINE: Strong autonomous fit with validated demand; fewer agent-native competitors than e-commerce intel; medium market size but room to own niche.
```

---

## Final Rankings

| Rank | Topic | Total | Status | Key Insight |
|------|-------|-------|--------|-------------|
| 1 | Scholarship Tracker | 18/27 | KEEP | Validated pain point, large market, low competition in agentic space |
| 2 | E-Commerce Intel | 18/27 | KEEP* | Strong demand/autonomy but crowded market — needs differentiation |
| 3 | Podcast Guest Matching | 17/27 | KEEP | Good fit, validated demand, medium competition, solid model |

*E-commerce intel: Keep if unique differentiation angle exists; otherwise crowded.

## Notes
- All three topics score Y on A1 (autonomy) — all fully executable by agents
- A7 (demand) scores 3/3 across all three — strong validation from GitHub activity
- E-commerce intel has highest competition (A8=1) despite strongest demand signal
- Scholarship tracker has best differentiation opportunity (underserved market)
