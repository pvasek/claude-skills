# Claude Skills Distribution

Pre-built skills for Claude Code.

## Installation

### As a Plugin (recommended)

```bash
/plugin add pvasek/claude-skills
```

### As a Marketplace

```bash
/plugin marketplace add pvasek/claude-skills
```

## Available Skills

| Skill | Description |
|-------|-------------|
| [csharp-expert](#csharp-expert) | C# code analysis and refactoring using Roslyn APIs |

---

### csharp-expert

Roslyn-powered CLI for C# code analysis. 18 commands for symbol lookup, references, refactoring, diagnostics, and more.

**Source**: [pvasek/csharp-project-expert-skill](https://github.com/pvasek/csharp-project-expert-skill)

**Commands**:

| Category | Commands |
|----------|----------|
| Symbol | `find-definition`, `find-references`, `signature`, `list-members`, `rename` |
| Compilation | `diagnostics`, `check-symbol-exists` |
| Type Hierarchy | `find-implementations`, `inheritance-tree` |
| Call Analysis | `find-callers`, `find-callees` |
| Dependencies | `dependencies`, `unused-code` |
| Code Generation | `generate-interface`, `implement-interface` |
| Organization | `list-types`, `namespace-tree`, `analyze-file` |

**Example prompts**:
- "Find all implementations of IUserRepository"
- "Rename the UserService class to UserManager"
- "Show me the inheritance tree for BaseController"

---

## Adding New Skills

Each skill lives in `skills/<skill-name>/` with:
- `SKILL.md` - Skill definition with frontmatter
- `references/` - Optional reference docs
- `scripts/` - Built binaries (per platform)

Skills are published here via CI from their source repos.

## License

This project is licensed under the [MIT License](LICENSE.md).
