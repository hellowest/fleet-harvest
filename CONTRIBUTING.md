# Contributing to Fleet Harvest

Thanks for your interest in contributing! This guide explains how work is planned and merged.

## Workflow

1. **Start from an issue.** Every change is linked to an issue. Use the templates (Bug report or Feature / task).
2. **Create a branch from `main`:**
   - `feat/<issue>-<short-name>` – new functionality
   - `fix/<issue>-<short-name>` – bug fixes
   - `chore/`, `docs/`, `ci/`, `refactor/` – everything else

   Example: `feat/4-docker-compose-skeleton`
3. **Commit using [Conventional Commits](https://www.conventionalcommits.org/):**

       feat: add ssh executor
       fix: handle timeout on file upload
       test: cover audit merge rules
       docs: update quick start
       chore: bump dependencies

   Keep commits small and focused. Use the imperative mood ("add", not "added").s
4. **Open a pull request** using the PR template and include `Closes #<issue>`.
   Open it as a draft while work is in progress.
5. **Review.** Check the diff, make sure CI passes, and resolve all comments.
6. **Squash and merge.** The PR title becomes the commit on `main`, so it must follow Conventional Commits too. Delete the branch after merging.

## Local setup

See the [README](README.md#quick-start) for running the project with Docker Compose.

## Code style

- Python formatting and linting with [ruff](https://docs.astral.sh/ruff/), enforced by pre-commit:
```bash
  pip install pre-commit
  pre-commit install
```
- Add or update tests for every behaviour change (`pytest`).
- Never commit secrets. Use `.env` (ignored) and keep `.env.example` up to date.

## Reporting bugs and requesting features

Open an issue using the matching template. Search existing issues first to avoid duplicates.