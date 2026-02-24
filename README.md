# workflows

> fork from [sxzz/workflows](https://github.com/sxzz/workflows/)

A collection of reusable GitHub Actions workflows and actions for CRXJS projects.


## Actions

- [Setup JS](setup-js/action.yml): Setup Node.js and install dependencies
- [Release](release/action.yml): Release a new version of the project

## Usage

To use a workflow, reference it in your project’s .github/workflows/*.yml:

### Example: Release 
```yaml
name: Release

on:
  push:
    tags:
      - 'v*'

jobs:
  release:
    uses: crxjs/workflows/release.yml@v1
    with:
      publish: true
    permissions:
      contents: write
      id-token: write
```

## Contributing

Contributions and suggestions are welcome! Please open issues or pull requests.

