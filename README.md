# Domain Name Finder

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that brainstorms catchy domain names and checks availability via `whois`.

## What it does

Give it a topic or business idea and it will:

1. Brainstorm 15-25 creative domain name ideas
2. Batch-check availability using `whois`
3. Present results in a clean table with availability status
4. Iterate based on your feedback until you find the perfect name

## Name style

The skill generates names that are:
- **Easy to spell** when heard aloud (no ambiguous spellings)
- **2-3 syllables**, compound words (noun+noun, verb+noun)
- **Catchy** - rhymes, alliteration, rhythmic patterns
- **No hyphens, no numbers**

## TLD priority

Checks `.com` first, then falls back to quality alternatives:
- **Tier 1:** .com, .io
- **Tier 2:** .co, .dev, .app, .ai, .so, .sh, .me, .to, .cc
- **Tier 3:** .net, .org, .xyz, .tech, .site, .land, .run, .fun, .gg, .tv, .fm

Avoids low-value/spammy TLDs (.biz, .info, .click, .top, etc).

## Requirements

- `whois` command available on your system (pre-installed on macOS)

## Installation

Copy `SKILL.md` to your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/domain-finder
cp SKILL.md ~/.claude/skills/domain-finder/SKILL.md
```

Then start a new Claude Code session and ask it to find you a domain name.

## Usage

Just describe what you need:

> "Find me a domain for a secure PDF sharing platform"

> "I need a name for a surf lifestyle brand"

> "Check if duckdoc.com is available, and try .io and .co too"

## License

MIT
