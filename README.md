# Repolex Knowledge Graph of expressjs/method-override

RDF knowledge graph data for [expressjs/method-override](https://github.com/expressjs/method-override), parsed by [repolex](https://repolex.ai).

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
lexq download expressjs/method-override
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5b83d4f0dc3db414df6c7e4a5da93dec170153de
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 5b83d4f0dc3db414df6c7e4a5da93dec170153de.nq.gz
│   └── repolex
│       └── 5b83d4f0dc3db414df6c7e4a5da93dec170153de
│           └── chunk-001.nq.gz
├── blob
│   ├── 0fa6951f088d91e437ea25699ee715cc6cf462a0.nq.gz
│   ├── 25a2f0f525ff824ea4391b4c4acf041a780c88a3.nq.gz
│   ├── 53e49a3821327050867cf866d9e1416a1f50750a.nq.gz
│   ├── 58e636c911dc91bcb5a95f17d6a491cc7def6fcd.nq.gz
│   ├── 62562b74a3b5a79e82ca417b02e0f597d85f5e2f.nq.gz
│   ├── 7eeefc33b66c055f211388c46d17b50c45db7c25.nq.gz
│   ├── 830b2ee0a97b9aafa4168c5678e099e594e52357.nq.gz
│   ├── c754bca3b500f3b3378a8aae744972d05badb0f1.nq.gz
│   ├── e256c2bcbf81b53a51c5bb9668da35fb74303a1c.nq.gz
│   ├── e3578aadfd3a97c6ef9d74f46e07314d775c9c61.nq.gz
│   └── e6dd59b69d8260d3df76c689e397e9b6174e62c8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 5b83d4f0dc3db414df6c7e4a5da93dec170153de.nq.gz
├── filetree
│   └── 5b83d4f0dc3db414df6c7e4a5da93dec170153de.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 21 files
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

[expressjs/method-override](https://github.com/expressjs/method-override)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
