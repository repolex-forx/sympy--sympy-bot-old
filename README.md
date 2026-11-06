# Repolex Knowledge Graph of sympy/sympy-bot-old

RDF knowledge graph data for [sympy/sympy-bot-old](https://github.com/sympy/sympy-bot-old), parsed by [repolex](https://repolex.ai).

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
rlex download sympy/sympy-bot-old
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7abf6b169052484707c7cbcf4086453808f79793
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7abf6b169052484707c7cbcf4086453808f79793
│           └── chunk-001.nq.gz
├── blob
│   ├── 015fc502e0a786ae78915fb4c151384518dbdaaf.nq.gz
│   ├── 02c147a5bcbd3f990b294f2bd6bb0a3b871dea31.nq.gz
│   ├── 06626f0bc8e22631354af3e0163778d737c1747d.nq.gz
│   ├── 07d1db921dca5d4c2831134938fac36effbbc3c9.nq.gz
│   ├── 09929cef2e9d7cb48ac96da96a0f3bae39291e11.nq.gz
│   ├── 1f872429dda4e0931e1b680e8d3f2aeca63ff354.nq.gz
│   ├── 214d96a3d8c636338223453dcc3272a3e8e2cd6f.nq.gz
│   ├── 38901312fdfafd82301e654a3ef8eabcf2214c38.nq.gz
│   ├── 39da4befa08b9aeb541dfee839bae42332dd53bb.nq.gz
│   ├── 3a703654876e69aa2cb5a8fa875795eaec9d28e9.nq.gz
│   ├── 3f082228b8fb6848bd63ded8499ed24792ce0b3c.nq.gz
│   ├── 605918462b351dacb3f9f100b423f828fc88bd4f.nq.gz
│   ├── 6a5d2467008356b9bb2687fbe698f54079b3adc1.nq.gz
│   ├── 76735f798631667e244096f27243e5ac7c6d17ed.nq.gz
│   ├── 82c00fff64dc92ba8376e0c729379ae22e3fcff1.nq.gz
│   ├── 846f10927e970d9a7c98b36aeb4e18313861fcb6.nq.gz
│   ├── 881d0f138d2cd6d707f0e8ff09792e3340697689.nq.gz
│   ├── 955b0eb57b83e1700858f0b94f6141fb17f9fd40.nq.gz
│   ├── 97373d9b6db320a1b93c3337294a54f4d634c9b1.nq.gz
│   ├── 9d6999b8f230f365c1a372376207fcc5348fa1d2.nq.gz
│   ├── b5f22c6a76c8faa60b3713cd7f0a53eba837708d.nq.gz
│   ├── b975f72424b3e9c7bd19dddd0817322e67b083d8.nq.gz
│   ├── bf46ea51fe37e1938136045ff280b901aa3cf8a4.nq.gz
│   ├── c1865c3b9869f6dafbf1f9b3e9a03fc3a71b3163.nq.gz
│   ├── c504efeea4960323048256a3d3aa91679bc92122.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ee2099550201d371e31859820e786ef208a32424.nq.gz
│   ├── f2180b999557ff743e19e621ff3c82300f429c08.nq.gz
│   └── fd0fc2d26a4e9afc94f3ebbe46b061255e39af78.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7abf6b169052484707c7cbcf4086453808f79793.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[sympy/sympy-bot-old](https://github.com/sympy/sympy-bot-old)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
