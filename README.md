# workflows-pnpm

pnpm related workflows

## Quality

```
name: Pull Request

on:
  pull_request:
    branches: [ main ]

jobs:
  quality:
    uses: harmony-labs/workflows-pnpm/.github/workflows/quality.yaml@main

```

## Release

```
name: On Version Tagged, Build and Publish
on:
  push:
    tags:
    - "v*.*.*"

permissions:
  contents: write
  packages: write

jobs:
  release:
    uses: harmony-labs/workflows-pnpm/.github/workflows/release.yaml@main
    secrets: inherit
```
