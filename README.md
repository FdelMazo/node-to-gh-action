```yaml
name: Build & Deploy to Github Pages

on:
  push:
    branches: [master, main]

# Before using this action
# 1. Create a `gh-pages` branch
# 2. Set up your github pages settings to point to that branch
# 3. Under your `package.json` set up the `homepage` attribute to your gh-page domain (i.e, `<username>.github.io/<repo>` or your own custom domain)

permissions:
  contents: write

jobs:
  node-to-gh:
    runs-on: ubuntu-latest
    name: Build & Deploy to Github Pages
    steps:
      - id: node-to-gh
        uses: fdelmazo/node-to-gh-action@v2
```
