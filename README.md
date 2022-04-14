# install-graphviz

This action provides the following functionality for GitHub Actions users:

- Install Graphviz cross-platform (Linux, macOS, Windows)

# Usage

This action will detect the operating system and install Graphviz cross-platform. You may use the action without any additional parameters.

```yaml
steps:
- uses: tlylt/install-graphviz@main
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

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)

