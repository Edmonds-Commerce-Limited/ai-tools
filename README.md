# Edmonds Commerce AI Tools

GitHub automation workflows for Edmonds Commerce repositories.

## Reusable Workflows

This repository contains centralised reusable workflows that can be called from other Edmonds Commerce repositories.

### Available Workflows

- **triage-reusable.yml** - Automated issue triage with Claude AI
- **pr-review-reusable.yml** - Automated PR review with Claude AI

## Usage

These workflows are called from other repositories using GitHub's reusable workflow syntax:

```yaml
jobs:
  call-triage:
    uses: edmondscommerce/ai-tools/.github/workflows/triage-reusable.yml@master
    secrets: inherit
```

See individual workflow documentation for setup instructions.

## Requirements

- `CLAUDE_CODE_OAUTH_TOKEN` secret must be set at organisation or repository level
- Claude GitHub App must be installed on target repositories
- Repositories must have CLAUDE.md file for project context

## Source

Workflows adapted from BallicomDev/ai-tools for use in Edmonds Commerce organisation.
