---
name: execution-protocol
description: Create an execution protocol—a complete spec for an AI agent working on a project.
---

# Execution Protocol

A job description for an AI agent: what to build, how it fits together, when it's done.

## Process

1. **Explore**: Check context—files, docs, commits, patterns.
2. **Ask**: Ask many questions (multiple choice when possible) until you can fill every protocol section.
3. **Approaches**: If multiple valid paths exist, present 2-3 options. Lead with your recommendation.
4. **Derive**: Map conversation to protocol sections:
   - Mission: What, who, why
   - Architecture: Technical decisions
   - Components: What to build
   - Constraints: Non-negotiables
   - Build Order: Sequence
   - Done When: Success criteria
5. **Write**: Output `PLAN.md`. Create `PROGRESS.md` with completed/remaining work.

## Protocol Structure (under 100 lines)

**Instructions**:
- Read PROGRESS.md to know what's done, check git log for context
- Build the next incomplete phase—do not ask what to work on
- Make decisions from existing code patterns
- Update PROGRESS.md when done, continue to next phase
- No clarifying questions—ship working features

**Mission**: 1-3 lines. What, who, why.

**Architecture**: Technical decisions stated, not debated.

**Components**: What to build. One line each—name and essence.

**Constraints**: Non-negotiables only.

**Build Order**: Sequenced phases. Names only.

**Done When**: Concrete, testable acceptance criteria.

## Writing Principles

**Concrete, not vague**
- "CLI tool for rotating AWS credentials" not "developer utility"
- "Postgres, Redis, S3" not "appropriate storage solutions"

**No filler**
- Cut: "Prefer working software over perfection", "Start simple", "Future integrations"