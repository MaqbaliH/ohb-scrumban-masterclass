# OHB Controlled Scrumban Framework — Master Study Guide & Conviction Playbook

**Prepared for**: Hassan Al-Maqbali, Agile Project Manager / Scrum Master  
**Source Baseline**: `OHB_Agile_Delivery_Executive_Presentation.pptx` (*OHB Agile Delivery Framework v0.1 — October 2026*)  
**Governance Alignment**: OHB P1–P5 Stage-Gate SOP, Audit Findings Remediation, CAB/CAT, Risk, ISO & CBO Compliance

---

## Executive Summary (BLUF)

**Bottom Line Up Front**: OHB is not adopting "textbook Scrum." Textbook Scrum assumes one dedicated team building one product with 100% capacity for new features in a low-regulation environment. At OHB, **one shared delivery team** supports **multiple products and Product Owners**, juggles **mixed work classes** (new MVPs, enhancements, UAT support, defects, production operations), answers to **fixed quarterly management horizons**, and operates under **strict banking governance** (CBO, Risk, ISO, VAPT, CAB, Audit).

To succeed at OHB, the proposed framework combines four elements into a **Controlled Scrumban Operating System**:
1. **Quarterly Portfolio Governance** (Management selects outcomes, capacity envelopes, and commitment tiers)
2. **Scrum Cadence** (Timeboxed Sprints for planning, demoing working software, and continuous improvement)
3. **Kanban Flow Controls** (One Shared Ready Queue, WIP limits, pull mechanics, aging tracking, and explicit Service Classes)
4. **DevOps Ownership** (The team builds, deploys, monitors, and supports what it delivers)

As **Agile Project Manager / Scrum Master**, you are the **lynchpin of this entire operating system**. You do not decide business value (Product Owners do) or cross-product portfolio rank (the Agile Management Group does)—you **own the flow, facilitate Weekly Replenishment, enforce the Readiness Gate (DoR) and Policy Stack, and protect the delivery team from chaos**.

---

## Part 1: Why You Should Believe in This Model (The Conviction Engine)

Before you can convince ExCom, Product Owners, Risk, or Developers, you must believe in the engineering and management logic behind this framework. Here is why this model is the **exact right answer** for OHB right now.

### 1. Why Pure Waterfall (Current P1–P5 Execution) Breaks in P4
In OHB's current 5-Phase SOP (`P1 Initiate → P2 Plan & Define → P3 Design → P4 Execute → P5 Close`), projects regularly stall in **P4 Execute** (averaging 188 WDs against a 160 WD SLA) and suffer from known PMO Audit Findings:
* **Audit Finding F12 (Weak)**: *The 90–160 WD build phase in P4 has zero interim milestones or checkpoints.* Sponsors wait months in the dark, only to discover during UAT that the software doesn't match business reality.
* **Audit Finding F15 (Adequate/Gap)**: *No structured regression testing after UAT defect fixes.* Late testing creates massive defect backlogs right before CAB.
* **Audit Finding F17 (Weak)**: *No benefits realization tracking post-Go-Live.* Projects close on paper without proving KPI impact.

### 2. Why "Textbook Scrum" Would Also Fail at OHB
If OHB tried standard textbook Scrum tomorrow, it would collapse within two Sprints because:
* **Multi-Product Contention**: Multiple Product Owners (BLs) compete for the same developers. In textbook Scrum, there is only one Product Owner and one Product Backlog. Without a **Shared Ready Queue** and **Replenishment rules**, POs lobby developers directly and whoever shouts loudest wins.
* **The "100% Feature Capacity" Myth**: Textbook Scrum assumes the team spends 100% of the Sprint on new Sprint Backlog stories. At OHB, the same team must support active UAT cycles, fix production defects, handle regulatory fixed dates, and build CI/CD enablers. Ignoring this guarantees broken Sprint commitments.
* **Banking Governance Reality**: You cannot tell ISO, Risk, CAB, or the Central Bank of Oman (CBO) "we value working software over comprehensive documentation." Evidence, Maker-Checker controls, VAPT, and UAT sign-offs must be **built into the workflow by design**, not skipped.

