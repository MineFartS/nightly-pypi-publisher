# Nightly PyPi Publisher

This action automates the compilation and deployment of C++20 python extension packages.

## Usage

```yaml
# .github/workflows/*.yml

name: Nightly Build

on:
  workflow_dispatch:
  schedule:
    - cron: '0 3 * * *'

permissions:
  contents: write
  id-token: write

jobs:
  build-and-publish:
    uses: minefarts/nightly-pypi-publisher/.github/workflows/run.yml@v2
    secrets:
      PYPI_API_TOKEN: ${{ secrets.PYPI_API_TOKEN }}

```
