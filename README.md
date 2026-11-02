# Repolex Knowledge Graph of zopefoundation/zExceptions

RDF knowledge graph data for [zopefoundation/zExceptions](https://github.com/zopefoundation/zExceptions), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/zExceptions
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0da83f1f967d8b0cb165b756bce42229b6fe75a6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0da83f1f967d8b0cb165b756bce42229b6fe75a6
│           └── chunk-001.nq.gz
├── blob
│   ├── 00237fed268f9d8587518bfb09bc0eeebe16a3cd.nq.gz
│   ├── 0fc8b1cb8e9db5a7df3d7ebba507ac713e991b9f.nq.gz
│   ├── 143b70e8666042556e1a264f1f818c4d48fcddec.nq.gz
│   ├── 1c6cad9db779d3a279810e356c50c08a08157e6b.nq.gz
│   ├── 2492f5d9e613de00deeb4ac671dbcdab9d6879bf.nq.gz
│   ├── 2e81cad90f6cc905a19da82ad81b737649e7270c.nq.gz
│   ├── 3a960de95530d83374fd6a96950157d7bc0933e3.nq.gz
│   ├── 3d70b7b9ed233260fc93dff8dc93a8a33039b50e.nq.gz
│   ├── 4bd670f9ed2c79d43ac4356c52c9403f1d618e7c.nq.gz
│   ├── 59628d6ca2d1c31ee96806973ce93af4908adc2c.nq.gz
│   ├── 623fa469a6a921299e79918b06678a76f9042013.nq.gz
│   ├── 7b4fbd9b8024313b9e9040e3335e481fb62dd78f.nq.gz
│   ├── 8ef0bc9bf18265fb94acea71418f865a98437cdb.nq.gz
│   ├── 9269c796605870e977bc1a5b4a9216c047df09fc.nq.gz
│   ├── b8581dd898cbb33e63961b4d181ff0ffbe5d03ee.nq.gz
│   ├── c0c8f5972aafd9f8568c8058e638708499d1727b.nq.gz
│   ├── ca517f4eb0cec1c691c0c2b54cd5eb85e906f11b.nq.gz
│   ├── dbb40fe06168a03ece18556f731f08236e4d04ea.nq.gz
│   ├── e184fd8f41cbc229060cf69967d916bf6e2ddf2a.nq.gz
│   ├── e1f9ad7b3b48377bfbfaa1b380c384ddea24060f.nq.gz
│   ├── e25bb2b50bae2076d00225d4d64ea7c6b4992f0a.nq.gz
│   ├── e4b867329e05886a4818f86b117fca2102bc84bf.nq.gz
│   ├── e5a05b0b3a40889c4f797b786ebc8de931f2fff8.nq.gz
│   ├── e82170842bf159d9fb07bbc03630fc9ba2995e92.nq.gz
│   ├── f507feda73c43de02c9268ef502bc4c3a2ebf32d.nq.gz
│   └── fa1d12e0d60d99c8339987524ef656da2dc93d16.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0da83f1f967d8b0cb165b756bce42229b6fe75a6.nq.gz
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

[zopefoundation/zExceptions](https://github.com/zopefoundation/zExceptions)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
