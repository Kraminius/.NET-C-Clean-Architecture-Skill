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

Claude Code skills live under your project's `.claude/skills/` directory. Each skill gets its own folder containing a `SKILL.md` file:

```
your-project/
└── .claude/
    └── skills/
        └── clean-naming/
            └── SKILL.md
```

To install, copy the `SKILL.md` file into your project:

```bash
mkdir -p .claude/skills/clean-naming
cp SKILL.md .claude/skills/clean-naming/SKILL.md
```

Claude Code automatically discovers skills in this directory — no additional configuration needed.

## Compatibility

- Claude Code
- OpenCode

## Example

```
Bad:  ISqlPatientStore, DataHelper, PatientService2, ProcessManager
Good: IPatientRepository, InboundMapper, WorkflowOrchestrator, LabResultProcessor
```

## License

[MIT](LICENSE) — use it, name things well, make the next developer smile instead of squint.
