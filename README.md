# Install Graphviz

[![GitHub CI](https://github.com/tlylt/install-graphviz/actions/workflows/test.yml/badge.svg)](https://github.com/tlylt/install-graphviz/actions/workflows/test.yml)

This action provides the following functionality for GitHub Actions users:

- Install Graphviz cross-platform (Linux, macOS, Windows)

# Usage

This action will detect the operating system and install Graphviz cross-platform. You may use the action without any additional parameters.

```yaml
steps:
- uses: tlylt/install-graphviz@v1
```

# Testing

```yaml
name: Test install-graphviz

on:
  push:
    branches:
      - main

jobs:
  build:
    strategy:
      matrix:
        platform: [ubuntu-latest, windows-latest, macos-latest]
    runs-on: ${{ matrix.platform }}
    name: Test
    steps:
      - uses: tlylt/install-graphviz@main
```

# Development

Updates will be done on the main branch. When ready, tag and release according to semver.

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)