### 3. Why Controlled Scrumban Wins
> **Your Core Conviction Mantra**:  
> *"The objective is not 'more Agile ceremonies'; it is faster learning with clearer commitments and stronger control."* (Slide 2)

| OHB Pain Point | How Controlled Scrumban Solves It |
| :--- | :--- |
| **POs fighting over developers** | **One Shared Ready Queue** fed by explicit **Weekly Replenishment** rules; POs cannot inject work directly into the team. |
| **Unplanned support & UAT derailing Sprints** | **70% / 20% / 10% Capacity Envelopes** + **6 Service Classes** make UAT (20%) and Operations (10%) visible and planned. |
| **Scope creep disguised as "Agile flexibility"** | **Protected MVP Boundary** (`Mandatory MVP` vs `Stretch MVP` vs `Post-MVP`) + **Explicit Displacement Rule** (adding scope requires deferring scope, using contingency, or revising the forecast). |
| **All-or-nothing commitments on vague ideas** | **3-Tier Roadmap** (`Committed` vs `Forecast` vs `Pipeline Candidate`) separates discovery from production promises. |
| **Audit / Risk fear of losing control** | **6 Lifecycle Gates (G1–G6)** + **8-Stage Workflow** with embedded Maker-Checker, DoR, Route A/B/C testing, and CAB release gates. |

---

## Part 2: Deep Breakdown of the Operating Architecture

### 1. The 8 OHB Delivery Principles (Slide 4)
Memorize these eight principles—they are your constitution when coaching stakeholders:
1. **Outcome before output**: We measure business KPIs and working journeys, not how busy developers are or how many documents were written.
2. **Finish before starting more**: Stop starting and start finishing. Capping Work in Progress (WIP) speeds up delivery.
3. **Variable scope with explicit trade-offs**: Scope inside an approved boundary can evolve, but every addition has a visible cost (displacement).
4. **Controls by design**: Security, Maker-Checker, and audit evidence happen *during* the workflow, not as a panic before CAB.
5. **Visible constraints**: Blockers, aging items, and capacity limits are displayed openly on the board.
6. **Evidence as work progresses**: Every transition across the board generates its required compliance artifact naturally.
7. **Measure the system**: Metrics diagnose workflow bottlenecks; they are never used to rank or punish individual engineers.
8. **Validate early and continuously**: Continuous PO validation and automated/iterative testing prevent UAT shock.

---

### 2. Decision Horizons: Who Decides What? (Slides 6 & 20)
One of the biggest sources of friction at OHB is executives micro-managing story order, or developers making unapproved scope commitments. The framework establishes **5 distinct decision horizons**:

1. **Annual / Demand Horizon** → **Authority**: *ExCom / Corporate Approval Authority* → **Decides**: Strategic needs & funding direction.
2. **Quarterly Portfolio Horizon** → **Authority**: *Agile Management Group* → **Decides**: Quarterly outcomes, `Committed` vs `Forecast`, and scarce capacity allocation.
3. **Product / Feature Horizon** → **Authority**: *Product Owner (BL)* → **Decides**: Value ordering within approved objectives (`Mandatory MVP` vs `Stretch MVP`).
4. **Sprint Horizon** → **Authority**: *Scrum Team (PO + SM + Devs)* → **Decides**: Sprint Goal & feasible ready work selection.
5. **Daily Flow Horizon** → **Authority**: *Development Team (Stewarded by SM)* → **Decides**: Pulling next eligible item & managing WIP limits.

> **Memorize this power-separation line from Slide 6**:  
> *"Management chooses outcomes; Product Owners choose value order; the team chooses the feasible plan and technical sequence."*

---

### 3. End-to-End Lifecycle & The 6 Governance Gates (G1–G6) (Slide 7)

