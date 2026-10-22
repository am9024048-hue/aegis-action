[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
# Aegis Security Action 🛡️

Automated SAST & Security Scanner for Python in GitHub Actions.

Aegis Security Action is an enterprise-grade Static Application Security Testing (SAST) tool designed to detect security vulnerabilities, dangerous coding patterns, and hardcoded secrets directly inside your CI/CD pipeline.

### ✨ Key Features
* **Zero Configuration:** Seamlessly integrates into any Python repository in seconds.
* **Continuous CI/CD Security:** Automatically scans every Push and Pull Request before code reaches production.
* **Privacy-First & Fast:** Runs AST-based security analysis directly within your runner environment without sending source code to external servers.
* **Developer-Friendly Output:** Clear and actionable error reporting to fix security issues faster.

### 🚀 Quick Start
Add the following workflow file to your repository at `.github/workflows/security.yml`:

name: Aegis Security Scan
on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]
jobs:
  security-check:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Code
        uses: actions/checkout@v4
      - name: Run Aegis Security Action
        uses: am9024048-hue/aegis-action@v1.0.0
        with:
          path: '.'

### ⚙️ Inputs
* `path`: The relative path of the directory you want to scan (Optional, Default: '.').

### 🗺️ Roadmap & Enterprise Support
* **v1.0.0:** Automated Python SAST & Secret Detection in GitHub Actions.
* **v1.1.0:** Native SARIF report generation for GitHub Code Scanning integration.
* **v2.0.0:** Polyglot support (JavaScript/TypeScript, Go) powered by Tree-sitter.

### 📄 License
This project is licensed under the MIT License.

