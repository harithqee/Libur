# Libur

**Libur** ("holiday" / "day off" in Malay & Indonesian) is a collaborative trip-planning app that combines AI-generated itineraries, community-shared travel plans and articles, and group decision-making (group chat + in-app voting) so that planning a trip with friends stops being a scattered mess of screenshots and group-chat chaos.

> 📝 *Sections marked with `> [FILL IN]` are facts only the team can confirm — tech stack, mentor names/quotes, target metrics, timeline. Everything else below is drawn directly from the use-case diagrams and ideation board.*

---

## 1. Ideation

### 1.1 Problem & Idea Origin
> [FILL IN — 2–3 sentences: what problem/challenge statement sparked Libur? e.g. "Group trips fall apart at the planning stage because itinerary ideas, articles, and votes live in five different apps."]

### 1.2 Visual Diagrams & Mindmaps
The core feature set was mapped as a UML **use-case diagram**, evolved across two passes:

**Final digital use-case diagram**

![Final use-case diagram](./assets/usecase-diagram-final.jpg)

The diagram centers on a single **User** actor with five primary use cases — *View plan/article*, *Post plan*, *Pick plan*, *Post article*, and *Group chat* — with two `<<include>>` relationships showing how AI and social features are woven into the core flows rather than bolted on:
- **Pick plan** `<<include>>` **AI-Based Plan** — plan selection is powered by AI-generated recommendations.
- **Group chat** `<<include>>` **Vote plan** — group decision-making happens inside the chat itself.

This was paired with a broader **feature/screen mindmap** (the ideation board below) mapping the full user flow from onboarding through to group voting, so the use-case diagram and the screen-level mindmap validate each other.

### 1.3 Iteration & Idea Evolution
Libur went through a documented pivot between its hand-drawn draft and the final digital use-case diagram:

**Early hand-drawn draft**

![Draft use-case diagram, hand-drawn](./assets/usecase-diagram-draft.jpg)

| Draft | Final | What changed & why |
|---|---|---|
| *Vote plan* listed as its own standalone use case | *Vote plan* folded into **Group chat** via `<<include>>` | Voting only makes sense in the context of a group discussion, so it was merged into the chat flow instead of being a separate, disconnected action. |
| *AI-Based Plan* drawn as an isolated bubble with a manual note *"(Place, Accommodation, Transport)"* | *AI-Based Plan* connected to **Pick plan** via `<<include>>` | The team realized AI generation isn't a feature on its own — it's the mechanism *behind* plan selection, so the relationship was formalized as an include rather than a floating idea. |
| No explicit relationships drawn between use cases | Two `<<include>>` dependencies added | Moving from a flat list of features to a diagram with real relationships forced the team to think about *how* features connect, not just what they are. |

This shows a clear pivot from "AI and voting as separate add-on features" → "AI and voting as embedded parts of the core plan-picking and chat flows."

### 1.4 Mentor Consultation & Feedback Integration
> [FILL IN — Who was consulted? What specific feedback was given, and what did the team change as a result? e.g. "Mentor X flagged that a standalone 'Vote plan' bubble was redundant with chat — this directly led to the <<include>> merge documented above."]

### 1.5 Breadth of Exploration
Before settling on the current five-use-case structure, the team explored and mapped a wide range of directions on the ideation board, including:
- **Onboarding & discovery** — splash screen, "Explore" feed, article-detail views ("A Trip That I Won't Forget")
- **Multiple AI-planning variants** — at least 8 distinct AI-based planner screen concepts were sketched and compared (flight picking, similar-trip suggestions, destination input, itinerary builder), narrowing down to one consistent "AI Trip Planner" pattern
- **Social/collaborative features** — 1:1 chat, in-context group chat, itinerary-sharing within chat
- **Navigation** — an in-app map view for itinerary stops, explored as a possible addition beyond the core five use cases

![Ideation board](./assets/ideation-board.png)

Several directions (e.g., a plain map/navigation screen, multiple redundant AI-planner layouts) were considered and consciously *not* carried into the final use-case diagram, showing comparison and rationale rather than "first idea wins."

