# Repolex Knowledge Graph of component/escape-html

RDF knowledge graph data for [component/escape-html](https://github.com/component/escape-html), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download component/escape-html
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7ac2ea3977fcac3d4c5be8d2a037812820c65f28
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 7ac2ea3977fcac3d4c5be8d2a037812820c65f28.nq.gz
│   └── repolex
│       └── 7ac2ea3977fcac3d4c5be8d2a037812820c65f28
│           └── chunk-001.nq.gz
├── blob
│   ├── 229e92e329df3f35af678cd588fcea6729b72fce.nq.gz
│   ├── 2e70de9717e715b4fc05c7f8bdc4e8d63a33b859.nq.gz
│   ├── 3f6119d227040d0493452f89e06013b2a9886da6.nq.gz
│   ├── 57ec7bd0754d50af9c5e96a208aed6d85c1e6d5e.nq.gz
│   ├── 653d9eaa793317827ce724c4a0756110e9356fc8.nq.gz
│   ├── bf9e226f4e872bee53a930739e5381d013c47568.nq.gz
│   ├── c21125b81c512007c68bd255c454532125833398.nq.gz
│   └── e78ec7cd37816f55e7e0201e8a6013b06cd5f210.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 7ac2ea3977fcac3d4c5be8d2a037812820c65f28.nq.gz
├── filetree
│   └── 7ac2ea3977fcac3d4c5be8d2a037812820c65f28.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 18 files
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

## Source repository

[component/escape-html](https://github.com/component/escape-html)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
