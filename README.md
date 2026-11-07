# Repolex Knowledge Graph of locustio/k8s-operator

RDF knowledge graph data for [locustio/k8s-operator](https://github.com/locustio/k8s-operator), parsed by [repolex](https://repolex.ai).

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
rlex download locustio/k8s-operator
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ef9f2b726a8fcceb18552f5778dd697f9c5ca263
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ef9f2b726a8fcceb18552f5778dd697f9c5ca263
│           └── chunk-001.nq.gz
├── blob
│   ├── 04b0e53e8e9a84478480ca118563f265b472c98c.nq.gz
│   ├── 0f4eef89afde62a78013e5a70ae21b538410a0be.nq.gz
│   ├── 1d919e04bfdf4b69baed08def8ab9c2c6250e41f.nq.gz
│   ├── 1f3b77f4234158b12d659ef75d83a603e8774376.nq.gz
│   ├── 222be671bc4a4a8aa68d336d35f9713cf120faf1.nq.gz
│   ├── 380eb24d6bf875c499d3a5c47b47721ee70d7022.nq.gz
│   ├── 3ae30e50a2f40b888391ba87da11caefc79bbc58.nq.gz
│   ├── 3ef8950a992acf6e548a80065d61f26e00e5db27.nq.gz
│   ├── 4888a9b167add62ddb14214f5aa65116bf3a006f.nq.gz
│   ├── 583ab4c9c4d6f253e04b55ceb00827b5275ff199.nq.gz
│   ├── 5d881dce16c5664da39e854fd518e2e91f54cf02.nq.gz
│   ├── 5fe3fccf3fb20a0bbc2034cee1833958a4771c3a.nq.gz
│   ├── 621984d5c4e976a7d82e64a7d83c6d714a1e78bd.nq.gz
│   ├── 75b3600cf6af0482759afcf2bb50869e9d60fefc.nq.gz
│   ├── 847acfb6f435a173dea808512182eaed1e371437.nq.gz
│   ├── 8fa796ec731e161b8ebcf4b0072419a08f69082b.nq.gz
│   ├── 9039d643790b808c7a26abe570996339fffc5031.nq.gz
│   ├── a02058d71787e08c6f729a971ad37700f3b3bbbb.nq.gz
│   ├── b272829d1a0ba7ffb6ecf9fcfa6291ea55ce8786.nq.gz
│   ├── c5f3f40d76bd9af2beea78426f80605c181ad433.nq.gz
│   ├── cac7bebd208dd9b0500a638ad6af80bf3c44be5b.nq.gz
│   ├── db2edd78d1121146bc40b8abd3f977ca63dbad00.nq.gz
│   ├── dc09a7e3c2a707b254dc3f152e0a3420ea4eccbb.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ee4140c4a9fd6c3952e4d1898155f0de22cfd997.nq.gz
│   └── fc36bed312d3e5624f87fe1025282358c46f460a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ef9f2b726a8fcceb18552f5778dd697f9c5ca263.nq.gz
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

[locustio/k8s-operator](https://github.com/locustio/k8s-operator)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
