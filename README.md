# Repolex Knowledge Graph of remithomas/eslint-plugin-ban

RDF knowledge graph data for [remithomas/eslint-plugin-ban](https://github.com/remithomas/eslint-plugin-ban), parsed by [repolex](https://repolex.ai).

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
lexq download remithomas/eslint-plugin-ban
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 312d84e2c6b18df2ddfeef7ae6f4f4af4bee4e31
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 312d84e2c6b18df2ddfeef7ae6f4f4af4bee4e31.nq.gz
│   └── repolex
│       └── 312d84e2c6b18df2ddfeef7ae6f4f4af4bee4e31
│           └── chunk-001.nq.gz
├── blob
│   ├── 0a725205c885956a06a70bd9ab7552f9eb164dd1.nq.gz
│   ├── 2166dc5cf0eb0977f8f729b94cd7140eeaf5ee96.nq.gz
│   ├── 3695c2b85bab2337ab8ea63381f77746a91e6bc5.nq.gz
│   ├── 3abb837bea8385d89c8fa6f428f809d011c30e29.nq.gz
│   ├── 5c42eede2c6c092878094644925a2d50d17de871.nq.gz
│   ├── 62165190346dbb524cdf073a96e9e3f4feedfc74.nq.gz
│   ├── 779f99a12b5c71692ad6d6908d6d2fc3bdba485d.nq.gz
│   ├── 7d1c138e2d89ee5e731f4239b46153009c9072ff.nq.gz
│   ├── 812b064b6d5db77eaeedbbbbfb2eea98b644a1b8.nq.gz
│   ├── 91cc34331df630f330f04bcf547bbd2b226982dc.nq.gz
│   ├── ae1f89f7c5ef3ad7303ec13c6d80f9e7080ae52d.nq.gz
│   ├── c6a703d6720a52686e4143d06f5a6024b776fcb7.nq.gz
│   ├── eecc2c3967e36b72bf2cf87a1ea2901d38acc6af.nq.gz
│   └── fbb6811c77672312bd98005dd9bd21134d1c9999.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 312d84e2c6b18df2ddfeef7ae6f4f4af4bee4e31.nq.gz
├── filetree
│   └── 312d84e2c6b18df2ddfeef7ae6f4f4af4bee4e31.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 24 files
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

[remithomas/eslint-plugin-ban](https://github.com/remithomas/eslint-plugin-ban)

---
*Parsed on 2026-04-09 by [repolex](https://repolex.ai)*
