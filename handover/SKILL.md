---
name: handover
description: Generate a comprehensive handover document. Use when the user types "/handover" or asks to "create a handover", "generate handover doc", "summarize the session", or "create a shift-change report".
disable-model-invocation: true
version: 1.0.0
---

# Handover Document Generator

Generate a comprehensive HANDOVER.md file that documents the current session's work, decisions, and progress.

## Current Context

- Current branch: !`git branch --show-current`
- Modified files: !`git status --short`
- Recent commits: !`git log -5 --oneline`

## Instructions

Review the entire conversation history from this session and create a `HANDOVER.md` file in the project root with the following structure:

```markdown
# Handover Document

> Generated: [current date and time]
> Session duration: [approximate time if discernible]

## What We Were Working On

[Brief overview of the main task or feature being developed]

## What Got Done

[Bulleted list of completed work items, changes made, files modified]

- Feature/fix implemented
- Files created/modified
- Tests added
- Documentation updated

## What Worked

[Successful approaches, solutions that worked well, positive outcomes]

- Approaches that were effective
- Solutions that resolved issues
- Patterns that should be repeated

## What Didn't Work

[Failed approaches, bugs encountered, issues discovered, blockers hit]

- Approaches that failed and why
- Bugs encountered and their root causes
- Issues discovered but not yet resolved
- Blockers that prevented progress

## Key Decisions Made

[Important architectural, technical, or design decisions and their rationale]

- Decision: [what was decided]
  - Rationale: [why this approach was chosen]
  - Alternatives considered: [what other options were evaluated]

## Lessons Learned & Gotchas

[Important insights, non-obvious behaviors, things to watch out for]

- Platform-specific behaviors discovered
- Edge cases identified
- Pitfalls to avoid
- Best practices reinforced

## Next Steps

[Clear action items for continuing the work]

- [ ] Immediate next action
- [ ] Follow-up tasks
- [ ] Testing needed
- [ ] Documentation to write
- [ ] Technical debt to address

## Important Files

[Map of key files touched or relevant to the work]

- `path/to/file1.ts` - [brief description of its role/changes]
- `path/to/file2.tsx` - [brief description of its role/changes]
- `path/to/file3.test.ts` - [brief description of tests added]

## Open Questions

[Unresolved questions, areas needing clarification or decision]

- Question that needs answering
- Design decision pending
- Uncertainty about approach

## Context for Next Session

[Any important context someone picking up this work should know]

[Additional notes, warnings, or context that doesn't fit other sections]
```

## Guidelines

1. **Be specific and concrete**: Use actual file names, function names, line numbers
2. **Be honest**: Document failures and blockers, not just successes
3. **Prioritize actionability**: Next steps should be clear and unambiguous
4. **Include technical details**: Code snippets, error messages, specific behaviors
5. **Think chronologically**: Review the conversation from start to finish
6. **Capture decisions**: Document not just what was done, but why
7. **Note surprises**: Unexpected behaviors, platform differences, gotchas
8. **Skip empty sections**: If there are no open questions, omit that section
9. **Be concise**: Each section should be scannable and to-the-point

## After Creating the File

1. Confirm the HANDOVER.md file was created successfully
2. Provide a brief summary of what was captured
3. Suggest any critical next steps from the document
