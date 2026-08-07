# AIOS BUILD BLUEPRINT

## Version 0.1 — Canonical Project Roadmap

**Status:** Architecture definition phase
**Purpose:** Preserve the intended design, build sequence, reasoning, and completion criteria for AIOS across chats, tools, models, and development sessions.

---

# 1. THE PROJECT

AIOS is an external executive-function system built around persistent files, AI agents, specialist domains, explicit governance, and closed-loop supervision.

Its intended hierarchy is:

USER
↓
EXECUTIVE / MASTER CONTROL
↓
DOMAIN DIRECTORS
↓
SPECIALISTS
↓
SUB-AGENTS / TOOLS / EXECUTION

Information then returns upward:

EXECUTION
↓
CHECKPOINTS + RESULTS + STATE
↓
DOMAIN DIRECTOR
↓
DIRECTOR REVIEW
↓
MASTER CONTROL
↓
ALIGNMENT REVIEW / INTERVENTION
↓
USER WHEN REQUIRED

The system must not depend on one conversation remembering everything.

Persistent files are the source of continuity.

AI sessions are replaceable compute.

---

# 2. CORE OWNERSHIP MODEL

## User owns Vision

The user decides:

* what ultimately matters
* priorities
* values
* constraints
* major objectives
* what constitutes an acceptable outcome
* decisions requiring human authority

AIOS exists to serve the user's objectives, not generate its own independent agenda.

---

## Executive owns Alignment

Master Control / Executive Function determines:

* which domain owns an objective
* relationships between objectives
* priority conflicts
* whether domain activity still serves the intended outcome
* whether intervention is required
* cross-domain coordination
* whether the system itself is functioning correctly

The Executive does not normally perform detailed domain execution.

---

## Directors own Strategy

Each major domain has a Director.

Examples might eventually include:

* AI Career Director
* SevenTwoSites Director
* Evolution Director
* other domains justified by actual need

The Director determines how its domain should achieve a mission.

It:

* understands domain context deeply
* decomposes missions
* creates and manages work
* delegates to specialists
* monitors progress
* maintains domain state
* reviews specialist output
* reports upward

---

## Specialists own Execution

Specialists perform bounded operational work.

Examples:

SevenTwoSites:

* Lead Research
* Outreach
* Sales
* Preview Builder
* Website Engineering

AI Career:

* Opportunity Research
* Candidate Positioning
* CV / Application
* Role Fit Analysis

Specialists should not independently redefine the Director's objective.

---

## Protocols govern Behaviour

All layers use shared rules for:

* missions
* tasks
* context
* checkpoints
* reviews
* state
* learning
* decisions
* escalation
* drift
* handoffs
* initialization

This prevents each domain from inventing incompatible operating methods.

---

## Knowledge lives in Persistent Storage

Important truth cannot exist only inside chat history.

The vault / repository should contain authoritative information about:

* objectives
* domain state
* decisions
* operating rules
* execution history where relevant
* project architecture
* lessons
* current missions

Chats consume and modify persistent state.

Chats are not themselves the state.

---

# 3. BUILD PRINCIPLES

The following principles govern construction of AIOS.

## Purpose before implementation

We define why something exists before deciding how it is implemented.

## Protocols before prompts

We define behaviour before writing model-specific instructions.

## Architecture before automation

We prove the information model manually before attempting autonomous orchestration.

## Alignment before activity

A large amount of activity does not constitute progress.

## Outcomes before tasks

Tasks exist because they contribute to outcomes.

## Evidence before assumptions

Persistent evidence should outrank inferred or remembered information.

## Source of truth over duplication

AIOS should know where authoritative information lives instead of copying everything everywhere.

## Simple beats clever

Complexity must earn its existence.

## Observable systems are controllable systems

Meaningful work should leave enough evidence that higher layers can understand what happened.

## Replaceable sessions

A new AI session should be able to recover operational state from persistent files.

## Human authority remains explicit

The user retains control of vision, material priority changes, and defined high-impact decisions.

---

# 4. BUILD ROADMAP

The build proceeds through eleven stages:

