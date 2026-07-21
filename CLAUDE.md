<!-- file: CLAUDE.md -->
<!-- version: 3.2.0 -->
<!-- guid: 3c4d5e6f-7a8b-9c0d-1e2f-3a4b5c6d7e8f -->
<!-- last-edited: 2026-07-21 -->

# CLAUDE.md

Magnet link handler and downloader — Go binary that registers itself as the
system-level `magnet:` URI handler on macOS, Windows, and Linux.

## Coding Standards

Org-wide coding standards are in the `.standards/` git submodule (cloned from `https://github.com/falkcorp/.github`).
Always clone with `git clone --recurse-submodules` so these are available.

Key files:
- **File headers (MANDATORY):** `.standards/instructions/file-headers.md`
- **Commit format:** `.standards/instructions/commit-messages.md`

## Quick Reference

**Main Documentation:**

- [Copilot Instructions](.github/instructions/copilot-instructions.md) - Primary
  AI agent configuration
- [Instructions Directory](.github/instructions/) - All coding standards and
  language-specific rules
- [Prompts Directory](.github/prompts/) - Specialized prompts for specific tasks

**For complete list of all instruction files, see [AGENTS.md](AGENTS.md)**

## 🚨 CRITICAL: Documentation Update Protocol

This repository uses direct-edit documentation workflow:

- Edit documentation directly in target files
- Always update version headers when making changes
- Do not use legacy doc-update scripts (create-doc-update.sh,
  doc_update_manager.py)
- Follow semantic versioning for version numbers

## 🔧 Git Operations Policy

**Preferred order for git operations:**

1. **MCP GitHub tools** (preferred) - Use when available
2. **safe-ai-util** (fallback) - Provides safety checks and logging
3. **Native git** (last resort) - Use only when other options unavailable

**Use VS Code tasks for non-git operations only** (build, lint, test, generate).

## 📋 Key Instruction Categories

### Workflow & Process

- Commit messages (conventional commits format)
- Pull request descriptions
- Code review guidelines
- Test generation standards
- Security best practices

### Language-Specific Rules

- Go, Python, TypeScript, JavaScript, Rust, Shell
- Protobuf, Markdown, JSON, JSONC, HTML/CSS
- GitHub Actions workflows

### Specialized Prompts

- Code review, documentation generation
- Bug reports, feature requests
- Merge conflict resolution
- Test generation

> For all Claude, Copilot, or workflow tasks, **refer to the files in
> `.github/instructions/` and `.github/prompts/`**.


## 📝 Changelog & TODO — Use the Fragment System (MANDATORY)

**Do not hand-edit `CHANGELOG.md`, and do not add new tasks straight into the
`TODO.md` inbox.** Both files are assembled from per-change fragments so that
parallel PRs never collide on them.

- **`CHANGELOG.md` is assembled, not hand-edited.** Add a fragment under
  `changelog.d/` (run `scriv create`, or write the Markdown file by hand). The
  fragments are folded into `CHANGELOG.md` at release time by `scriv`, and a CI
  check (`changelog-check.yml`) requires one on each PR. See `changelog.d/README.md`.
- **New `TODO.md` tasks are added via fragments.** Drop a Markdown fragment in
  `todo.d/` (see `todo.d/README.md`) instead of editing the `## 📥 Inbox`
  section. `scripts/assemble_todo.py` folds fragments in daily. This is
  **add-only**: checking a task off or removing it is a normal direct edit of
  `TODO.md`.
