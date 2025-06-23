# OperatingSystems
Welcome to the portfolio repository for the "Draw It or Lose It" web-based game service. Below you will find reflections on the project deliverable, demonstrating my process and insights as a software designer.

1. Client and Requirements

Who was the client? What type of software did they want you to design?

The client, The Gaming Room, originally offered a mobile-only Android app called Draw It or Lose It. They requested a web-based, multi-platform redesign of their game service so that users on desktop browsers, mobile browsers, and future console platforms (e.g., Xbox, PlayStation) could seamlessly participate in real-time drawing-and-guessing gameplay.

2. Strengths in Documentation

What did you do particularly well in developing this documentation?

Clarity and Consistency: I used an abstract Entity base class to standardize common fields (id, name) and behaviors across domain objects (Game, Team, Player), which makes the UML diagram and code samples easy to follow.

Design Patterns: I clearly articulated where and why I applied the Singleton (for centralized game state) and Iterator (to enforce unique naming) patterns, enhancing maintainability and preventing runtime errors.

Standards and Naming: I adhered to industry-standard naming conventions and included in-line documentation guidelines, promoting future team collaboration and code readability.

3. Benefits of the Design-Document Process

What about the process of working through a design document did you find helpful when developing the code?

Holistic Viewpoint: Sketching the System Architecture View and Domain Model diagrams upfront enabled me to anticipate integration points and dependencies before writing a single line of code.

Constraint Awareness: Listing Design Constraints (e.g., stateless front-ends, thread safety, unique naming) guided API signatures and influenced data structures, which reduced refactoring during implementation.

Evaluation Matrix: Comparing Linux, macOS, Windows, and mobile platforms in a feature matrix clarified deployment trade‑offs and ultimately led to a stronger recommendation for Ubuntu Server.

4. One Revision for Improvement

If you could choose one part of your work on these documents to revise, what would you pick? How would you improve it?

I would refine the Requirements section by translating the client’s high‑level goals (e.g., “support 1,000 concurrent users”) into measurable performance criteria (e.g., “average response time < 200ms under 1,000 WebSocket connections”). Adding these metrics would make acceptance testing more objective.

5. Interpreting User Needs

How did you interpret the user’s needs and implement them into your software design? Why is it so important to consider the user’s needs when designing?

I engaged with the client’s core requirement—real‑time, multiplayer drawing challenges—and surfaced two critical user needs:

Consistency across platforms, so players see the same game state.

Performance under load, to prevent lag during timed rounds.

I translated these into design choices such as a single in-memory GameService (to avoid divergent state) and a microservices architecture recommendation (for horizontal scalability). Centering the design around the user experience ensures we deliver a polished, reliable product that meets both business goals and player expectations.

6. Future Design Strategies

How did you approach designing software? What techniques or strategies would you use in the future to analyze and design a similar software application?

Use-Case Modeling: I would start with detailed user stories and sequence diagrams to capture every interaction, which helps uncover edge cases early (e.g., reconnects, permission errors).

Prototyping: Building a rapid UI mockup (using wireframes or a lightweight framework) allows stakeholders to validate workflows before deep backend work begins.

Iterative Refinement: I plan to adopt an Agile approach with short design spikes and feedback loops, so that each increment of the design is validated by both developers and end users.

Performance Benchmarks: Integrating small load tests alongside design documentation will keep nonfunctional requirements top-of-mind throughout development.