STEP 0 — Constitution
STEP 1 — Governance
STEP 2 — Language
STEP 3 — Protocols
STEP 4 — Architecture
STEP 5 — Executive
STEP 6 — Director Template
STEP 7 — First Director
STEP 8 — Simulation
STEP 9 — Refinement
STEP 10 — Scale

Each stage has an exit condition.

We do not advance merely because we discussed the topic.

---

# STEP 0 — CONSTITUTION

## Question

**What is AIOS?**

## Purpose

Define the enduring identity and philosophy of the system before defining implementation.

The Constitution should survive changes in:

* AI models
* Claude Code versions
* Obsidian
* directory layouts
* scripts
* automation technologies
* individual domains

It describes what the system fundamentally is.

---

## What must be defined

The Constitution should establish:

### Purpose

Why AIOS exists.

Example conceptual statement:

AIOS exists to externalize planning, coordination, persistent context, execution management, and alignment so the user can operate through one coherent system rather than independently managing many disconnected AI sessions.

### Hierarchy

The conceptual authority structure:

User
Executive
Director
Specialist
Sub-agent/tool

### Ownership

High-level ownership:

User → vision
Executive → alignment
Director → strategy
Specialist → execution

### Persistence philosophy

Sessions are temporary.

Persistent knowledge is authoritative.

### Outcome orientation

The system exists to produce real-world progress, not create administrative activity.

### Modularity

Domains should remain sufficiently isolated that changing one does not destabilize the entire system.

### Observability

Execution must leave meaningful evidence.

### Adaptability

The system may learn and improve while preserving fundamental authority boundaries.

---

## What does NOT belong here

Do not put:

* exact folder names
* detailed checkpoint templates
* Claude-specific commands
* individual business goals
* job-search criteria
* current tasks
* implementation scripts

Those belong in later layers.

---

## Deliverable

`CONSTITUTION.md`

Potential major sections:

1. Purpose
2. Operating Model
3. Authority Hierarchy
4. Core Responsibilities
5. Persistence Philosophy
6. Learning Philosophy
7. Alignment Philosophy
8. Human Authority
9. Modularity
10. Foundational Principles

---

## Exit Gate

Step 0 is complete when we can answer:

> "What is AIOS, who is responsible for what, and what fundamental principles must remain true regardless of implementation?"

without referencing any specific technology.

---

# STEP 1 — GOVERNANCE

## Question

**What is allowed?**

## Purpose

Convert the philosophy into authority boundaries.

The Constitution says what the system is.

Governance says what each component may do.

Without governance, hierarchical agents can gradually overlap responsibilities.

---

## What must be defined

### Decision rights

Determine which decisions belong to:

* User
* Executive
* Director
* Specialist

### Autonomy boundaries

For example:

A Director may be allowed to:

* change search strategy
* create specialist tasks
* commission research
* update domain working state

but may not be allowed to:

* change the user's overarching goal
* spend money
* contact external people
* destroy historical records
* redefine another domain

unless explicitly authorized.

### Escalation boundaries

Define circumstances where execution must move upward.

Example:

Specialist encounters strategic ambiguity.

↓

Escalate to Director.

Director detects conflict with another domain.

↓

Escalate to Executive.

Executive detects a material priority/value decision.

↓

Escalate to User.

### Modification rights

Define which layers may modify:

* Constitution
* Governance
* Protocols
* domain state
* task state
* source-of-truth information

### Historical integrity

Past decisions should not silently disappear.

Changes should preserve enough history to understand why the state changed.

### Reversibility

High-impact changes should be reversible where practical.

---

## Governance should answer cases such as

Can Master Control rewrite a Director's mission?

Can a Director create a new Specialist?

Can a Specialist change its own operating instructions?

Can an agent delete obsolete files?

Can a Director declare an objective complete?

Can Master change system architecture automatically?

What happens when two domains claim ownership?

What requires user approval?

---

## Deliverable

`GOVERNANCE.md`

---

## Exit Gate

Every important system action should have a clear authority owner.

If the answer to:

> "Who is allowed to make this decision?"

is ambiguous, governance is incomplete.

