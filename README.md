# calm-advent-2025

A 24-day hands-on challenge to dive deep into CALM concepts, model real-world identity architectures, and contribute meaningfully to the FINOS community — built as part of my security and open source development journey.

# My Advent of CALM Journey

This repository tracks my 24-day journey learning the Common Architecture Language Model (CALM).

## 📅 Challenge Summary

Each day, I complete a small architectural modeling task, document it, and commit it as a milestone.

- ✅ Uses [CALM CLI](https://www.npmjs.com/package/@finos/calm-cli)
- ✅ Structure powered by Git + GitHub Copilot (optional)
- ✅ One folder per day with its own README

## Table of Contents

| Day | Challenge Title | Status | Link |
|-----|------------------|--------|------|
| 1   | Install CALM CLI & Initialize Repo | ✅ Complete | [Day 1](advent/day-01/) |
| 2   | Define initial architecture and create first system node| ✅ Complete| [Day 2](advent/day-02/) |
| 3   | Connect Nodes with Relationships | ✅ Complete | [Day 3](advent/day-03/) |
| 4   | Install CALM VSCode Extension | ✅ Complete | [Day 4](advent/day-04/) |
| …   | _More Coming Soon_ | 🔜 | - |

## 📁 Repo Structure

## Architectures

This directory will contain CALM architecture files documenting systems.

## Patterns

This directory will contain CALM patterns for architectural governance.

## Docs

Generated documentation from CALM models.

## Tools

### 1. CALM CLI

**Installed**: Day 1

**Purpose**: Command-line interface for generating, validating, and transforming CALM architectures.

**What it's used for**:
- **Generation** – Create architectures from patterns: `calm generate -p pattern.json`
- **Validation** – Check compliance with schema: `calm validate -a architecture.json`
- **Templates** – Generate documentation/reports: `calm template -a architecture.json -o output/`
- **Docify** – Create HTML documentation: `calm docify -a architecture.json -o docs/`

**Basic commands**:
```bash
# Validate architecture
calm validate -a architectures/ransomware-defense-architecture.architecture.json

# Generate from pattern
calm generate -p patterns/my-pattern.json -o generated-arch.json

# Generate documentation
calm docify -a architecture.json -o ./docs
```

---

### 2. CALM VSCode Extension

**Installed**: Day 4

**Marketplace**: https://marketplace.visualstudio.com/items?itemName=FINOS.calm-vscode-plugin

**What it provides**:
- **Live Preview** – See real-time visualization of your CALM architecture as you edit
- **Tree Navigation** – Hierarchical view of nodes, relationships, flows, and controls
- **Syntax Highlighting** – JSON schema-aware editing with auto-completion
- **Error Detection** – Immediate feedback on schema violations
- **Interactive Exploration** – Click nodes to inspect properties and relationships

**Keyboard Shortcut**:
- **Open Preview**: `Ctrl+Shift+C` (Windows/Linux) or `Cmd+Shift+C` (macOS)

---

### 3. How These Tools Work Together

**Workflow**:

1. **Edit in VSCode** → CALM Extension provides live preview and validation feedback
2. **Refine Architecture** → Use extension to visualize and navigate structure
3. **Validate via CLI** → `calm validate` confirms full schema compliance and catches Spectral errors
4. **Generate Documentation** → `calm docify` creates shareable HTML documentation
5. **Version & Deploy** → Commit validated architecture to repository

**Synergy**:
- **Extension** = Real-time authoring and visual feedback during development
- **CLI** = Comprehensive validation, automation, and batch processing
- **Together** = Fast iteration + reliable compliance enforcement

Example workflow:
```bash
# 1. Edit ransomware-defense-architecture.architecture.json in VSCode
#    (Extension shows live preview)

# 2. Run validation to catch any issues
calm validate -a architectures/ransomware-defense-architecture.architecture.json

# 3. Generate documentation for stakeholders
calm docify -a architectures/ransomware-defense-architecture.architecture.json -o docs/ransomware/

# 4. Commit to repository
git add architectures/ docs/
git commit -m "Add ransomware defense architecture with documentation"
```

---

## Notes

- Extension preview updates in real-time as you type JSON
- CLI validation catches both JSON schema and Spectral rule violations
- Use CLI in CI/CD pipelines for automated architecture compliance checks