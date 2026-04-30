---
theme: seriph
background: https://cover.sli.dev
title: Software Fundamentals Matter More Than Ever
info: |
  ## Software Fundamentals Matter More Than Ever
  Presentation by Matt Pocock
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable Comark Syntax: https://comark.dev/syntax/markdown
comark: true
# duration of the presentation
duration: 35min
---

# Software Fundamentals Matter More Than Ever

### Matt Pocock

<span class="text-xl opacity-70">Presentation slides for real engineers in the age of AI</span>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn opacity-20 !border-none !bg-transparent !fill-white !text-white">
    <carbon:logo-github />
  </a>
</div>

<!--
Welcome to this presentation on software fundamentals in the age of AI.
Today we'll explore why foundational software engineering principles are actually more important than ever when working with AI coding assistants.
This presentation stems from the "Claude Code for real engineers" course and discusses how traditional software engineering practices enhance our ability to work effectively with AI.
-->

---
transition: slide-left
---

# The "Specs to Code" Movement

<div class="grid grid-cols-2 gap-4 mt-6">
  <div class="bg-gray-800/20 p-4 rounded-lg backdrop-blur-sm">
    <h3 class="text-xl font-bold mb-3 text-teal-300">The Approach</h3>
    <ol class="list-decimal pl-4 space-y-2 text-base">
      <li>Write a specification</li>
      <li>Use AI to turn it into code</li>
      <li>If there's a problem, change the spec, not the code</li>
      <li>Run the compiler again</li>
    </ol>
  </div>

  <div class="bg-red-800/20 p-4 rounded-lg backdrop-blur-sm">
    <h3 class="text-xl font-bold mb-3 text-red-300">The Problem</h3>
    <p class="text-base">Ignoring the code leads to <strong class="text-red-200">"v-coding"</strong> (voodoo coding) where repeated runs produce increasingly worse code and eventually "garbage"</p>
  </div>
</div>

<!--
The "specs to code" movement suggests a hands-off approach where humans write specifications and let AI handle the implementation.
The philosophy is to treat code generation like compilation - if there's an issue, adjust the specification rather than fixing the code directly.
However, this approach has a fundamental flaw: ignoring the quality and structure of the generated code leads to degradation over time.
When we don't review and maintain the code produced by AI, it becomes increasingly difficult to understand and modify, eventually becoming unusable "garbage".
-->

---
transition: slide-left
---

# Software Entropy and Complexity

<div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-4">
  <div class="p-4 rounded-lg backdrop-blur-sm border border-gray-300/10">
    <div class="text-4xl mb-2">⚠️</div>
    <h3 class="text-xl font-bold mb-2 text-orange-300">Definition of Bad Code</h3>
    <p class="text-base">Anything in the structure of a system that makes it hard to understand and modify</p>
  </div>

  <div class="p-4 rounded-lg backdrop-blur-sm border border-gray-300/10">
    <div class="text-4xl mb-2">🔄</div>
    <h3 class="text-xl font-bold mb-2 text-blue-300">Software Entropy</h3>
    <p class="text-base">The tendency for systems to drift toward disaster and collapse if changes are made without considering the design of the whole system</p>
  </div>
</div>

<div class="mt-4 p-4 bg-purple-800/20 rounded-lg backdrop-blur-sm">
  <h3 class="text-xl font-bold mb-2 text-purple-300">Thesis</h3>
  <p class="text-base"><strong>Code is NOT cheap.</strong> Bad code is the most expensive it has ever been because it prevents you from taking advantage of AI's bounty</p>
</div>

<!--
Software entropy refers to the natural tendency of systems to degrade over time when changes aren't made with consideration for the overall design.
John Ousterhout defines complexity as anything in the structure of a system that makes it hard to understand and modify.
In the AI era, bad code is particularly costly because AI tools perform best in well-structured, clean codebases.
Poor code quality creates a barrier to leveraging AI's full potential, making it impossible to benefit from automation and assistance.
-->

---
transition: slide-left
layout: quote
---

