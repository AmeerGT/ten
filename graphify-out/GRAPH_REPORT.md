# Graph Report - /root/.claude  (2026-04-18)

## Corpus Check
- Corpus is ~7,543 words - fits in a single context window. You may not need a graph.

## Summary
- 52 nodes · 55 edges · 8 communities detected
- Extraction: 85% EXTRACTED · 15% INFERRED · 0% AMBIGUOUS · INFERRED: 8 edges (avg confidence: 0.73)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Extraction & Ingestion Pipeline|Extraction & Ingestion Pipeline]]
- [[_COMMUNITY_Session Start Hook|Session Start Hook]]
- [[_COMMUNITY_Graph Detection & Output Formats|Graph Detection & Output Formats]]
- [[_COMMUNITY_Graph Analysis & Clustering|Graph Analysis & Clustering]]
- [[_COMMUNITY_Export & Query Modes|Export & Query Modes]]
- [[_COMMUNITY_Claude MD Integration|Claude MD Integration]]
- [[_COMMUNITY_Quality & Audit Rules|Quality & Audit Rules]]
- [[_COMMUNITY_Wiki Export|Wiki Export]]

## God Nodes (most connected - your core abstractions)
1. `Graphify Pipeline` - 10 edges
2. `AST Structural Extraction (Step 3A)` - 6 edges
3. `Graph Build and Cluster (Step 4)` - 6 edges
4. `graph.json Persistent Store` - 6 edges
5. `Semantic Extraction via Subagents (Step 3B)` - 5 edges
6. `Session Start Hook Skill` - 5 edges
7. `Graphify Skill` - 4 edges
8. `Incremental Update Mode (--update)` - 4 edges
9. `Session Start Hook Workflow` - 4 edges
10. `Extraction Cache` - 3 edges

## Surprising Connections (you probably didn't know these)
- `Session Start Hook Skill` --semantically_similar_to--> `Graphify Skill`  [INFERRED] [semantically similar]
  .claude/skills/session-start-hook/SKILL.md → .claude/skills/graphify/SKILL.md
- `Graphify Skill Registration` --references--> `Graphify Skill`  [EXTRACTED]
  .claude/CLAUDE.md → .claude/skills/graphify/SKILL.md
- `CLAUDE.md Native Integration` --references--> `Graphify Skill Registration`  [EXTRACTED]
  .claude/skills/graphify/SKILL.md → .claude/CLAUDE.md

## Hyperedges (group relationships)
- **Graphify Output Format Options** — skill_md_graphify_html_output, skill_md_graphify_obsidian_output, skill_md_graphify_neo4j_export, skill_md_graphify_svg_export, skill_md_graphify_graphml_export, skill_md_graphify_wiki_output, skill_md_graphify_mcp_server [EXTRACTED 0.95]
- **Graphify Three-Stage Extraction Pipeline** — skill_md_graphify_ast_extraction, skill_md_graphify_semantic_extraction, skill_md_graphify_merge [EXTRACTED 0.95]
- **Session Hook Setup and Validation Workflow** — session_start_hook_dependency_install, session_start_hook_settings_json, session_start_hook_validate [EXTRACTED 0.92]

## Communities

### Community 0 - "Extraction & Ingestion Pipeline"
Cohesion: 0.23
Nodes (12): Add URL Mode (/graphify add), AST Structural Extraction (Step 3A), Extraction Cache, Git Commit Hook Integration, AST + Semantic Merge (Step 3C), Rationale: Extraction Cache for Incremental Runs, Rationale: Parallel AST + Semantic Extraction, Raw Folder Workflow (Karpathy) (+4 more)

### Community 1 - "Session Start Hook"
Cohesion: 0.18
Nodes (11): Async Hook Mode, CLAUDE_CODE_REMOTE Environment Flag, Dependency Installation Script, Hook Environment Variables, SessionStart Hook Event, Hook Registration in .claude/settings.json, Session Start Hook Skill, Hook Validation (Linter + Test) (+3 more)

### Community 2 - "Graph Detection & Output Formats"
Cohesion: 0.25
Nodes (8): Community Labeling (Step 5), Graphify File Detection (Step 2), HTML Visualization Output (Step 6), Manifest Save and Cleanup (Step 9), Obsidian Vault Output, Graphify Pipeline, SVG Export (Step 7b), Video/Audio Transcription (Step 2.5)

### Community 3 - "Graph Analysis & Clustering"
Cohesion: 0.29
Nodes (7): Graph Build and Cluster (Step 4), Cluster-Only Mode (--cluster-only), Community Detection, God Nodes Analysis, GRAPH_REPORT.md Audit Report, Surprising Connections Analysis, Token Reduction Benchmark (Step 8)

### Community 4 - "Export & Query Modes"
Cohesion: 0.29
Nodes (7): Explain Mode (/graphify explain), graph.json Persistent Store, GraphML Export (Step 7c), MCP Server (Step 7d), Neo4j Export (Step 7), Path Mode (/graphify path), Query Mode (/graphify query)

### Community 5 - "Claude MD Integration"
Cohesion: 0.5
Nodes (4): Graphify Skill Registration, CLAUDE.md Native Integration, Graphify Skill, Graphify Trigger /graphify

### Community 6 - "Quality & Audit Rules"
Cohesion: 1.0
Nodes (2): Edge Confidence Tags (EXTRACTED/INFERRED/AMBIGUOUS), Honesty Rules (No Invented Edges)

### Community 7 - "Wiki Export"
Cohesion: 1.0
Nodes (1): Wiki Output (Step 6b)

## Knowledge Gaps
- **30 isolated node(s):** `Graphify Trigger /graphify`, `Graphify File Detection (Step 2)`, `Community Labeling (Step 5)`, `Obsidian Vault Output`, `Wiki Output (Step 6b)` (+25 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `Quality & Audit Rules`** (2 nodes): `Edge Confidence Tags (EXTRACTED/INFERRED/AMBIGUOUS)`, `Honesty Rules (No Invented Edges)`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Wiki Export`** (1 nodes): `Wiki Output (Step 6b)`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Graphify Pipeline` connect `Graph Detection & Output Formats` to `Extraction & Ingestion Pipeline`, `Graph Analysis & Clustering`, `Claude MD Integration`?**
  _High betweenness centrality (0.678) - this node is a cross-community bridge._
- **Why does `Graphify Skill` connect `Claude MD Integration` to `Session Start Hook`, `Graph Detection & Output Formats`?**
  _High betweenness centrality (0.401) - this node is a cross-community bridge._
- **Why does `Graph Build and Cluster (Step 4)` connect `Graph Analysis & Clustering` to `Graph Detection & Output Formats`, `Export & Query Modes`?**
  _High betweenness centrality (0.400) - this node is a cross-community bridge._
- **What connects `Graphify Trigger /graphify`, `Graphify File Detection (Step 2)`, `Community Labeling (Step 5)` to the rest of the system?**
  _30 weakly-connected nodes found - possible documentation gaps or missing edges._