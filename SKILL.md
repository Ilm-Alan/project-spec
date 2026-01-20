---
name: execution-protocol
description: Create an execution protocol—a complete spec for an AI agent working on a project.
---

# Execution Protocol

An execution protocol is a job description for an AI agent: what to build, how it fits together, when it's done.

---

## Process

1. **Explore**: If a project exists, check context—files, docs, recent commits, patterns.
2. **Ask**: Ask many questions—multiple choice when possible. Learn: what's being built, why it matters, target users, technical approach, constraints, what "done" looks like. Keep asking until you can fill every protocol section with confidence. The more you learn now, the more autonomous the executing agent can be.
3. **Approaches**: If multiple valid paths exist, present 2-3 options. Lead with your recommendation. Options are for the conversation—the final protocol states one decision.
4. **Derive**: From the conversation, work out the protocol sections:
   - Instructions ← standard (see Protocol Structure)
   - Mission ← what + why + who
   - Architecture ← technical choices from Ask and Approaches
   - Components ← breaking down the system
   - Constraints ← non-negotiables
   - Build Order ← dependencies
   - Done When ← success criteria
5. **Draft**: Write the protocol following Protocol Structure below.
6. **Cut**: Remove anything that isn't essential.
7. **Output**: Write protocol to `PLAN.md`. If it fails the Finish Checklist, revise.

---

## Protocol Structure (under 100 lines)

- **Instructions**: How the agent operates autonomously. Must include: read PROGRESS.md to know what's done, check git log for context, then build the next incomplete phase without asking. Make decisions based on existing code patterns. Update PROGRESS.md when work completes and continue to the next phase. No clarifying questions—inspect the code, make reasonable choices, ship working features.
- **Mission**: 1-3 lines. Job framing ("Your job is to..."), target users, why it matters.
- **Architecture**: How it fits together. Key technical decisions stated, not debated.
- **Components**: What to build. One line each—name and essence.
- **Constraints**: Non-negotiables. Requirements, not suggestions.
- **Build Order**: Sequenced phases. Names only.
- **Done When**: Acceptance criteria. Concrete, testable.

---

## Writing Principles

**Concrete, not vague**
- "CLI tool for rotating AWS credentials" not "developer utility"
- "Postgres, Redis, S3" not "appropriate storage solutions"

**No filler**
- Cut: "Prefer working software over perfection", "Start simple", "Future integrations"
- Components say what to build. Build Order says when. Don't duplicate.

---

## Finish Checklist

- Do Instructions tell the agent to build autonomously without asking questions?
- Do Instructions say to read PROGRESS.md, check git log, then build the next incomplete phase?
- Do Instructions say to make decisions from code patterns and ship working features?
- Can someone read Mission and know exactly what they're building and for whom?
- Are technical choices in Architecture stated, not listed as options?
- Is each Component one line—name and essence?
- Are Constraints requirements, not suggestions?
- Is Build Order sequenced with names only?
- Does Done When have concrete, verifiable conditions?