<div class="flex flex-col gap-5">
  <div class="p-5 rounded-xl border border-blue-300/30 bg-blue-900/20 flex items-start">
    <img src="/assets/a-philosophy-of-software-design-john-ousterhout.jpg" alt="A Philosophy of Software Design Book Cover" class="w-16 h-20 object-cover mr-4 rounded" />
    <div>
      <div class="text-xs font-bold uppercase tracking-widest text-blue-400 mb-2">📖 A Philosophy of Software Design — John Ousterhout</div>
      <p class="text-lg italic">"Complexity is anything related to the structure of a software system that makes it hard to understand and modify the system."</p>
      <p class="text-sm mt-2 opacity-60">→ The definition of bad code used throughout this presentation</p>
    </div>
  </div>

  <div class="p-5 rounded-xl border border-orange-300/30 bg-orange-900/20 flex items-start">
    <img src="/assets/the-pragmatic-programmer-hunt-thomas.jpg" alt="The Pragmatic Programmer Book Cover" class="w-16 h-20 object-cover mr-4 rounded" />
    <div>
      <div class="text-xs font-bold uppercase tracking-widest text-orange-400 mb-2">📖 The Pragmatic Programmer — Hunt & Thomas</div>
      <p class="text-lg italic">Software Entropy: systems tend toward "disaster" and "floating away from each other" when changes ignore the overall design.</p>
      <p class="text-sm mt-2 opacity-60">→ The force behind degrading AI-generated codebases</p>
    </div>
  </div>
</div>

<!--
These two books ground the core thesis of the presentation.
Ousterhout gives us a precise vocabulary for what we're fighting against.
The Pragmatic Programmer explains why ignoring design inevitably leads to collapse.
-->

---
transition: slide-left
---

# Garbage In, Garbage Out: AI's Dependency on Quality Code

<div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-4">
  <div class="p-4 rounded-lg backdrop-blur-sm border border-red-300/30 text-center">
    <div class="text-5xl mb-2">📥</div>
    <h3 class="text-xl font-bold mb-2 text-red-300">Bad Code Input</h3>
    <p class="text-lg">When we produce garbage code...</p>
  </div>

  <div class="p-4 rounded-lg backdrop-blur-sm border border-green-300/30 text-center">
    <div class="text-5xl mb-2">📤</div>
    <h3 class="text-xl font-bold mb-2 text-green-300">Quality Output</h3>
    <p class="text-lg">Good code makes AI work really well!</p>
  </div>
</div>

<div class="mt-4 p-4 bg-blue-800/20 rounded-lg backdrop-blur-sm text-center">
  <h4 class="font-bold text-lg text-blue-300 mb-2">The Cycle Effect</h4>
  <p class="text-lg"><strong>High-quality codebases</strong> enable AI to understand patterns, suggest improvements, and generate better code</p>
</div>

<!--
In the age of AI, the old adage "Garbage In, Garbage Out" takes on new meaning.
When we feed poor quality code to AI tools, they learn from bad patterns and perpetuate them.
Conversely, when we maintain clean, well-structured codebases, AI can better understand the patterns and help us write even better code.
The quality of our code directly impacts the effectiveness of our AI tools - making good software fundamentals more important than ever.
-->

---
transition: slide-left
---

# Tip #1 - Reach a Shared Design Concept

<div class="grid grid-cols-1 md:grid-cols-3 gap-3 mt-4">
  <div class="p-3 rounded-lg backdrop-blur-sm border border-red-300/20">
    <div class="text-3xl mb-1">❌</div>
    <h4 class="text-lg font-bold mb-1 text-red-300">Failure Mode</h4>
    <p class="text-sm">"The AI didn't do what I wanted"</p>
  </div>

  <div class="p-3 rounded-lg backdrop-blur-sm border border-blue-300/20">
    <div class="text-3xl mb-1">💡</div>
    <h4 class="text-lg font-bold mb-1 text-blue-300">The Skill</h4>
    <p class="text-sm"><strong>"Grill Me"</strong></p>
  </div>

  <div class="p-3 rounded-lg backdrop-blur-sm border border-green-300/20">
    <div class="text-3xl mb-1">🎯</div>
    <h4 class="text-lg font-bold mb-1 text-green-300">Goal</h4>
    <p class="text-sm">Shared "design concept" before creating assets</p>
  </div>
</div>

