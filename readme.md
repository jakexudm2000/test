# test

This is a test repository.

## Repository Structure

```
test/
├── .github/
│   └── workflows/
│       └── opencode.yml   # GitHub Actions workflow for opencode integration
└── readme.md              # This file
```

## GitHub Actions Workflow

`.github/workflows/opencode.yml` defines a workflow named **opencode** that:

- **Triggers on**: issue comments or pull request review comments containing `/oc` or `/opencode`
- **Runs on**: `ubuntu-latest`
- **Steps**:
  1. Checks out the repository (shallow clone, no persisted credentials)
  2. Runs the [`anomalyco/opencode`](https://github.com/anomalyco/opencode) action using model `anthropic/claude-sonnet-4-20250514`

### Required Secrets

| Secret | Description |
|---|---|
| `ANTHROPIC_API_KEY` | API key for Anthropic Claude |
| `GITHUB_TOKEN` | Automatically provided by GitHub Actions |
