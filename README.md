# Auto-Assign thread based on PTAL

This Github action automates the following functionality:
- When someone says `@someone PTAL`, assign the member to the thread automatically.
- Additionally, it can also assign multiple members at one using this syntax: `@abc @xyz @pqr ptal`

## Run as a github action

Here is a sample `.yml` file to add this action

```yaml
name: Assign members based on comments
on: [issue_comment]

jobs:
  assign:
    runs-on:  ubuntu-latest
    steps:
      - name: Auto assign on PTAL
        uses: sdhiman99/auto-assign-on-ptal@master
        with:
          repo-token: ${{ secrets.GITHUB_TOKEN }}
```