<div class="mt-4 p-3 bg-gray-800/30 rounded-lg backdrop-blur-sm">
  <h4 class="text-lg font-bold mb-2 text-yellow-300">"Grill Me" Technique:</h4>
  <ul class="space-y-2 text-base">
    <li>"Interview me relentlessly about every aspect of this plan until we reach a shared understanding."</li>
    <li>Walk down the "design tree" to resolve dependencies one by one</li>
  </ul>
</div>

<!--
Communication failures with AI often stem from mismatched expectations.
The "Grill Me" technique involves thoroughly questioning every aspect of a plan until there's complete clarity.
This means walking through the design tree, resolving dependencies one by one, and ensuring both you and the AI have the same understanding.
The goal is to establish a shared design concept - the invisible theory of what you're building - before moving to implementation.
-->

---
transition: slide-left
layout: quote
---

<div class="flex flex-col gap-5">
  <div class="p-5 rounded-xl border border-purple-300/30 bg-purple-900/20 flex items-start">
    <img src="/assets/the-design-of-design-frederick-p-brooks.jpg" alt="The Design of Design Book Cover" class="w-16 h-20 object-cover mr-4 rounded" />
    <div>
      <div class="text-xs font-bold uppercase tracking-widest text-purple-400 mb-2">📖 The Design of Design — Frederick P. Brooks</div>
      <p class="text-lg italic">The <strong>design concept</strong> is the "invisible theory" — the ephemeral shared understanding that must exist when more than one party designs something together.</p>
      <p class="text-sm mt-2 opacity-60">→ What the "Grill Me" technique is building toward</p>
      <p class="text-sm opacity-60">→ The <strong>design tree</strong> resolves dependencies between decisions one by one during planning</p>
    </div>
  </div>

  <div class="p-5 rounded-xl border border-orange-300/30 bg-orange-900/20">
    <div class="text-xs font-bold uppercase tracking-widest text-orange-400 mb-2">📖 The Pragmatic Programmer — Hunt & Thomas</div>
    <p class="text-lg italic">"No one knows exactly what they want."</p>
    <p class="text-sm mt-2 opacity-60">→ The communication barrier between a developer and an AI that "Grill Me" is designed to overcome</p>
  </div>
</div>

<!--
Brooks gives us the theory behind why alignment matters before implementation starts.
The Pragmatic Programmer explains why requirements are always fuzzy — a reality that applies equally to human-AI communication.
-->

---
transition: slide-left
---

# Tip #2 - Ubiquitous Language

<div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-4">
  <div class="p-4 rounded-lg backdrop-blur-sm border border-red-300/20">
    <div class="text-3xl mb-2">❌</div>
    <h3 class="text-xl font-bold mb-2 text-red-300">Failure Mode</h3>
    <p class="text-lg">"The AI is way too verbose"</p>
  </div>

  <div class="p-4 rounded-lg backdrop-blur-sm border border-green-300/20">
    <div class="text-3xl mb-2">✅</div>
    <h3 class="text-xl font-bold mb-2 text-green-300">Solution</h3>
    <p class="text-lg"><strong>Ubiquitous Language</strong> (from DDD)</p>
  </div>
</div>

<div class="mt-4 p-4 bg-gray-800/30 rounded-lg backdrop-blur-sm">
  <h4 class="text-lg font-bold mb-2 text-teal-300">Implementation:</h4>
  <ul class="space-y-2 text-base">
    <li>Create a markdown file of shared terms derived from the domain model</li>
    <li>Use these terms in code, conversations with AI, and with domain experts</li>
  </ul>

  <div class="mt-2 p-2 bg-blue-800/20 rounded-lg">
    <strong class="text-base">Benefit:</strong> Improves planning traces and keeps implementation aligned with the plan
  </div>
</div>

<!--
Derived from Domain-Driven Design, ubiquitous language ensures consistent terminology across the team, code, and interactions with AI.
Create a shared glossary document that defines terms from your domain model.
Using consistent language improves communication with AI, reduces verbosity, and keeps implementation aligned with your plans.
This shared vocabulary becomes crucial when directing AI to implement specific features.
-->

---
transition: slide-left
layout: quote
---

