# Self-Writing Software

*Principles for software that improves itself.*

---

## What this is

Self-writing software closes the loop between production signals and released code — autonomously. It doesn't just flag improvement opportunities, it diagnoses them, proposes fixes, validates them, and with human sign-off, deploys them. Humans set direction and make judgment calls. Everything else is automatic.

---

## The north star

A codebase that is continuously improving on it's own by using feature requests and failures as signals. The humans who own it are focused on what only humans can do: deciding what the software should become.

---

## Core Principles

### 1. Signals are improvement requests

Every log event, bug report, freature request, social media feedback post, analytic metric value different than expected is a signal for a potential system improvement. The system's job is to turn the full signal stream into a prioritized queue of proposed improvements — not a dashboard of things for humans to wonder about.

### 2. The build loop is the product

Signal intelligence without code delivery is a homework. Reporting without a resolution proposal is a burden. The value is the closed loop: signal → diagnosis → fix → test → staged → merged. Everything else is scaffolding for this loop.

### 3. Errors are never optional

Every failure is tracked, surfaced, and fed back as signal. Nothing is swallowed, suppressed, or hidden. A try/catch that silences an error is itself an error. The system rejects it.

### 4. Correctness before visibility

The agentic generator-reviewer loop runs internally until the proposed fix is compliant with the system's architectural constraints and best practices. Humans don't see a draft, they see a release candidate.

### 5. Conservative autonomy, earned incrementally

The system starts with nothing auto-merged. Every category of autonomous action must be explicitly unlocked by a human: "you can merge things like this yourself next time." Autonomy is not configured — it is taught. The system earns trust on specific, confirmed-safe patterns before it acts on them.

### 6. Policy governs; diffs inform

High-risk categories — authentication, payments, data migrations, anything on the revenue path — are managed at the policy level. They never reach the auto-merge queue regardless of confidence. The human manages the envelope of what is automatable, not each individual decision within it.

### 7. The human interface is judgment, not labor

Humans are shown what changed, what it means, and what the first and second-order effects are — in plain language. They can dig into any detail. They can ask questions, send it back for more work with feedback, or approve. What they are not doing is executing. Their value is knowing which direction to go.

### 8. Architecture is a living constraint

Intent documents, architectural decisions, and best practices are part of the agent review loop before any PR surfaces to a human. The agents check their proposed fix against the current architecture. When the architecture itself needs to change, that change is surfaced as a proposed improvement — not silently absorbed into the codebase.

### 9. Incidents are signal on the loop

zWhen an autonomous fix causes a production problem, that is not just a bug — it is feedback on the loop itself. The system that generated the bad fix must learn from the incident. Every rollback, every hotfix, every on-call page triggered by an agent PR is a another signal that tightens the loop.

### 10. Category normalization is a tailwind

As incumbents ship AI coding features, users are trained to expect autonomous agents. A platform that closes the full signal-to-merge loop doesn't compete with this normalization — it benefits from it. The question is never "will users accept autonomous agents." It is "who ships the complete loop first."

---

## What this is not

**Not a code generator.** Code generation is a component, not the product. The product is the loop.

**Not a monitoring tool.** Monitoring tells you what is wrong. Self-writing software fixes it.

**Not autopilot.** The human remains in the loop at every decision that matters. The system earns the right to act autonomously on decisions that don't.

**Not a replacement for good engineering.** The system enforces architectural best practices on every PR it generates. It doesn't lower the quality bar — it applies it consistently at a speed no human team can match.
