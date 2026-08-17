# Project Setup Roadmap

This roadmap defines the planning work that should be completed before TripCraft application implementation begins. These documents should remain concise, useful, and current as the project evolves.

## Pre-Development Principles

1. Do not begin implementation until the core product and architecture decisions exist in writing.
2. `README.md` is the project's front door, not the full specification.
3. `PRODUCT.md` defines the problem, product vision, target users, value proposition, product principles, major capabilities, non-goals, and future vision.
4. `REQUIREMENTS.md` converts product behavior into explicit, testable functional and non-functional requirements.
5. `MVP.md` clearly separates:
   - Required for V1
   - Explicitly not required for V1
   - Possible future features
6. `USER_FLOWS.md` describes important user workflows step-by-step before UI or implementation decisions are made.
7. `DOMAIN_MODEL.md` defines the conceptual business and domain entities before translating them into database tables.
8. `ARCHITECTURE.md` documents technology choices, application boundaries, client/server responsibilities, data access, authentication, authorization, validation, error handling, state management, external integrations, AI boundaries, deployment, and architectural constraints.
9. `DATA_MODEL.md` translates the domain model into persistent storage, relationships, fields, and invariants.
10. `API_DESIGN.md` defines API and server-function conventions, mutations, validation, authentication, IDs, dates, errors, and trust boundaries.
11. `AI_FEATURES.md` explicitly defines each AI capability, its inputs, structured output, validation, failure behavior, user confirmation, stored data, and security boundaries.
12. `UI_UX.md` documents major screens, purpose, actions, navigation, loading, error and empty states, accessibility, and responsive behavior.
13. `SECURITY.md` documents authentication, authorization, ownership, server/client trust boundaries, secrets, external APIs, AI validation, rate limiting, sensitive data, and logging.
14. `TESTING.md` defines unit, integration, and end-to-end testing expectations and the definition of done.
15. `DECISIONS.md` records meaningful product and technical decisions along with reasoning and alternatives considered.
16. Use architecture decision records for significant architectural decisions that would be expensive to reverse.
17. `IMPLEMENTATION_PLAN.md` breaks work into milestone, epic, feature, and small task.
18. `AGENTS.md` is Codex's project operating manual. It should summarize and enforce decisions that already exist rather than invent architecture.
19. Consider more specific nested `AGENTS.md` files later when portions of the repository need specialized instructions.
20. Establish coding conventions deliberately before AI-generated code accidentally establishes them.
21. Choose the technology stack deliberately and record the reasons for those choices.
22. Identify external integrations early and distinguish MVP integrations from future possibilities.
23. Treat dates, times, time zones, daylight saving time, travel across time zones, and multi-destination trips as first-class architectural concerns.
24. Design the itinerary domain carefully before creating database schemas. Consider how activities, accommodations, transportation, reservations, and multi-day items relate to an itinerary.
25. Define a strict AI trust boundary. The model proposes structured actions; the application validates them; users approve where appropriate; application code owns persistent state.
26. Maintain a glossary so concepts such as Trip, Destination, Place, Activity, Reservation, Booking, Itinerary Item, and Travel Segment are used consistently.
27. Establish quality gates before implementation. Done should include relevant tests, type checking, linting, security and authorization review, documentation updates, and manual diff review.
28. Keep the Git workflow simple initially: small branches, small changes, manual diff review, and intentional commits.
29. Later, use GitHub issues or equivalent tasks as bounded executable work units referencing requirements and acceptance criteria.
30. Do not allow documentation to become ceremonial or block development. Documents should be concise living project memory and evolve with the software.

## Planned Documentation Order

1. PRODUCT.md
2. MVP.md
3. USER_FLOWS.md
4. DOMAIN_MODEL.md
5. REQUIREMENTS.md
6. ARCHITECTURE.md
7. DATA_MODEL.md
8. AI_FEATURES.md
9. UI_UX.md
10. SECURITY.md and TESTING.md
11. DECISIONS.md / ADRs
12. IMPLEMENTATION_PLAN.md
13. Finalize AGENTS.md
14. Begin application implementation
