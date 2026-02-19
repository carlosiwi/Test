# CLAUDE.md

This file provides guidance for AI assistants (Claude and others) working with this repository.

## Repository Overview

**Name:** Test
**Owner:** carlosiwi
**Remote:** `http://local_proxy@127.0.0.1:60702/git/carlosiwi/Test`

This is a minimal/starter repository. At the time of writing it contains a single file (`test`) with placeholder content. There is no build system, framework, or application code yet.

## Repository Structure

```
Test/
├── CLAUDE.md   # This file — AI assistant guidance
└── test        # Placeholder file with content "Test"
```

## Git Workflow

### Branches

| Branch | Purpose |
|--------|---------|
| `master` | Main branch — stable, reviewed code |
| `claude/<description>-<session-id>` | AI-generated feature branches |

AI assistants **must** develop on a dedicated `claude/` branch and never push directly to `master`.

### Standard Workflow

```bash
# 1. Check current branch
git branch

# 2. Make changes, then stage specific files (never use git add -A blindly)
git add <file>

# 3. Commit with a descriptive message
git commit -m "Short imperative summary

Optional longer explanation of why the change was made."

# 4. Push to the feature branch
git push -u origin <branch-name>
```

### Commit Message Conventions

- Use the imperative mood for the subject line: `Add feature`, `Fix bug`, `Update docs`
- Keep the subject line under 72 characters
- Separate subject from body with a blank line when a body is needed
- The body should explain **why**, not what (the diff shows what)

### Branch Naming

AI-generated branches follow this pattern:
```
claude/<short-description>-<session-id>
```
Example: `claude/claude-md-mltan8xc5nq3txcf-8Mq9p`

## Development Conventions

Since the project has no established stack yet, the following conventions apply as defaults until overridden:

### General

- Prefer editing existing files over creating new ones
- Delete unused code rather than commenting it out
- Keep changes minimal and focused — avoid scope creep
- Do not add features or refactoring beyond what is explicitly requested

### File Operations

- Never commit secrets, credentials, or `.env` files
- Binary files and large assets should be evaluated before committing
- Use `.gitignore` to exclude generated files, build artifacts, and IDE config

### Pull Requests

When opening a PR:
1. Target `master` from your `claude/` branch
2. Title: short and imperative (under 70 characters)
3. Body: bullet-point summary + test plan

## Working with This Repository as an AI Assistant

1. **Always read files before editing them** — never propose changes to code you haven't read
2. **Stay on the assigned branch** — check `git branch` before making commits
3. **Push with upstream tracking**: `git push -u origin <branch-name>`
4. **Do not force-push** to `master` under any circumstances
5. **Retry on network failure** using exponential backoff (2s, 4s, 8s, 16s) for push/fetch
6. **Use specific file staging** (`git add <file>`) rather than `git add .` or `git add -A`
7. **Commit only when explicitly asked** — do not auto-commit exploratory changes

## Future Development Notes

When a language, framework, or build system is introduced to this repository, this file should be updated to include:

- **Build commands** (e.g., `npm run build`, `make`, `cargo build`)
- **Test commands** and how to run them
- **Lint/format commands** and any pre-commit hooks
- **Environment setup** (required env vars, `.env.example`, etc.)
- **Dependency installation** steps
- **Deployment process** if applicable