<div class="p-6 rounded-xl border border-green-300/30 bg-green-900/20 flex items-start">
  <img src="/assets/domain-driven-design-eric-evans.jpg" alt="Domain-Driven Design Book Cover" class="w-20 h-24 object-cover mr-4 rounded" />
  <div>
    <div class="text-xs font-bold uppercase tracking-widest text-green-400 mb-3">📖 Domain-Driven Design — Eric Evans</div>
    <p class="text-xl italic">"Conversations among developers and expressions of the code and conversations with domain experts are all derived from the same domain model."</p>
    <p class="text-sm mt-4 opacity-60">→ Applied to AI: a shared markdown glossary anchors the AI's implementation to your plan, reducing drift and verbosity</p>
  </div>
</div>

<!--
Domain-Driven Design coined ubiquitous language as a practice for aligning teams around a shared vocabulary.
Pocock extends this idea to human-AI collaboration — the same principle prevents the AI from drifting into its own interpretation of your domain.
-->

---
transition: slide-left
---

# Tip #3 - TDD (Test-Driven Development)

<div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-4">
  <div class="p-4 rounded-lg backdrop-blur-sm border border-red-300/20">
    <div class="text-3xl mb-2">❌</div>
    <h3 class="text-xl font-bold mb-2 text-red-300">Failure Mode</h3>
    <p class="text-lg">"It just doesn't work"</p>
  </div>

  <div class="p-4 rounded-lg backdrop-blur-sm border border-yellow-300/20">
    <div class="text-3xl mb-2">💡</div>
    <h3 class="text-xl font-bold mb-2 text-yellow-300">Key Principle</h3>
    <p class="text-lg"><strong>"The rate of feedback is your speed limit."</strong></p>
  </div>
</div>

<div class="mt-4 p-4 bg-gray-800/30 rounded-lg backdrop-blur-sm">
  <h4 class="text-lg font-bold mb-2 text-purple-300">Strategy:</h4>
  <p class="text-base mb-3">Don't "outrun your headlights" by producing too much code at once</p>

  <div class="p-3 bg-green-800/20 rounded-lg">
    <h5 class="text-base font-bold mb-1 text-green-300">Practice:</h5>
    <p class="text-base">Use TDD to force the AI to take small, deliberate steps: <strong>Create a test → Make it pass → Refactor</strong></p>
  </div>
</div>

<!--
AI can sometimes produce large amounts of code without verification, leading to non-functional results.
TDD provides the necessary feedback loops to ensure functionality.
The principle "the rate of feedback is your speed limit" means you shouldn't produce more code than you can verify.
Use TDD to constrain AI to small, verifiable steps: write a test, make it pass, then refactor.
This prevents the AI from "outrunning its headlights" and creating unverifiable code.
-->

---
transition: slide-left
layout: quote
---

<div class="p-6 rounded-xl border border-orange-300/30 bg-orange-900/20 flex items-start">
  <img src="/assets/the-pragmatic-programmer-hunt-thomas.jpg" alt="The Pragmatic Programmer Book Cover" class="w-20 h-24 object-cover mr-4 rounded" />
  <div>
    <div class="text-xs font-bold uppercase tracking-widest text-orange-400 mb-3">📖 The Pragmatic Programmer — Hunt & Thomas</div>
    <p class="text-xl italic">"Outrunning Your Headlights" — going too fast means you can't react to what's ahead in time.</p>
    <div class="mt-4 p-3 bg-black/20 rounded-lg">
      <p class="text-lg font-semibold">"The rate of feedback is your speed limit."</p>
    </div>
    <p class="text-sm mt-4 opacity-60">→ Applied to AI: don't let it generate more code than you can verify. TDD enforces this constraint.</p>
  </div>
</div>

<!--
The Pragmatic Programmer's "Outrunning Your Headlights" metaphor maps perfectly onto AI-assisted development.
Feedback loops — tests passing or failing — are the headlights. TDD keeps the AI within the beam.
-->

---
transition: slide-left
---

# Deep vs. Shallow Modules

<div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-4">
  <div class="p-4 rounded-lg backdrop-blur-sm border border-red-300/30">
    <div class="text-3xl mb-2">🌊</div>
    <h3 class="text-xl font-bold mb-2 text-red-300">Shallow Modules</h3>
    <ul class="space-y-2 text-base">
      <li>Small functionality</li>
      <li>Complex interface</li>
      <li>Hard for AI to navigate</li>
    </ul>
  </div>

  <div class="p-4 rounded-lg backdrop-blur-sm border border-green-300/30">
    <div class="text-3xl mb-2">💎</div>
    <h3 class="text-xl font-bold mb-2 text-green-300">Deep Modules</h3>
    <ul class="space-y-2 text-base">
      <li>Lots of functionality</li>
      <li>Simple interface</li>
      <li>Clear boundaries</li>
    </ul>
  </div>