---

# STEP 2 — LANGUAGE

## Question

**What do our words mean?**

## Purpose

Create a shared ontology.

An AI system can appear aligned while different layers are interpreting the same terminology differently.

Therefore critical concepts require canonical definitions.

---

## Terms likely requiring definition

### Vision

A high-level desired direction owned by the user.

### Goal

A desired measurable or meaningful outcome.

### Objective

A defined result being actively pursued.

### Mission

A strategic directive issued from one authority layer to another.

Example:

Master → Director.

### Strategy

The chosen approach for accomplishing an objective.

### Project

A bounded body of work with a completion condition.

### Task

A concrete executable unit of work.

### Checkpoint

A meaningful execution milestone recorded for observability.

### State

What is currently true.

### Knowledge

Information believed to remain useful beyond one execution cycle.

### Observation

Something discovered but not necessarily accepted as enduring truth.

### Decision

A deliberate choice that constrains future behaviour.

### Assumption

Something being temporarily treated as true without sufficient verification.

### Blocker

A condition preventing useful progress.

### Drift

Meaningful divergence between intended objective and actual behaviour/outcome.

### Review

Evaluation of execution against expectations.

### Intervention

An intentional modification to restore or improve alignment.

### Completion

The explicit conditions under which work is considered finished.

---

## Why this matters

Consider:

"Find 50 applications."

That could mean:

* 50 job advertisements
* 50 jobs worth applying to
* 50 completed applications
* 50 new opportunities each day

AIOS should never rely on ambiguous interpretation of important language.

---

## Deliverable

`LANGUAGE.md`

Potentially called:

`ONTOLOGY.md`

if a more technical name becomes useful.

---

## Exit Gate

Every term used in system protocols has one sufficiently precise shared meaning.

---

# STEP 3 — PROTOCOLS

## Question

**How does information move?**

## Purpose

Define the behavioural interfaces between layers.

This is arguably the most important stage.

Protocols prevent AIOS from becoming a collection of clever but incompatible agents.

---

# 3.1 Capture Protocol

Defines how raw user input enters AIOS.

Input may be:

* thought
* idea
* goal
* complaint
* problem
* observation
* voice transcription
* task
* decision
* question

Capture should preserve the original input.

The system may subsequently classify it.

Never assume every capture item represents executable work.

---

# 3.2 Interpretation Protocol

Determines what a capture item actually means.

The Executive should extract:

* underlying intent
* expected outcome
* constraints
* urgency
* domain
* dependencies
* ambiguities
* whether action is actually required

It must distinguish examples from instructions.

---

# 3.3 Routing Protocol

Determines ownership.

Possible outcomes:

* belongs to existing domain
* belongs to multiple domains
* belongs to Executive
* requires user decision
* belongs in knowledge/reference
* requires a new domain
* no action required

Creating a new domain should have a high threshold.

---

# 3.4 Mission Protocol

Defines how Executive gives work to Directors.

A mission should communicate primarily:

* intended outcome
* strategic context
* constraints
* success criteria
* relevant authoritative sources
* priority
* boundaries

It should NOT unnecessarily prescribe every implementation step.

Director owns strategy.

---

# 3.5 Task Protocol

Defines how Directors create executable work.

Tasks should contain enough context for fresh specialist sessions.

Typical task:

Objective

Context

Relevant Sources

Constraints

Required Work

Expected Deliverable

Definition of Done

Reporting Requirements

---

# 3.6 Context Protocol

Defines what information a session should load.

Central principle:

**Minimum complete context.**

Too little context causes bad execution.

Too much context causes:

* distraction
* stale information contamination
* unnecessary token use
* domain leakage
* conflicting instructions

Every layer should know:

* its authoritative sources
* its own state
* the immediate mission
* only the external context necessary

---

# 3.7 Checkpoint Protocol

Defines how meaningful progress is recorded.

Avoid logging microscopic operations.

A checkpoint should exist when something materially changes:

* understanding
* strategy
* state
* evidence
* output
* assumptions
* blockers

Suggested conceptual structure:

Checkpoint ID

Timestamp

Objective

