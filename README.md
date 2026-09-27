# Repolex Knowledge Graph of asimov-modules/asimov-modules.rb

RDF knowledge graph data for [asimov-modules/asimov-modules.rb](https://github.com/asimov-modules/asimov-modules.rb), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-modules.rb
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3763173d377fd10b01ef577d33afc878d650a475
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3763173d377fd10b01ef577d33afc878d650a475.nq.gz
│   └── repolex
│       └── 3763173d377fd10b01ef577d33afc878d650a475
│           └── chunk-001.nq.gz
├── blob
│   ├── 0074ac243e97f58407fc5578ba1618c45bf1d23e.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 3eca1aa492ea3e5b7d2e9404023535461dbaddf2.nq.gz
│   ├── 53683c76d06540eafca0436baf95f3981081e9f4.nq.gz
│   ├── 6f83656972dcf4cdabab996bd49dde3986bc10be.nq.gz
│   ├── 6f927781261f7af2a0aedc1b13e5c9d8fd639f3c.nq.gz
│   ├── b4e2a20bb6069d33479542fc863e7e36810e0f01.nq.gz
│   ├── b7f3a74ca7603fb0a6e32c31de0a52de3ac5befd.nq.gz
│   ├── bb67c988519445888ae76a7c7c4041de9dee75cf.nq.gz
│   ├── cc6f535b40f4ebf04221043237ff3deaf67f9549.nq.gz
│   ├── cd138f62a7d2e53edef94443810d0162e2c9f095.nq.gz
│   ├── d1128acc23464e163f326bfa662c52698a677005.nq.gz
│   ├── ddc62c374dc932cc14568686e267e2814a4c925d.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 3763173d377fd10b01ef577d33afc878d650a475.nq.gz
├── filetree
│   └── 3763173d377fd10b01ef577d33afc878d650a475.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[asimov-modules/asimov-modules.rb](https://github.com/asimov-modules/asimov-modules.rb)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