`1. DEMAND` → **[G1: Demand Approval]** → `2. PIPELINE CANDIDATE` → **[G2: Discovery Readiness]** → `3. FORECAST / STRETCH` → **[G3: Quarterly Planning]** → `4. COMMITTED` → **[G4: Story Ready (DoR)]** → `5. DELIVERY` → **[G5: UAT Accepted]** → `6. RELEASE` → **[G6: Release Ready]** → `7. VALUE`

#### Bridging G1–G6 to OHB's P1–P5 SOP (Your Translation Table for PMO & Audit)
| Scrumban Stage & Gate | What Happens Here | Equivalent OHB P1–P5 Phase & Artifacts |
| :--- | :--- | :--- |
| **Stage 1: Demand → Gate G1 (Demand Approval)** | Problem statement, Executive Sponsor identified, target business outcome & KPI defined. | **P1 Initiate**: Demand Request / Concept Form logged in PPM Central, Stakeholder Register, CBO determination. |
| **Stage 2: Pipeline Candidate → Gate G2 (Discovery Readiness)** | Discovery, architecture spikes, high-level sizing (`XS–XL`), reducing material unknowns, checking regulatory/security flags. | **P2 Plan & Define (Early)**: Charter, High-Level Business Case, initial RAID, early Security/CBO/Procurement triggers. |
| **Stage 3: Forecast / Stretch → Gate G3 (Quarterly Planning)** | Feature groups broken down (`Mandatory MVP` vs `Stretch`), dependencies & controls mapped, capacity checked by Agile Management Group. | **P2/P3 Transition**: High-Level Plan (HLP), BRD/FSD baseline at feature-group level, Solution Design spine. |
| **Stage 4: Committed → Gate G4 (Story Ready / DoR)** | Quarterly commitment locked. Features refined into testable user stories meeting Definition of Ready (DoR) to enter the **Shared Ready Queue**. | **P3 Design → P4 Execute Entry**: Detailed requirements slices, RTM traceability, Test Strategy readiness. |
| **Stage 5: Delivery → Gate G5 (UAT Accepted)** | Iterative Sprint execution, Maker-Checker code review, technical testing, PO story validation, and integrated Feature/UAT sign-off. | **P4 Execute (Build, SIT, UAT)**: Replaces the 160-WD black box (Audit Finding F12) with transparent 2-week increments and continuous UAT evidence. |
| **Stage 6: Release → Gate G6 (Release Ready)** | VAPT/NFT sign-off, rollback plan verified, CAB/CAT approval, CDC approval (if public-facing), production deployment. | **P4 Go-Live Gate**: Security Assessment Report, Cutover Plan, CAB/CAT approval in ManageEngine, SDP. |
| **Stage 7: Value (Post-Release)** | Production hypercare/stabilization and empirical KPI review against the original Demand target. | **P5 Close**: Project Closure Report, BAU transition, and **PIR with Benefits Realization** (solves Audit Finding F17). |

---

### 4. Roadmap Categories & Protecting the MVP Boundary (Slides 8 & 9)

#### How Management Sees the Portfolio Roadmap (Slide 8)
Never let stakeholders treat every item on a roadmap as a guaranteed deadline. The roadmap is divided into three strict zones:
1. **Committed (Committed Goal)**: What OHB formally expects to deliver this quarter. Mandatory MVP scope, capabilities, dependencies, controls, testing, release activities, and team capacity are **all confirmed**. *Measured for commitment reliability.*
2. **Forecast (Stretch Goal)**: Planning-ready work OHB intends to pursue *if* capacity or an explicit condition is met. Shown separately on the roadmap and **excluded from commitment-reliability penalties**.
3. **Pipeline Candidate**: Approved demand still in discovery or refinement. The roadmap shows **discovery timing and decision date only—never a production Go-Live date**.

