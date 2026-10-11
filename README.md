# Repolex Knowledge Graph of pallets-eco/flask-environments

RDF knowledge graph data for [pallets-eco/flask-environments](https://github.com/pallets-eco/flask-environments), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/flask-environments
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6a6cb75ad2c29435d74768aa88c5d925570a6ad0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6a6cb75ad2c29435d74768aa88c5d925570a6ad0
│           └── chunk-001.nq.gz
├── blob
│   ├── 1e800de895412aa8ce24b20153a533c46cabf1d6.nq.gz
│   ├── 23d1773c9bce8c85ef767ff6666d42ad93ca082b.nq.gz
│   ├── 2b1a4f0b9c203602ddb36d0d6ba3939d49e86e11.nq.gz
│   ├── 2d56772a58865f2c343e65a2fb04ac04ecd67d03.nq.gz
│   ├── 35a2ae899e4a7bb589c25a99e6199c90c5bf4af3.nq.gz
│   ├── 48a68f67f7ea3a8bf081fd732db59e42017553d5.nq.gz
│   ├── 4f585fef999a504cf87ab6c8581e17405f72af26.nq.gz
│   ├── 52fde3ad1ff8a7af1356e437e7a6e1a3b2a72dfa.nq.gz
│   ├── 793736dcf3f95366c06343c33076fd0d9f5664c4.nq.gz
│   ├── 9139bc828a943e2957da38bc7f19bead0edf2cf8.nq.gz
│   ├── bf7b494fc7044e1395c1c821f2babc309277bf78.nq.gz
│   ├── e0f7c7213711eba60d32da1341f1170cadeb0c23.nq.gz
│   └── f30bdd66d152cb3ef358ac38d5ae46ea36629b9a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6a6cb75ad2c29435d74768aa88c5d925570a6ad0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[pallets-eco/flask-environments](https://github.com/pallets-eco/flask-environments)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
