# Repolex Knowledge Graph of adamchainz/pytest-restrict

RDF knowledge graph data for [adamchainz/pytest-restrict](https://github.com/adamchainz/pytest-restrict), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download adamchainz/pytest-restrict
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4deef6fed138c6380ca3855313a98ab4805e4b1c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4deef6fed138c6380ca3855313a98ab4805e4b1c
│           └── chunk-001.nq.gz
├── blob
│   ├── 05d6d11c2ddffe38c4dfddc648609e39e217b0be.nq.gz
│   ├── 0f3524a3d8c34af10c39aaf4199c2af5e0bfe1e4.nq.gz
│   ├── 205ab9ad9df4ab629d1b7b8d8a72b41f44d8824c.nq.gz
│   ├── 22ddbb118475b52ce8ecba56d9ec45009923da58.nq.gz
│   ├── 2a7f84f54867d02714727f82eef95d3be939d666.nq.gz
│   ├── 30acc83b6797da94e6f047ba88ccfb5b934894ee.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 3e816915c4f7bbdb111ec3f3c07e5bb7cc0a0742.nq.gz
│   ├── 40f4ac757715bb1a8c355eda9124141fdda3aeff.nq.gz
│   ├── 438d629c3ce988e3afffa71110b9660853d38549.nq.gz
│   ├── 7f1d007c01048570d774e58f46203d3e92056c39.nq.gz
│   ├── 826cf1c573112a7ecde6cb65421a3ebc0491066c.nq.gz
│   ├── 888154126e0bffdd382468ea10780ec9cd190469.nq.gz
│   ├── 93acb639926ccf42e9a2f76f02419eeaf0405c3a.nq.gz
│   ├── cbe1d62d353e1468867c1ac699e6a64411e200d3.nq.gz
│   ├── cc4545a1222f182b8ac8205e6da7f2ec561b6384.nq.gz
│   ├── cdd89c5f491c97cf589eb332c35b72e4d4bec447.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f0a2abfa16717167b289159a2f38a41fde8a3457.nq.gz
│   └── f42ca091a2bc6228d5146fee576ed4e7c622fbae.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4deef6fed138c6380ca3855313a98ab4805e4b1c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[adamchainz/pytest-restrict](https://github.com/adamchainz/pytest-restrict)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
