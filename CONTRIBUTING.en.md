<p align="center">
  <a href="CONTRIBUTING.md">Español</a> | <b>English</b>
</p>

# Contributing guide

Working rules for the repository: branches, commits and Pull Requests. They are enforced by GitHub rulesets and GitHub Actions workflows.

## Branches

| Branch | Purpose |
|---|---|
| `main` | Final delivery. It is locked and is not touched until delivery. |
| `develop` | Integration. It is the default branch and only changes through Pull Requests. |
| `feature/pablo` | Pablo's working branch. |
| `feature/alvaro` | Álvaro's working branch. |

Each person works only on their own `feature` branch. These branches are never deleted or rewritten: no force push.

## Workflow

1. Update your branch with the latest changes from `develop`.
2. Make small commits on your branch and push them.
3. Open a Pull Request from your branch to `develop` and fill in the template (Summary, Changes and Notes).
4. Assign the PR to yourself and make sure **Validate commits** and **Validate PR title** are green.
5. The repository owner merges using **Create a merge commit**.
6. When the work is finished, open a single PR from `develop` to `main`.

## Commits and PR titles

[Conventional Commits](https://www.conventionalcommits.org/) are used, written in English: `type(scope): description in imperative mood`. The scope is optional.

| Type | Use |
|---|---|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation |
| `style` | Formatting, no logic change |
| `refactor` | Restructuring without changing behavior |
| `test` | Tests |
| `chore` | Configuration and maintenance |
| `ci` | Automation (GitHub Actions) |

Examples: `feat(expenses): add receipt upload`, `docs(readme): update branding paths`.

One purpose per commit and per PR.

## Automated checks

Two GitHub Actions workflows review Pull Requests:

| Workflow | Job | What it checks |
|---|---|---|
| **Commit messages** | `Validate commits` | That every commit in the PR follows Conventional Commits. Only for PRs to `develop`. |
| **PR title** | `Validate PR title` | That the PR title follows Conventional Commits. |

Where each PR comes from (only from `feature/pablo` or `feature/alvaro` into `develop`, and only from `develop` into `main`) is a team rule: no workflow enforces it.

## File style

`.editorconfig` defines encoding, indentation and the final newline. All files end with an empty line.