Actions Performed

Evidence / Findings

Decisions

State Change

Problems / Risks

Next Intended Action

---

# 3.8 State Protocol

Defines how current truth is represented.

Execution logs answer:

> What happened?

State answers:

> What is true now?

They should not be confused.

State should remain concise enough to load regularly.

---

# 3.9 Review Protocol

Defines how higher layers evaluate lower layers.

Specialist → Director review.

Director → Executive review.

Executive → User-visible review when necessary.

Possible review states:

ALIGNED

ALIGNED — IMPROVEMENT AVAILABLE

MISALIGNED

BLOCKED

COMPLETE

Review compares:

Objective

vs

Current State

vs

Observed Execution

vs

Expected Outcome

---

# 3.10 Drift Protocol

Defines how the system detects loss of alignment.

Potential drift:

### Objective Drift

Work slowly changes what it is trying to accomplish.

### Strategy Drift

Execution stops matching the chosen strategy.

### Scope Drift

The domain begins solving unrelated problems.

### State Drift

Documentation differs from reality.

### Knowledge Drift

Old facts remain treated as current.

### Metric Drift

Proxy metrics become more important than the real outcome.

Example:

Goal:

Get strong job opportunities.

Drift:

System optimizes for "number of search results."

### Complexity Drift

The system creates unnecessary infrastructure instead of producing outcomes.

---

# 3.11 Intervention Protocol

Defines what happens after drift is detected.

Possible responses:

Continue.

Adjust.

Replan.

Suspend.

Escalate.

Rollback.

Request user decision.

Every material intervention should record:

What changed.

Why.

Evidence.

Expected consequence.

---

# 3.12 Decision Protocol

Important decisions should become persistent.

A decision record should contain:

Decision

Context

Alternatives considered where relevant

Reason

Authority

Date

Effect

Superseded decision if applicable

This prevents repeatedly reopening settled questions without reason.

---

# 3.13 Learning Protocol

Determines when execution experience becomes permanent knowledge.

Not every observation deserves permanent memory.

Potential learning test:

Is it reusable?

Is it supported by evidence?

Will it change future execution?

Does it belong to this domain or system-wide?

If yes, persist it in the appropriate authoritative location.

---

# 3.14 Escalation Protocol

Defines when lower layers stop and report upward.

Specialist → Director:

strategic ambiguity
conflicting instructions
blocked execution
major unexpected finding

Director → Executive:

cross-domain conflict
mission ambiguity
priority issue
systemic problem

Executive → User:

vision choice
material priority change
high-impact irreversible action
unclear personal preference

---

# 3.15 Initialization Protocol

A fresh session should be able to initialize without conversational memory.

It should determine:

Who am I?

What do I own?

What is my current objective?

What is currently true?

What work is active?

Which files are authoritative?

What protocols govern me?

What should I do next?

---

# 3.16 Handoff Protocol

When work moves between agents, important context must move with it.

A handoff should not require the receiving agent to infer everything from logs.

---

# 3.17 Completion Protocol

"Done" must mean something.

Every mission/project/task should define completion criteria.

Completion should usually include:

* expected output exists
* required validation performed
* relevant state updated
* appropriate evidence recorded
* downstream dependencies informed where necessary

---

## Deliverables

Likely a `/Protocols/` directory containing individual protocol documents.

The final number should be determined by usefulness, not aesthetics.

---

## Exit Gate

We should be able to simulate information moving:

User → Capture → Executive → Director → Specialist → Director → Executive

without inventing behaviour halfway through.

---

# STEP 4 — ARCHITECTURE

## Question

**What exists?**

## Purpose

Translate conceptual design into an actual filesystem and information architecture.

Only now should folder/file structure become concrete.

---

## Architecture should define

### System-level assets

Potential examples:

`/AIOS/`

`/AIOS/Constitution/`

`/AIOS/Protocols/`

`/AIOS/Executive/`

`/AIOS/Templates/`

`/AIOS/Registry/`

Actual names remain open until this stage.

### Domain structure

Determine the minimum files every Director needs.

Possibilities:

Director identity/instructions

