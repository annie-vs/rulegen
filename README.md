# RuleGen

**Generate Pairwise test cases and coverage reports from business rule tables — no coding required.**

Download and run. Works on Windows without installing Python.

---

## What It Does

| You have | RuleGen generates |
|----------|------------------|
| A business rule Excel file | Pairwise test cases (`.xlsx`) |
| Parameters + value ranges | Pair coverage matrix (`.html`) |

**Example:** A rule table with 6 parameters → 13 test cases covering all pairwise combinations (brute force would require 144).

---

## Download

Go to [Releases](../../releases/latest) to download the latest version:

| Platform | File |
|----------|------|
| Windows 64-bit | `rulegen.exe` |

No installation needed. Run directly from the command line.

---

## Quick Start

**Step 1 — Generate example rule files (optional)**

```cmd
rulegen.exe example
```

Creates `insurance.xlsx`, `coupon.xlsx`, and `approval.xlsx` in the current directory. Use them as a reference for your own rule tables.

**Step 2 — Generate test cases**

```cmd
rulegen.exe generate your_rules.xlsx
```

Output:
- `output/cases.xlsx` — test case table
- `output/coverage.html` — pair coverage matrix (open in browser)

**Help**

```cmd
rulegen.exe --help
rulegen.exe generate --help
```

---

## Rule Table Format

An Excel file where each column is a parameter. Row 1 is the parameter name; remaining rows are the values:

| Age   | Region   | Coverage Level | Occupation  |
|-------|----------|----------------|-------------|
| <18   | Domestic | Basic          | White-collar|
| 18-60 | Overseas | Standard       | Blue-collar |
| >60   |          | Premium        | Other       |

See the [examples/](examples/) directory for ready-to-use sample files.

---

## Feedback & Contributions

File an issue to:

- **[Report a Bug](../../issues/new?template=bug_report.md)** — crashes, wrong output
- **[Submit a Parse Failure](../../issues/new?template=parse_failure.md)** — attach your rule table (anonymized) to help improve parsing
- **[Contribute Industry Rules](../../issues/new?template=rule_submission.md)** — share rule templates from your domain
- **[Request a Feature](../../issues/new?template=feature_request.md)** — suggest improvements or new capabilities

---

## Changelog

See [CHANGELOG.md](CHANGELOG.md)

---

## License

Free to use (including commercial use). Source code is not open. See [LICENSE](LICENSE).