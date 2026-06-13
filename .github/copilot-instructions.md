<!-- file: .github/copilot-instructions.md -->
<!-- version: 2.4.0 -->
<!-- guid: 4d5e6f7a-8b9c-0d1e-2f3a-4b5c6d7e8f9a -->
<!-- last-edited: 2026-06-13 -->

# magnet-handler — Additional Context

Org-wide coding standards (file headers, language rules, commit format) are at
**https://github.com/falkcarp/.github** and apply automatically to this repo.

For full project context: **CLAUDE.md** at the repo root.

## Project overview

Magnet link handler and downloader. Language: Go. Registers itself as the
system-level magnet: URI handler on macOS, Windows, and Linux.

## Key directories

| Path | Purpose |
|---|---|
| `magnet-handler.go` | Main entry point and magnet URL parsing |
| `register_unix.go` | Unix/macOS handler registration |
| `register_windows.go` | Windows handler registration |
| `install-macos.sh` | macOS install script |
| `install.ps1` | Windows PowerShell install script |

## Critical constraints

- Cross-platform: code must build and work on Linux, macOS, and Windows.
- No external dependencies beyond `golang.org/x/sys`.