---

## 2. Creativity & Novelty

### 2.1 Originality
Libur isn't a generic itinerary app or a generic group-chat app — it's positioned at the intersection of both: **AI-generated plans that are meant to be argued over and voted on by a group**, not just accepted by a solo user.

### 2.2 Novel Features / Twists
- **AI-Based Plan as an included sub-process of Pick Plan** — AI suggestions (place, accommodation, transport) are generated *inline* with the plan-picking flow, not as a separate "chatbot" tab.
- **Voting embedded inside Group Chat** — instead of a separate polls feature, the group votes on plans in the same thread they're discussing them, removing app-switching friction.
- **Article + Plan duality** — users can post either inspirational travel articles *or* structured plans, and view/browse both through the same "View plan/article" entry point, blending inspiration and execution in one feed.

### 2.3 Differentiation from Existing Solutions
> [FILL IN — name 1–2 existing apps/tools (e.g. TripIt, Wanderlog, a shared Notion doc + group chat combo) and explain concretely why Libur's include-relationship model (AI embedded in plan-picking, voting embedded in chat) is different/better.]

---

## 3. Feasibility

### 3.1 Technical Viability & Tech Stack
> [FILL IN — frontend framework, backend, database, which AI model/API powers "AI-Based Plan," auth, hosting. Note any known unknowns/risks.]

### 3.2 Planning & Scope Realism
The use-case diagram intentionally scopes the MVP to **five core use cases** (View plan/article, Post plan, Pick plan, Post article, Group chat) plus two supporting include-relationships (AI-Based Plan, Vote plan) — rather than the wider set of screens explored on the ideation board (e.g., standalone navigation/map). This is a deliberate scope cut to keep the build achievable.

> [FILL IN — build plan / milestones / what's built vs. what's mocked for the prototype.]

### 3.3 Resource & Time Awareness
> [FILL IN — team size/skills, timeline, and where the biggest time risk is (likely the AI-plan generation feature).]

---

## 4. Design

### 4.1 Visual Consistency
Mockups follow a consistent iPhone-frame, card-based layout across all screens (Explore feed, Article detail, Pick Plan, AI Trip Planner, Group Chat), using a repeated bottom nav bar and card component throughout — visible in the ideation board.

### 4.2 Usability & UX
The flow is designed to minimize app-switching: from Explore → Article/Plan detail → Pick Plan (with AI suggestions inline) → share into an itinerary → discuss and vote in Group Chat, all without leaving the app.

### 4.3 Mockup Completeness
Current mockups cover the **core flow end-to-end**:
1. Splash → Explore feed
2. Article / Plan detail view
3. Pick Plan (AI-assisted)
4. Make/Share Itinerary
5. Group Chat with itinerary card + voting
6. AI Trip Planner variants (destination input → generated plan)
7. Navigation/map view (exploratory, not in final use-case scope)

---

## 5. Impact

### 5.1 Understanding the Problem Context
> [FILL IN — what's the real-world pain point? e.g. group trip planning fragmentation, decision fatigue, time lost comparing options across apps.]

### 5.2 Target Group Alignment
> [FILL IN — who specifically is this for? e.g. friend groups aged 18–30 planning domestic trips together, first-time group travelers, etc.]

### 5.3 Effectiveness of the Solution
By embedding AI recommendations directly into the plan-picking step and voting directly into group chat, Libur removes two common friction points in group trip planning: **decision paralysis** (too many options, no easy way to narrow down) and **coordination overhead** (plans and decisions scattered across separate apps).

> [FILL IN — any before/after comparison, user testing feedback, or expected time-saved metric.]

### 5.4 Reach & Scalability
> [FILL IN — path to more users/markets, e.g. localization beyond Malay/Indonesian-speaking users, expansion from friend-group trips to family/corporate trip planning, etc.]

---

## Appendix: Assets
- `assets/usecase-diagram-draft.jpg` — early hand-drawn use-case sketch
- `assets/usecase-diagram-final.jpg` — final digital use-case diagram
- `assets/ideation-board.png` — full ideation/mockup board (screens, motivation, feature groupings)