#### How Product Owners Protect the MVP Boundary (Slide 9)
Within an approved initiative, features are decomposed into three rings:
* **Ring 1 — Mandatory MVP**: Strictly required for the approved objective, KPI, regulatory control, or viable end-to-end user journey. *This is what is committed.*
* **Ring 2 — Stretch MVP**: Valuable enhancements that improve the experience but can be deferred without breaking the core MVP objective. *Used as the buffer to protect the release date.*
* **Ring 3 — Post-MVP Enhancements / Standard Work**: Further automation or nice-to-haves not required for first productive use.

> **The Iron Law of Scope Trade-Offs (Slide 9)**:  
> *"Commit the outcome and mandatory feature groups, not every detailed story. A scope addition must create a visible trade-off: defer other scope, use approved contingency, or revise the forecast."*

---

### 5. The 3-Level Prioritization Model & The Shared Ready Queue (Slides 10–13)

Why doesn't OHB use one single scoring formula for everything? Because comparing a quarterly strategic banking product against a 2-day production bug or a CI/CD upgrade using the same scorecard is mathematically meaningless (Slide 10). Instead:
* **Level 1 (Quarterly Portfolio)**: Agile Management Group ranks MVP goals, material enhancements, and technical enablers → Outputs `Committed / Forecast / Candidate`.
* **Level 2 (Product & Feature)**: Each Product Owner orders their own backlog (`Mandatory MVP → Stretch MVP → Post-MVP`) → Outputs `Ordered Feature Groups`.
* **Level 3 (Sprint & Flow)**: Scrum Team / Dev Team pulls from **One Shared Ready Queue** → Outputs `Sprint Goal + Daily Pull Execution`.

