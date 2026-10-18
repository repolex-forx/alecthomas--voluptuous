# Repolex Knowledge Graph of alecthomas/voluptuous

RDF knowledge graph data for [alecthomas/voluptuous](https://github.com/alecthomas/voluptuous), parsed by [repolex](https://repolex.ai).

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
rlex download alecthomas/voluptuous
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 44593ce7c330faf9418252c4b5448f4736144a7f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 44593ce7c330faf9418252c4b5448f4736144a7f
│           └── chunk-001.nq.gz
├── blob
│   ├── 0289f6d3f308606de4e3033d7c015387f291799a.nq.gz
│   ├── 060854867dd06efe2cb539351cfd391a359ef280.nq.gz
│   ├── 08653ed8ef59f36f962ff3be65726e4879af1873.nq.gz
│   ├── 0bf93022871bb1edc6630e9e9db60b291fc16494.nq.gz
│   ├── 2fd32941985e91d74246e2f29e88d00c5c5ecf0c.nq.gz
│   ├── 331b5d84309f3be7ca7bae6ac675d6595b9118eb.nq.gz
│   ├── 3673e86704d502daf2f72b561864fc701e378e4f.nq.gz
│   ├── 369f548d63c1daa66b14ca3d153f53295679f248.nq.gz
│   ├── 383f4511d444516caed0fd113ee8a2b640cd2290.nq.gz
│   ├── 5ba97ab64b542fca8e9f3125867e3241c50a69a2.nq.gz
│   ├── 71b89199217b44069300d39bcc56be68468a7afd.nq.gz
│   ├── 78739db043867e5964bd0f2b15850d9f891a6e8c.nq.gz
│   ├── 7fef769248e85eab6c828b9f2f7b802296cddadc.nq.gz
│   ├── 897864b852f50776a7de7bdc9523ef3e201413a4.nq.gz
│   ├── 966ab6f4da7fe647b41b1bae383446ca174b76fd.nq.gz
│   ├── a19b7057faab4ddf95569fcc3bae9f76d496c3de.nq.gz
│   ├── a69bb8a00fd9ab7182e28cbbb003e401e4257fd7.nq.gz
│   ├── a889e41a50b62ab48ca70dfb221b1342063a7497.nq.gz
│   ├── aad10a6558260f4f5643e8901cde9328ee7ae9d0.nq.gz
│   ├── acb505dc15777c4c0aa8e8dc162d5e3813419140.nq.gz
│   ├── b3e10453af5fb040f88c58b3a56006d645ba2471.nq.gz
│   ├── cfd671712462535f85605b77bbec1e7e261528cf.nq.gz
│   ├── d978679938e59b975e04403db85e221b6a8bbb25.nq.gz
│   ├── e359f119862c67362124e704c88be16c12688190.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e889550ba4cbc92a720527042e5f6e7a303bfcbc.nq.gz
│   ├── e9795d0e7a8499b76c87c3b5938b74c39150ed53.nq.gz
│   ├── eabfd027871d99bb57859f54b43e960e15c2d9aa.nq.gz
│   ├── f29719c7262f82e27b954d843c279c80afe65646.nq.gz
│   ├── fdedb5e3ca089f357d8b367b22f21ffbb3c7db87.nq.gz
│   └── fe28214d3352b0ed40820a4999317694c8b1ef57.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 44593ce7c330faf9418252c4b5448f4736144a7f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[alecthomas/voluptuous](https://github.com/alecthomas/voluptuous)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
