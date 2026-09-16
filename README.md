# Repolex Knowledge Graph of ipython/matplotlib-inline

RDF knowledge graph data for [ipython/matplotlib-inline](https://github.com/ipython/matplotlib-inline), parsed by [repolex](https://repolex.ai).

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
lexq download ipython/matplotlib-inline
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 30bf01b0774d92bbff91a7738b9eef3ba4a55fa6
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 30bf01b0774d92bbff91a7738b9eef3ba4a55fa6.nq.gz
│   └── repolex
│       └── 30bf01b0774d92bbff91a7738b9eef3ba4a55fa6
│           └── chunk-001.nq.gz
├── blob
│   ├── 21c64188ce2e8d30179dc10242f133b0d65b3964.nq.gz
│   ├── 329e3e782941ce0df871a24ba6c1988c34d9d68f.nq.gz
│   ├── 3b292824d15a68bbc788913c738cc896867e42f2.nq.gz
│   ├── 4784e9a0caab5779079c23ab92d4d249a32f8c62.nq.gz
│   ├── 75e4c5d57e909f0e6bc12223b000bc5d0cad5c39.nq.gz
│   ├── 86c88c328c0085ddedcbc01797ba95a91a900374.nq.gz
│   ├── 9d1ededb922dc0a11cd574f94741bfe00bddc841.nq.gz
│   ├── a798c562a7fa6c07d32e6e0dd742d0e6c711b699.nq.gz
│   ├── a862d83fc07042ef7a5058a8d314789910bf2aa6.nq.gz
│   ├── b8350378e810121d96bc065a8ddaab7d2ec38308.nq.gz
│   ├── c816b29836cfe958e74f8f11c5f4ddf8f0ead2b7.nq.gz
│   ├── ce9be032fbd3af9563facf42d5b950990b03317e.nq.gz
│   ├── d275175ecd970d64aa94db01b833fd4ebf7ce1ea.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fd328375991f666cf2ccffc80338357a98c34178.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 30bf01b0774d92bbff91a7738b9eef3ba4a55fa6.nq.gz
├── filetree
│   └── 30bf01b0774d92bbff91a7738b9eef3ba4a55fa6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 25 files
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

[ipython/matplotlib-inline](https://github.com/ipython/matplotlib-inline)

---
*Parsed on 2026-09-16 by [repolex](https://repolex.ai)*
