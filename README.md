# Clean Naming Skill

> There are only two hard things in Computer Science: cache invalidation and naming things.
> — Phil Karlton

This skill tackles the second one. You're on your own for cache invalidation.

## What Is This?

A [Claude Code skill](https://docs.anthropic.com/en/docs/claude-code/skills) that enforces **Clean Architecture naming conventions** in .NET/C# codebases. It activates during code generation, refactoring, and review — even when you don't explicitly ask for naming help — because good naming is non-negotiable.

## What It Does

- Enforces **intent-revealing names** over implementation-leaking ones (`IPatientRepository`, not `ISqlPatientStore`)
- Applies **layer-appropriate vocabulary** — Domain speaks business, Infrastructure speaks technology, and never the twain shall mix
- Bans naming anti-patterns: `Manager`, `Helper`, `Utils`, `Data`, `Info`, `Impl`, numbered suffixes, and gratuitous abbreviations
- Guides **Clean Architecture project structure** and dependency direction (dependencies flow inward, always)
- Provides the "Conversation Test" — if you can't say the name out loud in a sentence to a colleague, it's wrong

## Installation

Copy `SKILL.md` into your Claude Code skills directory, or add this project as a skill source in your Claude Code configuration.

## Compatibility

- Claude Code
- OpenCode

## Example

```
Bad:  ISqlPatientStore, DataHelper, PatientService2, ProcessManager
Good: IPatientRepository, InboundMapper, WorkflowOrchestrator, LabResultProcessor
```

## License

Use it. Name things well. Make the next developer smile instead of squint.
