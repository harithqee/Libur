
![App Banner](./assets/banner.png)

# Libur

**Libur** ("holiday" / "day off" in Malay & Indonesian) is a collaborative trip-planning app that combines AI-generated plans, community-shared travel plans and articles, and group decision-making where every voice is heard — group chat, in-app voting, and a shared wishlist — so that planning a trip with friends stops being a scattered mess spread across different apps, and everyone's wishes actually get fulfilled.

---

## Ideation

### Problem & Idea Origin

Group trips constantly fall apart at the planning stage because itineraries and ideas end up scattered across half a dozen different apps. Furthermore, as our own real-life experiences prove, many of us are simply too lazy to take on the tedious burden of building a structured schedule from scratch. This sparked a realization: instead of forcing users to create a plan from zero, why not let them easily grab, adapt, and engage with proven itineraries already used by the community? To solve this, Libur blends AI-generated plans, community-shared trips, travel articles (inspired by Substack), and in-chat voting into one seamless platform — letting your group experience a perfectly curated vacation without the mental heavy lifting. On top of that, group members can drop their individual must-dos into a shared wishlist, and the AI automatically weaves them together into an itinerary.

- **AI-Based Plan** — AI suggestions (place, accommodation, transport).

- **Article + Plan duality** — users can post either inspirational travel articles *or* structured plans, and view/browse both through the same "View plan/article" entry point, blending inspiration and execution in one feed.

- **Voting** — ensuring every voice is heard and keeping the group happy with transparent, democratic decision-making built right into the discussion.

- **Collaborative AI Group Plan** — group members drop their individual must-dos into a shared wishlist, and the AI automatically weaves them together into a balanced master itinerary, ensuring everyone's wishes come true without the scheduling headaches.

### Visual Diagrams & Mindmaps
The core feature set was mapped as a UML **use-case diagram**, evolved across three passes:

**Latest use-case diagram**

![Latest use-case diagram](./assets/usecase-diagram-final.png)

### Iteration & Idea Evolution
Libur went through a documented pivot between its hand-drawn draft and the final digital use-case diagram:

**Early hand-drawn draft**

![Draft use-case diagram, hand-drawn](./assets/usecase-diagram-draft.jpg)



**Second draft**

![Second use-case diagram, hand-drawn](./assets/usecase-diagram-second.png)

| Draft | Final | What changed & why |
|---|---|---|
| *Vote plan* listed as its own standalone use case | *Vote plan* included into **Group chat**  | Voting only makes sense in the context of a group discussion, so it was merged into the chat flow instead of being a separate, disconnected action. |
| *AI-Based Plan* listed as its own standalone use case | *AI-Based Plan* included into **Pick plan** | The team realized AI generation isn't a feature on its own — it's the mechanism *behind* plan selection, so the relationship was formalized as an include rather than a floating idea. |

**Latest draft**

![Second use-case diagram, hand-drawn](./assets/usecase-diagram-third.png)

| Draft | Final | What changed & why |
|---|---|---|
| *Shared Wishlist* wasn't listed | *Shared Wishlist* is included into **Group chat**  | The idea came out of nowhere mid-build — not a planned pivot, just a spontaneous "what if everyone could drop their must-dos in and let the AI merge them" moment that got added as a second <<include>> off Group chat. |

### From use case to UI/UX Prototype

The final use-case diagram wasn't just documentation — it was used directly as the reference for building out the UI/UX mockups and screen flow, shown on the ideation board below:

![Ideation board](./assets/ideation-board.png)

**AI-Based Plan UI/UX**
![AI-Based Plan UI/UX](./assets/Mockup%20Page.png)

**Article + Plan duality UI/UX**
![Article + Plan duality UI/UX](./assets/Mockup%20Page%20(1).png)

**Voting UI/UX**
![Voting UI/UX](./assets/Mockup%20Page%20(2).png)

**Collaborative AI Group Plan UI/UX**
![Collaborative AI Group Plan UI/UX](./assets/Mockup%20Page%20(3).png)


During the UI/UX design phase, we realized that keeping users in one cohesive app meant solving the friction of execution, not just planning. To ensure the entire trip lifecycle happens in one place, we are considering to expand our feature set to navigation and hotel booking.

![New Use-case Consideration](./assets/consideration%201.0.png)



