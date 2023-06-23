# Auto Rebase

This action rebases all open PR's when the base branch in updated.

## Inputs

### `github_token`

**Required** Github token for the repository

### `filter`

`label` **default** Rebase PRs that contain the label **rebase**

`auto-merge` Only rebase PR's set automatically merge when all requirements are met

`always` Rebase all PR's to the current branch

## Example usage
```yaml
on:
  push:
    branches:
      - master

jobs:
  rebase:
    runs-on: ubuntu-latest
    steps:
      - uses: Vin65/auto-rebase@v0.1.1
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          filter: label
```
