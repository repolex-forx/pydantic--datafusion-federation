# Repolex Knowledge Graph of pydantic/datafusion-federation

RDF knowledge graph data for [pydantic/datafusion-federation](https://github.com/pydantic/datafusion-federation), parsed by [repolex](https://repolex.ai).

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
rlex download pydantic/datafusion-federation
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 36b0d03a08cbe9f6f968fa4b72de430cfef3410e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 36b0d03a08cbe9f6f968fa4b72de430cfef3410e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0bee170cb8e17a51ba3763271d63b835483048c3.nq.gz
│   ├── 0f1e299a1e922a9c8e1f837654209b8008e5b8ff.nq.gz
│   ├── 155b39284cc021d7818c7f30a3b51941bde0aa88.nq.gz
│   ├── 1fb0772d56aea2b2c166968b487eef53b6099dcb.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 377b4694aef709bef4300f911e7d9fe21dea8fe8.nq.gz
│   ├── 42d433c543d742b3e4f972bb9d1cf5afe9328c33.nq.gz
│   ├── 4891b12fe107bd239278531ae7580b967a9a3475.nq.gz
│   ├── 4b1999011790c7f8951c75e512131cdd2434f33a.nq.gz
│   ├── 4c3b2b7f8a4ab3f850e0fc473d8345eb2214b9f2.nq.gz
│   ├── 53d1f2663d4c46de4e8c5c01580a3bfbfdc3037d.nq.gz
│   ├── 5fbd8060d7cef7bad577308ed71477f626aeb332.nq.gz
│   ├── 639cff4dd5b6ec1e8b310890b090f77186a0b229.nq.gz
│   ├── 64a60bb1cff3756e2b59ed43a6232d894b572409.nq.gz
│   ├── 6da1eb1d171719a215873e62d3b87ea10548c907.nq.gz
│   ├── 79af1c1d22d553b10e8bb860a88ff2c55fe2c642.nq.gz
│   ├── 7ee8cf824921379d5633056db53ea5bfe4222726.nq.gz
│   ├── 8844cd2d8c1f773b76a00dff7d6b683f7ab11a4e.nq.gz
│   ├── 8971e72f94d58950e6783f69da1e9ea46387bacf.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── 8c07d996748492fc4d3d0ff616792a9da31ff639.nq.gz
│   ├── 9c16dfc03a9e58e57a75edb5243e97eb0f081659.nq.gz
│   ├── a3675b754b694588c9c87ff08ea5e67651d7b598.nq.gz
│   ├── a6dad0aeb1a02e158b1c6eb85d7ae2a7d64029cc.nq.gz
│   ├── aca2cccaeb55e5720b1fa8c5a6eda1f46dc95ca4.nq.gz
│   ├── b10725ea2404fa177f7199e89e203f2df82f939d.nq.gz
│   ├── c2371329e3ab9d55cc0ecaaa677822fd11822790.nq.gz
│   ├── c71c6abff1a44c7fc2742a0f78bb48e39c83a87e.nq.gz
│   ├── e34f1bbb290a2a318d4b8104df7a74619c3c1138.nq.gz
│   ├── e7b709f97a2f81a814d12bdf8b11934b7400b217.nq.gz
│   └── e974d2456725ab4bd1103deb678a207009ff0816.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 36b0d03a08cbe9f6f968fa4b72de430cfef3410e.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 37 files
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

[pydantic/datafusion-federation](https://github.com/pydantic/datafusion-federation)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