#### How Cross-Product Priority is Resolved (Slide 11)
The presentation evaluates three governance options and **recommends Option A** (paired with work-type capacity envelopes from Slide 15):
* **Option A (RECOMMENDED): Executive-Led Quarterly Order** — The Agile Management Group ranks outcomes quarterly; Weekly Replenishment executes within those boundaries. *(High clarity of authority, low meeting overhead).*
* **Option B: Capacity Envelopes** — Management allocates % capacity by work purpose or product; POs order inside their bucket. *(Good for protecting UAT/Ops/Engineering, risky if POs treat % as permanent political entitlements).*
* **Option C: Product Owner Alignment Forum** — POs negotiate the near-term queue together. *(High consensus risk—POs rarely volunteer to put another PO's product ahead of their own).*

#### The 6-Step Policy Stack: How the Next Item is Selected (Slide 13)
Whenever two items compete to enter the Shared Ready Queue or be pulled next, you apply this **exact 6-step filter in order** (this eliminates political lobbying):

1. **AUTHORIZED**: Is this item allowed to consume capacity? It must belong to an approved source: a *Committed Goal*, an approved *Stretch Goal*, an *Operational/Support Reserve*, a *Technical Enabler allocation*, an *authorized Fixed-Date obligation*, or a valid *Expedite* item. *(If a PO tries to sneak in an unapproved pet feature, it fails Step 1 immediately).*
2. **READY**: Does it meet the **Definition of Ready (DoR)**? Clear expected outcome, testable acceptance criteria, appropriately sized (`Small` or `Medium`), dependencies understood, required access/data/environments identified, and zero blocking issues. *(Authorized means OHB permits the work; Ready means the team can responsibly start it).*
3. **SERVICE CLASS**: What class of service does it carry? (`Expedite → Fixed Date → Committed → Operational → Enabler → Stretch`).
4. **CAPACITY**: Does the relevant **WIP limit** and **capacity reserve** allow entry right now?
5. **ORDER**: Within its class, how does it rank by **Goal contribution, urgency, risk reduction, dependency unlocking, size, and learning value**?
6. **DISPLACEMENT**: If this item is injected ahead of planned work, what specific work is displaced and what is the impact on the quarterly forecast?
* *Tie-Breaker Only*: **FIFO (First-In, First-Out)** is used *only* when two items are completely equivalent across Steps 1–6.

---

### 6. The 6 Classes of Service & Capacity Envelopes (Slides 15 & 19)

#### The 6 Service Classes (Slide 19)
| Service Class | Definition at OHB | Operating Policy & Flow Rule |
| :--- | :--- | :--- |
| **1. EXPEDITE** | Critical production outage, material security/data breach, or hard blocker to a committed release. | **Global WIP Limit = 1**. Can preempt active work, but **must explicitly show displaced work**. |
| **2. FIXED DATE** | Regulatory (e.g., CBO deadline) or immovable operational date. | Sequenced by **Latest Responsible Start Date** so it finishes on time without becoming a last-minute Expedite. |
| **3. OPERATIONAL** | Production support and live defects for products the team operates (DevOps ownership). | Consumes the dedicated **Operational Capacity Reserve (10%)**; triaged by severity. |
| **4. TECHNICAL ENABLER** | Infrastructure, CI/CD, licensing, test automation, architectural refactoring, and engineering controls. | **Plan explicit capacity**; never treat engineering health as "spare-time/weekend work." |
| **5. STANDARD** | Normal MVP stories, enhancements, non-critical defects, and routine technical work. | Pulled in order from the **Shared Ready Queue** within normal WIP limits. |
| **6. SPIKE** | Research/prototype activity to reduce a material technical or functional unknown. | Strictly **time-boxed**; output is **evidence and a decision**, not production code. |

#### The Pilot Capacity Allocation Hypothesis (Slide 15)
> *"The team cannot assume 100% of capacity is available for new feature development."*

* **70% — Planned MVP / Features** (Committed Goals, Stretch Goals, and planned Technical Enablers)
* **20% — UAT & Release Support** (Supporting business users in UAT, fixing UAT findings, CAB prep, cutover support)
* **10% — Operations / Urgent Work** (Live production support, incident triage, urgent operational fixes)

---

### 7. Progressive Estimation: "Estimate Coarsely Early; Forecast Empirically" (Slide 14)

| Backlog Layer | Estimation Unit | Decision Purpose |
| :--- | :--- | :--- |
| **1. Demand / Candidate** | `XS – XL` T-shirt size + Uncertainty rating | Decide discovery need and broad feasibility (Gate G1/G2). |
| **2. MVP / Quarter Goal** | Mandatory feature-group sizes + dependencies | Build quarterly capacity scenario and lock `Committed` scope (Gate G3). |
| **3. Feature / Enhancement** | `XS – XL` + Reference Feature comparison + value inputs | Assess quarterly fit and scope trade-offs. |
| **4. User Story** | Right-sized: `Small / Medium / Too Large` *(Story points optional)* | Split `Too Large` stories and select feasible work for the Sprint (Gate G4). |
| **5. Technical Task** | Optional hours or no estimate | Immediate day-to-day developer coordination only. |
| **6. Delivery System** | Empirical **Throughput** (items/week) + **Cycle-Time distributions** | Probabilistic future forecasting (e.g., Monte Carlo / cycle-time percentiles). |

> **Golden Rule of Estimation (Slide 14)**:  
> *"Estimate informs forecast; forecast informs commitment; an estimate is never a commitment."*

---

### 8. The 8-Stage Delivery Workflow, Control Gates & 3 Validation Routes (Slide 18)

`1. Ready` *(Story Ready / Entry Evidence)* → `2. Active Dev` → `3. Code Review` *(Maker-Checker & Code Quality)* → `4. Technical Test` → `5. PO Validation` *(Story Accepted / Business Behaviour)* → `6. Feature / UAT` *(G5: UAT Accepted / E2E Evidence)* → `7. Release Ready` *(G6: Controls + Rollback + CAB)* → `8. Live` *(MVP Live / Prod Validation)*

#### The 3 Validation Routes (Slide 18)
* **Route A — Independently Testable Story**: Tested and validated by the Tester and Product Owner right at the Story level (`Columns 4 & 5`), followed by standard feature/release regression in `Column 6`.
* **Route B — Connected Story**: Individual stories are technically verified (`Columns 3 & 4`), and full business/UAT validation occurs in `Column 6 (Feature / UAT)` once the connected stories come together to form a usable end-to-end feature.
* **Route C — Technical Enabler**: Validated via technical acceptance criteria first, then verified through the consuming business feature and release assurance tests.

---

## Part 3: Your Mastery Playbook as Agile PM / Scrum Master

### 1. Your 3 Core Accountabilities
1. **Flow Steward**: You monitor WIP limits, Work-Item Age, and Blocked-Time Ratio daily. When work stalls in `Code Review` or `PO Validation`, you make the bottleneck visible and mobilize action to clear it.
2. **Neutral Replenishment Facilitator**: You chair the **Backlog Replenishment** ceremony and administer the **Shared Ready Queue**.
   * **What you DO**: Verify that items meet the **Authorized** and **Ready (DoR)** policies, enforce WIP/capacity envelopes, and ensure any mid-stream injection documents its **Displacement** impact.
   * **What you NEVER DO**: You never unilaterally decide business value or play favorite between Product Owners. Staying process-neutral protects you politically and forces POs and the Agile Management Group to own business trade-offs.
3. **Continuity & Governance Guardian**: You maintain documented queue procedures, visible decision logs (which map straight into PPM Central / Audit trails), and train a **delivery-side deputy** so the system has zero key-person dependency (Slide 12).

### 2. The 7 Ceremonies You Run (Slides 16 & 17)
| Ceremony | Cadence | Key Participants | Distinct Decision Purpose |
| :--- | :--- | :--- | :--- |
| **1. Quarterly Planning** | Quarterly (Gate G3) | Agile Mgmt Group, Sponsors, POs, SM, Tech/Shared Functions | Approve quarterly Outcomes, classify `Committed / Forecast / Candidate`, set 70/20/10 capacity envelopes, and lock control/release windows. |
| **2. Feature Refinement** | Ongoing / Mid-Sprint | PO, Tech Lead/Devs, QA, SM | Break approved features into testable slices (`Small/Medium`), assign **Route A/B/C**, and confirm dependencies. |
| **3. Backlog Replenishment** *(New Ceremony!)* | Weekly or Pre-Sprint | POs, SM (Facilitator), Dev Lead | Filter candidate stories through the **6-Step Policy Stack** and admit Ready work into the **One Shared Ready Queue** within WIP limits. |
| **4. Sprint Planning** | Start of Sprint | Scrum Team (POs, Devs, SM) | Set **one primary Sprint Goal** and pull a conservative, feasible batch of Ready work from the Shared Ready Queue. |
| **5. Daily Flow Review** | Daily (15 mins) | Development Team + SM (POs optional/as needed) | **Do NOT ask "What did you do yesterday?"** Walk the board **Right-to-Left** (`Release Ready ← UAT ← PO Validation ← Test ← Code Review ← Dev`). Focus on: *Finishing closest-to-done items, Work-Item Age, Blockers, and WIP violations.* |
| **6. Sprint Review** | End of Sprint | Scrum Team, Sponsors, Business Stakeholders | Inspect integrated, working software (not slide decks!) and feed stakeholder feedback back into the ordered Product Backlog. |
| **7. Retrospective** | End of Sprint | Scrum Team (Devs, PO, SM) | Inspect flow/quality metrics (cycle time, UAT leakage, blocked time) and commit to **1 or 2 concrete system improvements** for the next Sprint. |

---

### 3. The Metrics Dashboard You Champion (Slide 21)

* **1. OUTCOMES**: MVP Milestone Reliability | User Adoption & Turnaround Time | Benefit Realization (PIR KPIs)
* **2. PREDICTABILITY**: Committed Feature Delivery (%) | Sprint Goal Achievement Rate | Forecast Range vs. Actual Delivery
* **3. FLOW**: Throughput (items/week) | Cycle Time (start to live) | Work-Item Age | Blocked-Time Ratio
* **4. QUALITY & CAPACITY**: UAT Defect Leakage | Escaped Production Defects | Actual Operational & UAT Consumption
* **PROHIBITED MANAGEMENT METRICS**: Individual Developer Velocity, Lines of Code (LoC), and AI Prompt Counts.

---

## Part 4: The Persuasion & Objection-Handling Playbook (Convincing OHB)

### 1. Pitching to ExCom / MSSC / Sponsors
* **Their Hidden Fear**: *"Agile means the team won't give me a fixed deadline or scope, and they'll use 'Agile' as an excuse when they miss quarterly targets."*
* **Your Counter-Narrative**:
  > "In our current Waterfall P4 phase, you wait 160 working days in a black box and discover delays only when UAT fails at the end. Under Controlled Scrumban, you actually get **stronger quarterly commitment**. At Gate G3 (Quarterly Planning), we lock **Committed Goals** backed by confirmed capacity and a protected **Mandatory MVP boundary**. We separate speculative **Forecast** and **Pipeline Discovery** work so your Committed targets aren't sabotaged by unready ideas. And every two weeks at Sprint Review, you see working, tested software—not a green status report that turns red two days before Go-Live."

### 2. Pitching to Risk, ISO, Compliance & Internal Audit
* **Their Hidden Fear**: *"Agile teams skip documentation, bypass security reviews, and deploy cowboy code without audit trails."*
* **Your Counter-Narrative**:
  > "This framework was designed specifically for regulated banking. Instead of treating Risk, ISO, VAPT, and CAB as a last-minute hurdle at the end of P4, we embed **Controls by Design** across **6 formal Gates (G1–G6)** and **8 workflow columns**. No story can start without **Entry Evidence (G4 DoR)**. No code moves to test without **Maker-Checker peer review**. Every story follows an explicit validation route (**Route A, B, or C**). No feature hits production without **G5 (UAT Acceptance)** and **G6 (Release Ready — VAPT, Rollback Plan, CAB sign-off)**. Plus, this directly remediates **PMO Audit Finding F12** (no build checkpoints), **F15** (regression testing), and **F17** (benefits realization)."

### 3. Pitching to Business Leads / Product Owners
* **Their Hidden Fear**: *"If I can't email a developer directly or push my urgent request in mid-Sprint, my department will lose out to other departments."*
* **Your Counter-Narrative**:
  > "Right now, when every department pushes 'urgent' work directly onto developers, developers switch contexts 5 times a day. Nothing finishes, UAT drags on, and everyone's project slips. By routing all work through **Weekly Replenishment** and a WIP-limited **Shared Ready Queue**, once the team pulls your story, **they finish it before starting more**. Even better: you remain 100% in control of your Product Backlog's priority order, and if another PO wants to displace your Committed work mid-quarter, our **Cross-Product Change Rule** forbids it unless there is collective agreement or Agile Management Group escalation with visible displacement."

### 4. Pitching to Developers, Tech Leads & QA
* **Their Hidden Fear**: *"Scrumban means double the meetings, POs breathing down our necks, zero time for technical debt, and management judging our individual story points."*
* **Your Counter-Narrative**:
  > "This framework is built to protect your engineering sanity. First, **Product Owners cannot inject work directly to you anymore**—everything must pass the **Definition of Ready** and enter the single **Shared Ready Queue**, so you never have to guess which PO to listen to. Second, we stop pretending you have 100% capacity for new features: **20% of capacity is explicitly reserved for UAT/Release support and 10% for Operations**, and **Technical Enablers** (CI/CD, refactoring, automation) are a first-class Service Class. Third, **individual velocity, lines of code, and AI prompt counts are strictly prohibited** as management metrics."

---

## Part 5: The 6 Executive Decisions to Lock Before the Pilot (Slide 23)

| # | Decision Area | What Management Must Decide | Your Recommended Advisory Stance |
| :- | :--- | :--- | :--- |
| **1** | **Operating Model** | Adopt Scrumban with DevOps ownership and OHB-specific governance. | **Endorse strongly**. It is the only model that fits a single shared team supporting multiple products + BAU ops. |
| **2** | **Roadmap Language** | Choose `Committed / Stretch / Pipeline` OR retain `Committed / Forecast / Candidate`. | **Recommend `Committed / Forecast / Pipeline Candidate`** (or `Committed / Stretch / Pipeline` if executives prefer simpler goal language). The non-negotiable rule is keeping `Forecast/Stretch` excluded from commitment-reliability penalties. |
| **3** | **Prioritization Model** | Approve Option A (Executive quarterly ordering + Weekly Replenishment) as the baseline. | **Endorse Option A**. It avoids the endless deadlock of PO consensus forums (Option C) while giving you clear quarterly guardrails to run Weekly Replenishment. |
| **4** | **Capacity Policy** | Approve pilot reserves (`70% MVP / 20% UAT / 10% Ops`) and decide whether Technical Enablers get an explicit reserve. | **Recommend carving out an explicit 10%–15% Technical Enabler allocation** (e.g., `60% MVP / 10% Enablers / 20% UAT / 10% Ops`) during early Sprints so CI/CD and automated testing get built early. |
| **5** | **Queue Governance** | Approve One Shared Ready Queue, neutral facilitator (SM), and cross-product change rule. | **Non-negotiable**. Without a single queue and neutral Scrum Master enforcement, the model reverts to ad-hoc lobbying. |
| **6** | **Pilot Mandate** | Authorize **Sprint 0** and **1 controlled representative product pilot** (following the 7-step Pilot Roadmap on Slide 22). | **Endorse**. Remind leadership: *"The pilot validates the operating system (queue policy, reserves, CI/CD, control evidence), not just a single product."* |

---

## Part 6: Scenario Mastery Drills (Test Yourself Before You Teach)

### Scenario 1: The "VIP Shoulder-Tap"
* **Situation**: Tuesday mid-Sprint, PO A asks a developer directly to code a "small" GM export button today before finishing their current story.
* **Your Action**: Protect the developer using the **Shared Ready Queue** rule (Slide 12) and **6-Step Policy Stack** (Slide 13). Confirm it is not a true **Expedite** (production outage/release blocker), ensure it passes **Definition of Ready**, and route it to **Weekly Replenishment** (or require formal **Displacement** sign-off if it must preempt committed work).

### Scenario 2: The "Authorized vs. Ready" Trap
* **Situation**: PO B demands an ExCom-approved story enter the Shared Ready Queue during Replenishment even though trigger rules and test data are missing.
* **Your Action**: Invoke Slide 12/13: *"Authorized means OHB permits the work; Ready means the team can responsibly start it."* Hold it at **Gate G4 (Definition of Ready)** until acceptance criteria and test data are ready, or create a time-boxed **Spike** to resolve the unknown.

### Scenario 3: UAT Wave Colliding with Sprint Velocity
* **Situation**: Product 1 enters UAT and floods developers with questions/defects, threatening Product 2's Sprint Goal.
* **Your Action**: Track UAT work against the **20% UAT & Release Support Envelope** (Slide 15). When UAT demand exceeds 20%, surface the constraint visibly and ask POs/Agile Management Group whether to queue non-critical UAT defects as Standard items for next Sprint or formally adjust Product 2's Sprint forecast.

### Scenario 4: The "Estimate = Commitment" Pushback
* **Situation**: A Sponsor claims a rough `XS–XL` sizing given during Demand/Discovery (G1/G2) was a hard deadline commitment.
* **Your Action**: Apply **Progressive Estimation** (Slide 14): *"Estimate informs forecast; forecast informs commitment; an estimate is never a commitment."* Commitments are only made at **Gate G3 (Quarterly Planning)** after Mandatory MVP features, dependencies, and controls are confirmed.