Current mission

State

Tasks

Execution/checkpoints

Decisions

Reviews

Domain knowledge

Specialist registry

### Registries

Master needs to know:

What domains exist?

Who owns them?

Where is their source of truth?

What missions are active?

Potentially a `DOMAIN_REGISTRY`.

### Source-of-truth mapping

Each important category should have authoritative ownership.

Do not copy the same state into five locations.

### Inheritance

Determine what every layer inherits.

For example:

Constitution
↓
Governance
↓
Protocols
↓
Director Template
↓
Domain-specific Director

### Archives

Historical material should remain available without contaminating current context.

---

## Architecture rule

Every file needs an answer to:

> Why does this need to exist independently?

If there is no clear answer, do not create it.

---

## Deliverable

An architecture specification plus the initial directory tree.

---

## Exit Gate

Every required piece of persistent information has:

* a location
* an owner
* a purpose
* a lifecycle

without unnecessary duplication.

---

# STEP 5 — EXECUTIVE

## Question

**How does Master Control think?**

## Purpose

Build the supervisory executive layer.

Master Control is not an all-purpose worker.

It is the system's executive function.

---

## Executive responsibilities

### Intake

Read new captures.

### Interpretation

Understand what the user actually wants.

### Routing

Determine ownership.

### Priority management

Understand relationships between active objectives.

### Mission issuance

Give Directors strategic objectives.

### Monitoring

Inspect:

* Director state
* meaningful checkpoints
* mission progress
* reviews
* blockers

### Alignment evaluation

Compare intended outcomes with observed progress.

### Intervention

Adjust direction where necessary.

### Cross-domain coordination

Example:

Career income goal and SevenTwoSites revenue strategy might interact.

Directors should not need full awareness of one another.

Master handles the intersection.

### System health

Detect:

* stale state
* abandoned missions
* duplicated work
* missing reporting
* repeated failures
* unnecessary complexity
* broken protocols

### Audit trail

Master should record material actions and their rationale.

---

## Executive must NOT

Micromanage every specialist action.

Duplicate Director strategy work.

Become the source of truth for every domain detail.

Constantly rewrite the architecture.

Treat activity as success.

Silently alter user objectives.

---

## Master self-review

The Executive should periodically evaluate itself:

Did I interpret the user correctly?

Did I route correctly?

Am I interfering too much?

Am I failing to intervene?

Am I creating unnecessary complexity?

Are priorities still accurate?

Did my interventions improve outcomes?

This creates the top AI feedback loop.

---

## Deliverables

Executive specification.

Master Control operating instructions.

Executive state model.

Executive review mechanism.

Audit mechanism.

Capture-processing mechanism.

---

## Exit Gate

A fresh Master Control session can inspect the system and correctly determine:

* who it is
* what is happening
* what matters
* what needs attention
* where work belongs

without requiring a full explanation from the user.

---

# STEP 6 — DIRECTOR TEMPLATE

## Question

**How does every domain work?**

## Purpose

Build the reusable management layer between Master Control and execution.

This is critical.

Master should not manage every specialist directly.

---

## Every Director should know

### Identity

What domain am I responsible for?

### Mission

What outcome has Executive assigned?

### Scope

What belongs inside my domain?

What does not?

### Authority

Which decisions can I make?

### Strategy

How will I pursue the mission?

### Current State

What is true?

### Capabilities

What specialists/tools can I use?

### Constraints

What must I avoid?

### Success Measures

How do I know the domain is progressing?

### Reporting

What must be visible to Executive?

---

## Director responsibilities

Understand mission.

Inspect domain state.

Create strategy.

Decompose strategy into projects/tasks.

Select specialists.

Delegate.

Monitor specialist checkpoints.

Review output.

Correct local drift.

Maintain authoritative domain state.

Escalate only when necessary.

Report mission-level progress upward.

---

## Important distinction

Master Control should not receive every specialist checkpoint.

That would recreate the scalability problem.

Instead:

Specialist
↓
Director

Director synthesizes.

Director
↓
Master

Master sees:

* meaningful progress
* strategic changes
* blockers
* mission risk
* important decisions
* aggregate state

