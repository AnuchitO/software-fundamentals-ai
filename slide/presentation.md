# Software Fundamentals Matter More Than Ever

## Slide 1: Title Slide
**Title:** Software Fundamentals Matter More Than Ever
**Presenter:** Matt Pocock
**Context:** Introducing the course "Claude Code for real engineers" and the new paradigm of AI coding.

**Speaker Notes:**
Welcome to this presentation on software fundamentals in the age of AI. Today we'll explore why foundational software engineering principles are actually more important than ever when working with AI coding assistants. This presentation stems from the "Claude Code for real engineers" course and discusses how traditional software engineering practices enhance our ability to work effectively with AI.

---

## Slide 2: The "Specs to Code" Movement
**Content:**
- Concept: Write a specification → Use AI to turn it into code → If there is a problem, change the spec, not the code → Run the compiler again
- The Problem: Ignoring the code leads to "v-coding" (voodoo coding) where repeated runs produce increasingly worse code and eventually "garbage"

**Speaker Notes:**
The "specs to code" movement suggests a hands-off approach where humans write specifications and let AI handle the implementation. The philosophy is to treat code generation like compilation - if there's an issue, adjust the specification rather than fixing the code directly. However, this approach has a fundamental flaw: ignoring the quality and structure of the generated code leads to degradation over time. When we don't review and maintain the code produced by AI, it becomes increasingly difficult to understand and modify, eventually becoming unusable "garbage".

---

## Slide 3: Software Entropy and Complexity
**Content:**
- Definition of Bad Code: Anything in the structure of a system that makes it hard to understand and modify
- Software Entropy: The tendency for systems to drift toward disaster and collapse if changes are made without considering the design of the whole system
- Thesis: Code is NOT cheap. Bad code is the most expensive it has ever been because it prevents you from taking advantage of AI's bounty

**Speaker Notes:**
Software entropy refers to the natural tendency of systems to degrade over time when changes aren't made with consideration for the overall design. John Ousterhout defines complexity as anything in the structure of a system that makes it hard to understand and modify. In the AI era, bad code is particularly costly because AI tools perform best in well-structured, clean codebases. Poor code quality creates a barrier to leveraging AI's full potential, making it impossible to benefit from automation and assistance.

---

## Slide 4: Tip #1 - Reach a Shared Design Concept
**Content:**
- Failure Mode: "The AI didn't do what I wanted"
- The Skill: "Grill Me"
  - "Interview me relentlessly about every aspect of this plan until we reach a shared understanding."
  - Walk down the "design tree" to resolve dependencies one by one
- Goal: Reach a shared "design concept" (the invisible theory of what you're building) before creating assets like PRDs or code

**Speaker Notes:**
Communication failures with AI often stem from mismatched expectations. The "Grill Me" technique involves thoroughly questioning every aspect of a plan until there's complete clarity. This means walking through the design tree, resolving dependencies one by one, and ensuring both you and the AI have the same understanding. The goal is to establish a shared design concept - the invisible theory of what you're building - before moving to implementation.

---

## Slide 5: Tip #2 - Ubiquitous Language
**Content:**
- Failure Mode: "The AI is way too verbose"
- Concept (from DDD): Ubiquitous Language
- Implementation:
  - Create a markdown file of shared terms derived from the domain model
  - Use these terms in code, conversations with AI, and with domain experts
- Benefit: Improves planning traces and keeps implementation aligned with the plan

**Speaker Notes:**
Derived from Domain-Driven Design, ubiquitous language ensures consistent terminology across the team, code, and interactions with AI. Create a shared glossary document that defines terms from your domain model. Using consistent language improves communication with AI, reduces verbosity, and keeps implementation aligned with your plans. This shared vocabulary becomes crucial when directing AI to implement specific features.

---

## Slide 6: Tip #3 - TDD (Test-Driven Development)
**Content:**
- Failure Mode: "It just doesn't work"
- The Speed Limit: "The rate of feedback is your speed limit."
- The Strategy: Don't "outrun your headlights" by producing too much code at once
- Practice: Use TDD to force the AI to take small, deliberate steps: Create a test → Make it pass → Refactor

**Speaker Notes:**
AI can sometimes produce large amounts of code without verification, leading to non-functional results. TDD provides the necessary feedback loops to ensure functionality. The principle "the rate of feedback is your speed limit" means you shouldn't produce more code than you can verify. Use TDD to constrain AI to small, verifiable steps: write a test, make it pass, then refactor. This prevents the AI from "outrunning its headlights" and creating unverifiable code.

---

## Slide 7: Comparison: Deep vs. Shallow Modules
**Content:**
- Shallow Modules:
  - Small functionality hidden behind a complex interface
  - Visual: A "ton of different tiny little blobs" that are hard for AI to navigate and explore
- Deep Modules:
  - Lots of functionality hidden behind a simple interface
  - Visual: Code structured inside clear boundaries with well-designed interfaces
- Goal: Turn shallow modules into deep modules to create a "testable codebase"

**Speaker Notes:**
Shallow modules have complex interfaces relative to their functionality, creating many small, interconnected parts that are difficult for both humans and AI to navigate. Deep modules provide lots of functionality through simple, well-defined interfaces. In the AI era, deep modules are preferable because they provide clear boundaries and interfaces that AI can understand and work with more effectively. Transforming shallow modules into deep ones creates a more testable and maintainable codebase.

---

## Slide 8: Tip #4 - Improve Codebase Architecture
**Content:**
- Process: Explore the codebase, find related code, and wrap it in a deep module
- Benefit: Simplifies the "map" of the application for both the human developer and the AI

**Speaker Notes:**
Continuously improve your codebase by identifying related functionality and encapsulating it in well-designed modules. This process simplifies the overall architecture, making it easier for both human developers and AI assistants to understand and navigate the codebase. Good architecture acts as a roadmap that guides both human thought processes and AI implementation decisions.

---

## Slide 9: Tip #5 - Design the Interface, Delegate the Implementation
**Content:**
- Strategy: Treat deep modules as "gray boxes"
- The Human Role: Design the interface and verify it from the outside via tests
- The AI Role: Handle the complex implementation inside the "big blob"
- Result: Saves "brain power" by reducing the amount of implementation details a developer needs to hold in mind

**Speaker Notes:**
As a human developer, focus on designing clean interfaces and verifying their correctness through tests. Let AI handle the complex implementation details within modules. This division of labor allows humans to concentrate on architecture and design while AI handles the detailed implementation. This approach conserves cognitive resources by reducing the amount of detail humans need to manage simultaneously.

---

## Slide 10: Conclusion - Strategic vs. Tactical
**Content:**
- Core Message: Invest in the design of the system every day
- The Relationship:
  - AI: The "Tactical Programmer" (Sergeant on the ground making code changes)
  - Human (You): The "Strategic Level" thinker
- Final Word: Software fundamentals are what allow you to make a high impact in the AI age

**Speaker Notes:**
In the AI era, the relationship between humans and machines shifts to a strategic-tactical dynamic. Humans operate at the strategic level, focusing on design, architecture, and system-wide decisions. AI serves as the tactical programmer, implementing specific changes and handling detailed work. Success in this new paradigm requires a strong foundation in software fundamentals - these principles are what enable us to leverage AI effectively and create high-impact solutions.