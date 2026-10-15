# Repolex Knowledge Graph of jupyter-server/jupyter_server_mathjax

RDF knowledge graph data for [jupyter-server/jupyter_server_mathjax](https://github.com/jupyter-server/jupyter_server_mathjax), parsed by [repolex](https://repolex.ai).

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
rlex download jupyter-server/jupyter_server_mathjax
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 286f3852ae2490f649c663638f3f2f2503599cf8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 286f3852ae2490f649c663638f3f2f2503599cf8
│           └── chunk-001.nq.gz
├── blob
│   ├── 0033efc0b86f61d59270818ad798a7704544cad4.nq.gz
│   ├── 0722960e516e7c8def9000426db4faf86dff0cdb.nq.gz
│   ├── 12db427fd4082ef3c2100b71d8a3531f75812051.nq.gz
│   ├── 14dcfad379ba3b949f237ed4365633d2306d2648.nq.gz
│   ├── 1874003e7d1223a2aa052c3b5a3ff78c5365f505.nq.gz
│   ├── 32ba6fc0b3e0790be337caa791012c880f4b9d80.nq.gz
│   ├── 32d86be31c0d187155f1bea7a3af8208210d48a2.nq.gz
│   ├── 44d0f243b9c4c43692083490dbc479643354ea53.nq.gz
│   ├── 4a456f726d7799f430b05ea12dd769ab89bad665.nq.gz
│   ├── 660aabc3e34c041274b4e381b70ac01a7305eb16.nq.gz
│   ├── 72a37ea142417e9cda6d5fd7dd12295539edb0a0.nq.gz
│   ├── 7f652648d222565ac8c87f2de2dbbde8281a4a09.nq.gz
│   ├── 974f85e6e3324919fdc1b6cb5965b798917c56bd.nq.gz
│   ├── 9dfa5688301fe13b7b948f3ddf9a5788bc5d57c5.nq.gz
│   ├── ab5fef452545691608abb03d30f0ce36818b9a89.nq.gz
│   ├── c22984cb8705b94cd89a4633fd18d6507c01b01c.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── edddc1a6e516e1dee038d376550d175924a83ef3.nq.gz
│   └── f1c2c50335bc1639a5aefa3523cb998ea76a3a7d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 286f3852ae2490f649c663638f3f2f2503599cf8.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[jupyter-server/jupyter_server_mathjax](https://github.com/jupyter-server/jupyter_server_mathjax)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