Master may audit deeper logs when necessary.

---

## Deliverable

A generic reusable Director template.

Not yet tied to one domain.

---

## Exit Gate

We can instantiate a new domain Director largely by supplying domain-specific:

* scope
* source-of-truth map
* goals
* capabilities
* constraints

without redesigning the management system.

---

# STEP 7 — FIRST DIRECTOR

## Question

**Does the architecture actually work?**

## Purpose

Test AIOS on one real domain before scaling.

The first Director should be substantial enough to reveal problems but contained enough to debug.

AI Career is a likely candidate because its objective, information sources, research workflow, and outputs can be clearly tested.

The final choice will be made during implementation.

---

## What we test

User capture.

Master interpretation.

Mission creation.

Director initialization.

Strategy generation.

Task decomposition.

Specialist delegation.

Checkpoint recording.

Director review.

State updates.

Master review.

Drift detection.

Intervention.

Completion.

Fresh-session recovery.

---

## Use real work

Do not create toy tests like:

"Create a grocery list."

Use a genuine objective.

Example:

Build a repeatable pipeline capable of surfacing a defined number of genuinely suitable opportunities each day.

---

## Deliverable

One fully functioning domain implementation.

---

## Exit Gate

The domain can operate across multiple fresh sessions without loss of:

* purpose
* context
* state
* history
* ownership

and Master can understand its condition without manually reconstructing the work.

---

# STEP 8 — SIMULATION

## Question

**Can the whole system survive reality?**

## Purpose

Stress-test the design.

Testing should intentionally create conditions likely to break the architecture.

---

## Scenario types

### Normal progression

Mission executes successfully.

### Worker drift

Specialist solves the wrong problem.

### Director drift

Strategy stops serving mission.

### Stale context

An old assumption conflicts with newer state.

### Conflicting information

Two files disagree.

### Cross-domain dependency

A mission affects more than one Director.

### User priority change

Active mission suddenly becomes secondary.

### Failure

Approach produces poor outcomes.

### Session loss

Entire Claude session disappears.

Fresh session must recover.

### Partial completion

Work stops halfway through.

### Over-engineering

Agent proposes unnecessary infrastructure.

### Bad delegation

Task lacks sufficient context.

### Information overload

Specialist receives excessive context.

---

## Deliverable

Simulation findings.

Failure catalogue.

Protocol violations.

Architecture weaknesses.

---

## Exit Gate

Major failure modes have been identified and the system handles them predictably enough to proceed.

---

# STEP 9 — REFINEMENT

## Question

**What did we learn?**

## Purpose

Improve the system based on evidence.

This phase specifically resists feature creep.

Do not respond to testing by adding endless new components.

---

## Actions

Remove unnecessary files.

Simplify protocols.

Fix unclear ownership.

Strengthen weak handoffs.

Improve state representation.

Improve context selection.

Reduce logging noise.

Improve drift detection.

Improve initialization.

Improve review thresholds.

Resolve duplicated knowledge.

Document important design decisions.

---

## Core rule

During refinement:

**No feature earns permanence merely because it is interesting.**

It must solve an observed problem.

---

## Deliverable

AIOS v1 architecture.

Stable protocol set.

Documented lessons.

Known limitations.

---

## Exit Gate

The first domain works reliably enough that the architecture can be repeated without major redesign.

---

# STEP 10 — SCALE

## Question

**Can this become the operating system?**

## Purpose

Expand the proven architecture gradually.

---

## Scale domains

Introduce additional Directors.

Likely future candidates may include domains such as:

* SevenTwoSites
* personal development / Evolution
* additional operating areas that genuinely justify independent ownership

Do not create Directors simply because a folder exists.

A Director should represent an enduring domain requiring independent strategic management.

---

## Add Specialists carefully

Specialists should exist when:

* recurring work requires specialization
* context isolation improves performance
* independent execution is useful
* the workload justifies the abstraction

Otherwise the Director may execute directly.

---

## Introduce automation

Only after manual protocols are proven.

Possible later automation:

Capture watchers.

Mission generation.