</div>

<div class="mt-4 p-4 bg-blue-800/20 rounded-lg backdrop-blur-sm text-center">
  <h4 class="text-xl font-bold text-blue-300">Goal</h4>
  <p class="text-lg mt-1">Turn shallow modules into deep modules to create a <strong>"testable codebase"</strong></p>
</div>

<!--
Shallow modules have complex interfaces relative to their functionality, creating many small, interconnected parts that are difficult for both humans and AI to navigate.
Deep modules provide lots of functionality through simple, well-defined interfaces.
In the AI era, deep modules are preferable because they provide clear boundaries and interfaces that AI can understand and work with more effectively.
Transforming shallow modules into deep ones creates a more testable and maintainable codebase.
-->

---
transition: slide-left
layout: quote
---

<div class="p-6 rounded-xl border border-blue-300/30 bg-blue-900/20 flex items-start">
  <img src="/assets/a-philosophy-of-software-design-john-ousterhout.jpg" alt="A Philosophy of Software Design Book Cover" class="w-20 h-24 object-cover mr-4 rounded" />
  <div>
    <div class="text-xs font-bold uppercase tracking-widest text-blue-400 mb-3">📖 A Philosophy of Software Design — John Ousterhout</div>
    <p class="text-xl italic"><strong>Deep modules</strong> hide significant functionality behind a simple interface. <strong>Shallow modules</strong> expose a complex interface for little internal functionality.</p>
    <div class="mt-4 grid grid-cols-2 gap-3 text-sm">
      <div class="p-3 bg-red-900/30 rounded-lg">
        <p class="font-bold text-red-300 mb-1">Shallow</p>
        <p class="opacity-70">Complex interface → little power → AI gets lost</p>
      </div>
      <div class="p-3 bg-green-900/30 rounded-lg">
        <p class="font-bold text-green-300 mb-1">Deep</p>
        <p class="opacity-70">Simple interface → lots of power → AI navigates easily</p>
      </div>
    </div>
  </div>
</div>

<!--
Ousterhout's deep/shallow module framework gives us a concrete target when improving codebase architecture.
Deep modules are AI-friendly: a simple interface means fewer decisions an AI has to navigate to use a component correctly.
-->

---
transition: slide-left
---

# Tip #4 - Improve Codebase Architecture

<div class="flex flex-col items-center justify-center mt-2">
  <div class="text-5xl mb-2">🏗️</div>
  <h3 class="text-xl font-bold mb-2 text-center text-teal-300">Process</h3>

  <div class="flex flex-wrap justify-center gap-4 mb-3">
    <div class="flex flex-col items-center">
      <div class="text-3xl mb-1">🔍</div>
      <p class="text-base text-center">Explore codebase</p>
    </div>
    <div class="flex flex-col items-center">
      <div class="text-3xl mb-1">🔗</div>
      <p class="text-base text-center">Find related code</p>
    </div>
    <div class="flex flex-col items-center">
      <div class="text-3xl mb-1">📦</div>
      <p class="text-base text-center">Wrap in module</p>
    </div>
  </div>

  <div class="p-3 bg-purple-800/20 rounded-lg backdrop-blur-sm text-center">
    <h4 class="text-base font-bold text-purple-300 mb-1">Benefit</h4>
    <p class="text-sm">Simplifies the "map" for both humans and AI</p>
  </div>
</div>

<!--
Continuously improve your codebase by identifying related functionality and encapsulating it in well-designed modules.
This process simplifies the overall architecture, making it easier for both human developers and AI assistants to understand and navigate the codebase.
Good architecture acts as a roadmap that guides both human thought processes and AI implementation decisions.
-->

---
transition: slide-left
---

# Tip #5 - Design the Interface, Delegate the Implementation

