# batchask

Run a JSONL of prompts through an LLM, results to JSONL

Small but I use it weekly.

## Highlights

- JSONL in, JSONL out: stream-safe for huge inputs
- Concurrent workers with a rate ceiling
- Idempotent: skips ids already present in the output
- Retries failed items with backoff, logs them aside

## Usage

```bash
python batch.py prompts.jsonl -o answers.jsonl --workers 4
```

## Installation

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   └── dependabot.yml
├── docs/
│   ├── configuration.md
│   └── usage.md
├── tests/
│   └── test_smoke.py
├── .editorconfig
├── .gitattributes
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── batch.py
├── prompts.sample.jsonl
└── requirements.txt
```

## License

MIT. Do whatever you want.