Task queues.

Checkpoint processors.

Automated status summaries.

Scheduled Master audits.

Git hooks.

Claude Code hooks.

Session initialization commands.

Agent launching/orchestration where technically possible.

Monitoring dashboards.

Do not automate ambiguity.

---

## Model independence

Over time, specialist implementation may use:

* Claude Code
* Codex
* other models
* scripts
* APIs
* deterministic software

AIOS should define the contract.

The worker implementation can change.

---

## Deliverable

Multi-domain AIOS.

---

## Exit Gate

Not applicable in the same sense.

Scale becomes an ongoing lifecycle.

---

# 5. THE THREE FEEDBACK LOOPS

The architecture depends on three nested feedback systems.

## Loop 1 — Specialist

Question:

**Does my execution satisfy the assigned task?**

Specialist observes its own execution and records meaningful checkpoints.

---

## Loop 2 — Director

Question:

**Does specialist execution advance my domain strategy and mission?**

Director reviews specialists and corrects local execution.

---

## Loop 3 — Executive

Question:

**Does the Director's strategy and state remain aligned with the user's intended outcome?**

Executive monitors Directors rather than individual operations by default.

---

## Loop 4 — User

Although not an autonomous loop, the final authority is:

**Is Executive still correctly representing what I want?**

The user supervises Master Control.

Master Control supervises Directors.

Directors supervise Specialists.

This is the intended scalability mechanism.

---

# 6. OBSERVABILITY MODEL

AIOS must make work inspectable without creating excessive documentation.

Therefore execution should produce **meaningful checkpoints**, not exhaustive activity logs.

Record when there is:

* new evidence
* a state change
* a decision
* a strategy change
* completion of a meaningful stage
* a blocker
* a failure
* an unexpected result
* a relevant lesson

Do not record every file open, shell command, search click, or trivial action unless debugging requires it.

The higher the layer, the greater the compression.

Specialist:

detailed checkpoints

↓

Director:

strategic summary

↓

Executive:

mission-level state

↓

User:

only material understanding/decisions

---

# 7. SOURCE-OF-TRUTH MODEL

One of the most important architectural principles:

**Do not teach every agent everything. Teach every agent where authoritative truth lives.**

Example:

Instead of Master permanently storing:

"The user's CV contains X."

Master should know:

"The authoritative candidate profile/CV is located here."

Instead of copying SevenTwoSites strategy into Executive files:

Master knows:

"SevenTwoSites Director owns this domain; its current state is here."

This minimizes stale duplicated context.

---

# 8. ANTI-DRIFT DESIGN

AIOS itself can drift during construction.

Therefore this blueprint is a project control document.

Future chats should not casually redefine the roadmap.

Changes are allowed.

But material changes require:

1. identify the proposed change
2. explain why
3. identify which existing assumption/design it supersedes
4. assess downstream consequences
5. deliberately update the canonical specification
6. record the decision

This distinction matters:

**Evolution is deliberate. Drift is accidental.**

AIOS should evolve.

AIOS should not silently drift.

---

# 9. PROJECT DEVELOPMENT MODEL

AIOS itself should be treated as a software/system-design project.

It should eventually live in Git.

Expected practices:

* GitHub repository
* version control
* meaningful commits
* architectural documentation
* decision records
* changelog/versioning
* issues/tasks where useful
* tagged milestones eventually
* README suitable for technical explanation
* diagrams
* examples
* tests/simulations
* documented known limitations

This serves three purposes:

### Preservation

The project cannot simply disappear.

### Engineering Discipline

Changes become inspectable and reversible.

### Portfolio Value

The finished system can demonstrate:

* agent architecture
* prompt/context engineering
* multi-agent orchestration
* state management
* human-in-the-loop design
* observability
* governance
* AI systems thinking
* automation
* software architecture
* iterative testing

Any future commercialisation is secondary.

The immediate goal is building the system properly.

---

# 10. LEARNING REQUIREMENT

The project should not merely produce a working system.

The user should understand how it works.

Therefore important implementation stages should explain:

