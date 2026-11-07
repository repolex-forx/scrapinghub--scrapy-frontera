# Repolex Knowledge Graph of scrapinghub/scrapy-frontera

RDF knowledge graph data for [scrapinghub/scrapy-frontera](https://github.com/scrapinghub/scrapy-frontera), parsed by [repolex](https://repolex.ai).

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
rlex download scrapinghub/scrapy-frontera
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 56ea2e1ef39a174eac61da2edcdb21d1f1ecf5e5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 56ea2e1ef39a174eac61da2edcdb21d1f1ecf5e5
│           └── chunk-001.nq.gz
├── blob
│   ├── 00ec9dc8a3bb205bce8a1fd62605a1c72ce294da.nq.gz
│   ├── 01602a694c600abb583e6139bd17d7d234af1fd9.nq.gz
│   ├── 302c79b532f61e328519629ba8f94208c37cea33.nq.gz
│   ├── 3aa37e863af7a69f3ca1c3493294d251e728a3e7.nq.gz
│   ├── 459dc5ad1f5f4892f16a4489f080bc70269c87ca.nq.gz
│   ├── 493f7415d73d5d2a0875222a1c7296000935cccc.nq.gz
│   ├── 6deafc261704e20369c0983af88042e502ae4880.nq.gz
│   ├── 798fff074d5c584f9d124c382a09501a58f117bb.nq.gz
│   ├── 7c3652bbbf84c185f7271611b853617b3037286f.nq.gz
│   ├── 7f08759fdf4264cb741a40155bfc4d4d892415a5.nq.gz
│   ├── 8950e594cdbbe714abcf79c4190dbe8a879c498e.nq.gz
│   ├── 897efb249ae8ff1591ead51feaebe0f2c2f055c0.nq.gz
│   ├── a2566a4e0c67476240aa3fe7765c4c2cf1f0c67c.nq.gz
│   ├── a4169acc19fd5e3df12444614f8bb66fa8603430.nq.gz
│   ├── abf2288181636e0d4747170ec7f4a8e5b9abe7c9.nq.gz
│   ├── cb5bf4bbfc89265373df70b4f9df69662be6d5e4.nq.gz
│   ├── cedd6a304502684a16f70e63664136897d39fcc0.nq.gz
│   ├── dc6b9d47748a8afa7b50287b3eeb1f3a236b1434.nq.gz
│   ├── e0c2661976bf79a320f15fa655c70a67762bffea.nq.gz
│   ├── e459bcd8dd4ceda37a814eda0cad4d977cd0624e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f2b2c5744478987ca7d99a9062d4cb7887a3def2.nq.gz
│   └── fdc4fa0a766da228f80705225bfecf276e79d99e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 56ea2e1ef39a174eac61da2edcdb21d1f1ecf5e5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[scrapinghub/scrapy-frontera](https://github.com/scrapinghub/scrapy-frontera)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
