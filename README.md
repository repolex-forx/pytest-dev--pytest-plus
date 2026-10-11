# Repolex Knowledge Graph of pytest-dev/pytest-plus

RDF knowledge graph data for [pytest-dev/pytest-plus](https://github.com/pytest-dev/pytest-plus), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-plus
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 8d78b89522ad0e7716a9fdc6337aacb6d848ad1e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 8d78b89522ad0e7716a9fdc6337aacb6d848ad1e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0709f9a46155b2f6c92b4dc98de324e7b35aff28.nq.gz
│   ├── 0e6fc72a7e2fe003b8f68965ed2759c443129db8.nq.gz
│   ├── 11fa6141ce4d3221741c9aa108d1ab6c67f258d3.nq.gz
│   ├── 4d2ea99c26f8ebb650cc41658ebe44088e6bb74b.nq.gz
│   ├── 53cfa20bba888c74c29fbf417b9719f3250d822b.nq.gz
│   ├── 88603f9ee9c271f1da5e9062826fe297b2ad9697.nq.gz
│   ├── 8a3a8cddc9208c1eb5f6983dba2f34928aa7ebbc.nq.gz
│   ├── 8d84a7a321b9543fbd2c297fcec3de384043f806.nq.gz
│   ├── 9fc7142ce9441c148c8fd84f9b12cca8418d8d2a.nq.gz
│   ├── accacd6b567e9b0ef6bd0a07fa29df5c9c362c57.nq.gz
│   ├── b4f95731eaab61b36e01e64ec05105a4b19cb596.nq.gz
│   ├── ba952063dd19d10fca5b55acddb7455d9d679293.nq.gz
│   ├── bbb2768241f170dc8eb928ed9e4f345ea3ece71f.nq.gz
│   ├── bc0b46031cc13b37bce266e0979440c5f881e5a1.nq.gz
│   ├── bf066f6a41c2a4bade46d11abd68e4c83491e450.nq.gz
│   ├── c2aa0a8d5b4fba9083350977249ca9b421c6c4a9.nq.gz
│   ├── c6241762a5c90b7ad1c497529d310c9f9e6c8fc4.nq.gz
│   ├── ca224b916146b215df301bb861f703bdd483cd6a.nq.gz
│   ├── cd1375683598d96eda005935d786fd28fa91e582.nq.gz
│   ├── d6e365b1f70bddf06cdf21b60696af755d946bbc.nq.gz
│   ├── dd87f502f369755ed6f1a90ace65fc4924294235.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eda45e3e94c6744f445b792e8fa0b7a3fb84abb7.nq.gz
│   ├── eef92a6b9a43158cb8a570bf8e2b283839fe8fa3.nq.gz
│   ├── f6abbd3ec409bda2ae950a46d5ab0c9f852eecff.nq.gz
│   └── fcfe0cc52ad38c5d1c511a19f9b1a00680c98681.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 8d78b89522ad0e7716a9fdc6337aacb6d848ad1e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[pytest-dev/pytest-plus](https://github.com/pytest-dev/pytest-plus)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
