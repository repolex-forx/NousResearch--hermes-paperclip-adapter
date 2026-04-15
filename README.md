# Repolex Knowledge Graph of NousResearch/hermes-paperclip-adapter

RDF knowledge graph data for [NousResearch/hermes-paperclip-adapter](https://github.com/NousResearch/hermes-paperclip-adapter), parsed by [repolex](https://repolex.ai).

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
lexq download NousResearch/hermes-paperclip-adapter
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bcca625618394a98af7555bbbc2faa05005776ab
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── bcca625618394a98af7555bbbc2faa05005776ab.nq.gz
│   └── repolex
│       └── bcca625618394a98af7555bbbc2faa05005776ab
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d699789cf34c2840693959f6b68e2a4d8506d7d.nq.gz
│   ├── 116efc5ef9f7d25b493a9fd8b65af295c1799a22.nq.gz
│   ├── 1d77b90a4407dd513d808925479f2efaf989a83a.nq.gz
│   ├── 2177ef66279071901f17bec5dd6b88a8af823064.nq.gz
│   ├── 3a49f112093b53cb97f9af82c8220d1a1c30f25e.nq.gz
│   ├── 3d201e419478b1f94891ae9600ef44151b0f6d45.nq.gz
│   ├── 3e0d1659ac7fded27bf21a4df750422415aa2f8a.nq.gz
│   ├── 5700b997827973cb0eb6d84a2782bb08a5872434.nq.gz
│   ├── 5f44bbeb4d89fe2f5f55e022367ca9b341fb76df.nq.gz
│   ├── 64ad2df8887ab38b4e70c6f40efb58392f31cc3a.nq.gz
│   ├── 9cb200afa0ad93c4fbd8b54064141e9d8e7cb255.nq.gz
│   ├── b1bfd01a432c37eab971e4b41b5f1f252d85e440.nq.gz
│   ├── b2ac8e6e060e342f8bb0ced3d5f2b1339d808cea.nq.gz
│   ├── d102dd64e5ad1f4c44d1a4406ee500f3f86b42bb.nq.gz
│   ├── d5c54ad33eb68ecb32a644552cff6a14c31dc408.nq.gz
│   ├── f08c3c9d2c7ad8780864b69002111975cb436b7f.nq.gz
│   └── fe7114403b4ce31d0cfd32316df48237ed0d52a7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── bcca625618394a98af7555bbbc2faa05005776ab.nq.gz
├── filetree
│   └── bcca625618394a98af7555bbbc2faa05005776ab.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 27 files
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

[NousResearch/hermes-paperclip-adapter](https://github.com/NousResearch/hermes-paperclip-adapter)

---
*Parsed on 2026-04-15 by [repolex](https://repolex.ai)*
