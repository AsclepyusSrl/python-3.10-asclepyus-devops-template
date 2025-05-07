# Asclepyus Python Project Template

An internal Python project template for Asclepyus projects, featuring automated setup and release management.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Quick Start](#quick-start)
- [Development Setup](#development-setup)
- [Creating Releases](#creating-releases)
- [Documentation](#documentation)
- [Project Structure](#project-structure)

## Features

- 🚀 Automatic project renaming and configuration
- 📦 UV for dependency management
- 📝 MkDocs for documentation
- 🔄 Automated releases with semantic versioning using GPT and Changelog Weaver
- ✨ Pre-commit hooks for code quality
- 🧪 Ready for testing

## Prerequisites

1. GEMINI API KEY
   - Requires a Gemini API key and  be stored as an repository secret named `GEMINI_API_KEY`
   - Click here to generate your own personal api key https://aistudio.google.com/app/apikey

2. GPT API KEY
   - Requires a GPT API key and  be stored as an repository secret named `GPT_API_KEY`

3. FEATURE_PRAGENT
   - Requires a boolean value and  be stored as an repository Variable named `FEATURE_PRAGENT`
   - Default value is `true`

4. FEATURE_DOCS
   - Requires a boolean value and  be stored as an repository Variable named `FEATURE_DOCS`
   - Default value is `true`

5. FEATURE_CI
   - Requires a boolean value and  be stored as an repository Variable named `FEATURE_CI`
   - Default value is `true`

6. FEATURE_CD
   - Requires a boolean value and  be stored as an repository Variable named `FEATURE_CD`
   - Default value is `true`

7. Workflow PAT
   - Requires a Workflow PAT and  be stored as an Organization secret named `Workflow_PAT` (Should be done by the Administrator)

## Quick Start

1. Click the "Use this template" button at the top of this repository
2. Clone your new repository
3. The template will automatically configure itself on your first push:
   - Renames all placeholder references
   - Sets up the project structure
   - Configures GitHub Actions

## Development Setup

Run the setup script:
```bash
./setup.bat
```
```bash
.venv\Scripts\activate
```

## Creating Releases

Releases are automatically created when you push to main. The version bump is determined by PR labels and/or description:
- `major`: Breaking changes
- `minor`: New features
- `patch`: Bug fixes

## Documentation

- Run locally:
  ```bash
  poetry run mkdocs serve
  ```
- View at: http://localhost:8000

## Project Structure

```
├── .github/          # GitHub Actions workflows and templates
├── docs/            # Documentation
├── src/             # Source code
    └── package_name/ # Default package (will be renamed to your repository name)
└── tests/           # Test files
```

> **Note**: By default, the package name under `src/` will be set to your repository name. If you want to use a different name, make sure to also update the package name in the [release workflow](.github/workflows/release.yml#L34).

## License

This project is licensed under the MIT License - see the LICENSE file for details.