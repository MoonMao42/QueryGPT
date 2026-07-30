<div align="center">

<img src="docs/images/receiptbi-icon.png" width="144" alt="ReceiptBI logo">

# ReceiptBI

**Turn CSV, Excel, and read-only databases into verified, editable business reports.**

[Download the desktop app](https://github.com/MoonMao42/ReceiptBI/releases/latest) · [Try the sample](#try-the-sample) · [中文](README.md)

[![CI](https://github.com/MoonMao42/ReceiptBI/actions/workflows/ci.yml/badge.svg)](https://github.com/MoonMao42/ReceiptBI/actions/workflows/ci.yml)
[![Release](https://img.shields.io/github/v/release/MoonMao42/ReceiptBI?label=release)](https://github.com/MoonMao42/ReceiptBI/releases/latest)
[![License](https://img.shields.io/github/license/MoonMao42/ReceiptBI)](LICENSE)

</div>

![Reviewing report pages and moving into the editing layout](docs/images/demo/receiptbi-report-demo.gif)

<p align="center"><sub>Interact with databases, Excel files and more via natural language (read-only). Generate charts and summaries.</sub></p>

## Try the sample

1. Install the [ReceiptBI desktop app](https://github.com/MoonMao42/ReceiptBI/releases/latest), or run it from source.
2. Download the [coffee retail order sample](examples/retail/orders.csv).
3. Choose a model provider in Settings, then add the sample file to your project.
4. Ask:

> Analyze sales, gross profit, and refunds for the latest month. Compare regions and channels.

## Download

The current version is [ReceiptBI 1.0.0](https://github.com/MoonMao42/ReceiptBI/releases/tag/v1.0.0).

<details>
<summary><strong>First launch on macOS</strong></summary>

1. Open the DMG and move ReceiptBI to Applications.
2. The current 1.0.0 build is unsigned. If macOS blocks the first launch, run in Terminal:

```bash
xattr -cr /Applications/ReceiptBI.app
```

</details>

## Features

### Full analysis process with highlights and charts

![An investigation with key metrics, findings, and charts](docs/images/en/workspace-analysis.png)

### AI-generated semantic layer per data source

![Business definitions organized by data source and table](docs/images/en/semantic-governance.png)

### Convert to editable reports

![Reviewing an investigation before organizing it into a report](docs/images/en/report-organizing.png)

### Preview pagination before export

![A paginated report print preview](docs/images/en/report-print-preview.png)

<div align="center">

[⭐ Star ReceiptBI](https://github.com/MoonMao42/ReceiptBI)

</div>

## How it works

```mermaid
flowchart LR
    data["Files / Read-only DBs"] --> prep["Prepare data"]
    prep --> semantic["Confirm business context"]
    semantic --> ask["Ask a question"]
    ask --> run["Analyze"]
    run --> validate["Check the evidence"]
    validate -->|Needs another pass| run
    validate --> report["Editable report"]
```

Confirmed data preparation steps and business definitions are saved. When data updates but the schema stays the same, you can reuse existing definitions to re-run analysis and refresh reports.


## Previous versions

| Version | Based on | Branch |
|---|---|---|
| v2 | [gptme](https://github.com/gptme/gptme) | [v2](https://github.com/MoonMao42/ReceiptBI/tree/v2) |
| v1 | [Open Interpreter 0.4.3](https://github.com/OpenInterpreter/open-interpreter) | [v1](https://github.com/MoonMao42/ReceiptBI/tree/v1) |

## License

[MIT](LICENSE)
