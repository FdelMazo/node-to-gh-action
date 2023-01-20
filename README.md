```yaml
name: Build & Deploy to Github Pages

on:
  push:
    branches: [master, main]

# Before using this action
# 1. Create a `gh-pages` branch
# 2. Set up your github pages settings to point to that branch
# 3. Under settings/actions, on "Workflow permissions" give the action "Read & Write permissions"

jobs:
  node-to-gh:
    runs-on: ubuntu-latest
    name: Build & Deploy to Github Pages
    steps:
      - id: node-to-gh
        uses: fdelmazo/node-to-gh-action@v1
```