* what we are building
* why it exists
* what problem it solves
* alternatives
* trade-offs
* why a design was chosen
* how to diagnose failure
* how to reproduce the pattern elsewhere

AI assistance should accelerate understanding, not replace it.

The desired end state is that the user can reason about AIOS architecture independently rather than requiring the original chat to reconstruct it.

---

# 11. AIOS PROJECT CONTINUITY

This project will span multiple conversations and AI sessions.

Therefore continuity cannot depend on conversational context.

We need a project-level recovery mechanism.

Eventually, a fresh session should be able to read a small set of canonical files and answer:

1. What are we building?
2. Why?
3. What architecture have we agreed on?
4. What stage are we currently at?
5. What has already been completed?
6. What decisions have been made?
7. What remains unresolved?
8. What should happen next?
9. What must not be changed casually?
10. Where can deeper information be found?

This is a requirement of the AIOS project itself before we begin implementing AIOS for other domains.

---

# 12. CURRENT PROJECT STATE

At the creation of this blueprint:

## Completed conceptually

Core AIOS vision.

Layered ownership model.

User → Executive → Director → Specialist hierarchy.

Closed-loop monitoring concept.

Persistent-state principle.

Meaningful checkpoint concept.

Master supervision rather than Master micromanagement.

Director intermediary layer.

Need for Constitution.

Need for Governance.

Need for shared Language.

Need for Protocols.

Need for filesystem Architecture.

Need for Git/version-controlled development.

Need for project continuity across chats.

Need to teach the user the architecture during development.

---

## Not yet completed

Constitution.

Governance.

Language definitions.

Formal protocols.

Filesystem architecture.

Executive specification.

Director template.

First Director.

Simulation framework.

Repository structure.

GitHub repository.

Project anti-drift mechanism.

Cross-chat continuity system.

Implementation.

---

# 13. IMMEDIATE NEXT ACTION

Do NOT begin Step 0 yet.

Before Step 0, establish the **AIOS project's own development environment and continuity system**.

Specifically:

1. Establish how this ChatGPT project preserves canonical decisions across future conversations.
2. Create the AIOS project repository / working directory.
3. Establish version control.
4. Create the minimal project documentation required to prevent drift.
5. Store this blueprint as the canonical roadmap.
6. Define how future chats/sessions initialize into the AIOS project.
7. Define how project decisions and progress are persisted.
8. Only then begin Step 0 — Constitution.

This is effectively:

**PRE-STEP / PROJECT BOOTSTRAP**

Question:

> How do we ensure the process of building AIOS does not itself suffer from the exact problems AIOS is being designed to solve?

Solve that first.

Then build AIOS.

---

# 14. BUILD SEQUENCE — CANONICAL

PRE-STEP — Project Bootstrap
**How do we prevent AIOS development itself from drifting?**

↓

STEP 0 — Constitution
**What is AIOS?**

↓

STEP 1 — Governance
**What is allowed?**

↓

STEP 2 — Language
**What do our words mean?**

↓

STEP 3 — Protocols
**How does information move?**

↓

STEP 4 — Architecture
**What exists?**

↓

STEP 5 — Executive
**How does Master Control think?**

↓

STEP 6 — Director Template
**How does every domain work?**

↓

STEP 7 — First Director
**Does the architecture actually work?**

↓

STEP 8 — Simulation
**Can the whole system survive reality?**

↓

STEP 9 — Refinement
**What did we learn?**

↓

STEP 10 — Scale
**Can this become the operating system?**

---

# 15. FINAL NORTH STAR

USER OWNS VISION.

EXECUTIVE OWNS ALIGNMENT.

DIRECTORS OWN STRATEGY.

SPECIALISTS OWN EXECUTION.

PROTOCOLS GOVERN BEHAVIOUR.

KNOWLEDGE LIVES IN PERSISTENT STORAGE.

AIOS should reduce the amount of coordination the user personally performs while increasing the user's visibility and control over the system.

The objective is not maximum autonomy.

The objective is:

**maximum useful leverage with preserved human control, persistent understanding, observable execution, and recoverable state.**

We are not building prompts.

We are engineering an operating system.
