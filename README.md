# Repolex Knowledge Graph of astropy/pytest-remotedata

RDF knowledge graph data for [astropy/pytest-remotedata](https://github.com/astropy/pytest-remotedata), parsed by [repolex](https://repolex.ai).

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
rlex download astropy/pytest-remotedata
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5e6bbf150cd6c47dc05b6db28d787fecf952edd2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5e6bbf150cd6c47dc05b6db28d787fecf952edd2
│           └── chunk-001.nq.gz
├── blob
│   ├── 07c4d460fe5b4bed999cf759b77ff4419afbd497.nq.gz
│   ├── 0c082cc4daa1dc9586bb24ac268da09dd92f14c9.nq.gz
│   ├── 1110225936f4e04989a86a0dd1c6a484352ec8e0.nq.gz
│   ├── 1f89952dd4f6df2c466979159bfded697e8b97e7.nq.gz
│   ├── 381d874fd90c5cdbe8724a0a1f969370102635d4.nq.gz
│   ├── 51a2fc59a8c86c2f1b949e45b767c896a75d4c10.nq.gz
│   ├── 54a850a031b5b84c55dfdb1881cde9dcd306925a.nq.gz
│   ├── 59a01685d00983f3332f96d15a8ea3ebd58ada03.nq.gz
│   ├── 69a981ac22b8374710cb12d33df4926723a7cd15.nq.gz
│   ├── 72b3806a059359c52b6deb119157f537fa7b6442.nq.gz
│   ├── 730502d0262abc7ac6d0c24b42ab6de273805c05.nq.gz
│   ├── 814bd404d2a4de1e7bc3ce1efa07f03573595e88.nq.gz
│   ├── 827958933393df35badbc9a52c1286d50397bb7b.nq.gz
│   ├── 8b8ebcc690eccac11585517c67b0af23b63cf444.nq.gz
│   ├── b43eb7170f1e5e7a5efc3df31f745ed7d70a0e15.nq.gz
│   ├── b507b35474ebf2eb9aeb41a0a0b918e0c6c1464b.nq.gz
│   ├── bb34a538e5089eeb043bf0fc7b945e005753a771.nq.gz
│   ├── d78e1f16744fdf871cd4a60daa143ba91e9142bc.nq.gz
│   ├── dbf98108be67a2d6b2bc59afb568a1fc56797f2e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ef27aa41062b9c0cc43162f251ec449cacfb3ee7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5e6bbf150cd6c47dc05b6db28d787fecf952edd2.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[astropy/pytest-remotedata](https://github.com/astropy/pytest-remotedata)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