<div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-4">
  <div class="p-4 rounded-lg backdrop-blur-sm border border-blue-300/30">
    <div class="text-3xl mb-2">👤</div>
    <h3 class="text-xl font-bold mb-2 text-blue-300">Human Role</h3>
    <ul class="space-y-2 text-base">
      <li>Design the interface</li>
      <li>Verify via tests</li>
      <li>Focus on architecture</li>
    </ul>
  </div>

  <div class="p-4 rounded-lg backdrop-blur-sm border border-green-300/30">
    <div class="text-3xl mb-2">🤖</div>
    <h3 class="text-xl font-bold mb-2 text-green-300">AI Role</h3>
    <ul class="space-y-2 text-base">
      <li>Handle implementation</li>
      <li>Inside the "big blob"</li>
      <li>Deal with complexity</li>
    </ul>
  </div>
</div>

<div class="mt-4 p-4 bg-yellow-800/20 rounded-lg backdrop-blur-sm text-center">
  <h4 class="text-lg font-bold text-yellow-300 mb-1">Result</h4>
  <p class="text-base">Saves "brain power" by reducing implementation details a developer needs to hold in mind</p>
</div>

<div class="mt-2 text-center text-sm opacity-70">
  <em class="text-base">Treat deep modules as "gray boxes"</em>
</div>

<!--
As a human developer, focus on designing clean interfaces and verifying their correctness through tests.
Let AI handle the complex implementation details within modules.
This division of labor allows humans to concentrate on architecture and design while AI handles the detailed implementation.
This approach conserves cognitive resources by reducing the amount of detail humans need to manage simultaneously.
-->

---
transition: slide-left
---

# Conclusion - Strategic vs. Tactical

<div class="flex flex-col items-center justify-center mt-4">
  <div class="text-6xl mb-4">🧠</div>
  <h3 class="text-2xl font-bold mb-6 text-center text-purple-300">Core Message</h3>

  <div class="p-4 bg-gray-800/30 rounded-lg backdrop-blur-sm mb-6">
    <p class="text-lg text-center"><strong>Invest in the design of the system every day</strong></p>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-4 w-full max-w-2xl">
    <div class="p-4 rounded-lg backdrop-blur-sm border border-teal-300/30 text-center">
      <div class="text-4xl mb-2">🤖</div>
      <h4 class="text-lg font-bold text-teal-300">AI</h4>
      <p class="text-base">Tactical Programmer</p>
      <p class="text-sm opacity-70">Sergeant on the ground making code changes</p>
    </div>
    <div class="p-4 rounded-lg backdrop-blur-sm border border-orange-300/30 text-center">
      <div class="text-4xl mb-2">👤</div>
      <h4 class="text-lg font-bold text-orange-300">Human</h4>
      <p class="text-base">Strategic Level Thinker</p>
      <p class="text-sm opacity-70">Designing the system</p>
    </div>
  </div>

  <div class="mt-6 p-4 bg-green-800/20 rounded-lg backdrop-blur-sm text-center">
    <p class="text-lg"><strong>Software fundamentals are what allow you to make a high impact in the AI age</strong></p>
  </div>
</div>

<!--
In the AI era, the relationship between humans and machines shifts to a strategic-tactical dynamic.
Humans operate at the strategic level, focusing on design, architecture, and system-wide decisions.
AI serves as the tactical programmer, implementing specific changes and handling detailed work.
Success in this new paradigm requires a strong foundation in software fundamentals - these principles are what enable us to leverage AI effectively and create high-impact solutions.
-->

---
transition: slide-left
layout: quote
---

<div class="p-6 rounded-xl border border-yellow-300/30 bg-yellow-900/20 flex items-start">
  <img src="/assets/test-driven-development-by-example-beck-kent.jpg" alt="Test Driven Development by Example Book Cover" class="w-20 h-24 object-cover mr-4 rounded" />
  <div>
    <div class="text-xs font-bold uppercase tracking-widest text-yellow-400 mb-3">Kent Beck — Test Driven Development by Example</div>
    <p class="text-2xl italic font-semibold">"Invest in the design of the system every day."</p>
    <p class="text-sm mt-4 opacity-60">→ The "specs to code" movement is the opposite: it <em>divests</em> from system design by ignoring the code entirely. Software fundamentals are the antidote.</p>
  </div>
</div>

<!--
Kent Beck's principle captures the entire thesis of this presentation in a single sentence.
Daily investment in design — not outsourcing it entirely to AI — is what separates engineers who thrive in the AI age from those who don't.
-->

