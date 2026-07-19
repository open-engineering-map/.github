# Open Engineering Map

<p align="center">
  <img src="../assets/hero-banner.png" alt="Open Engineering Map">
</p>

The **Open Engineering Map** organization maintains the tooling that discovers, validates, combines, and visualizes metadata published throughout the Open Engineering ecosystem.

Rather than being another source of truth, the Map provides a **derived view** of the ecosystem. It continuously builds a navigable graph from distributed repository metadata while preserving provenance and reporting diagnostics whenever inconsistencies are encountered.

---

## Purpose

Open Engineering is intentionally decentralized.

Each repository owns its own metadata and publishes it alongside its implementation. Open Engineering Map connects these independent sources into a coherent landscape without taking ownership away from the repositories themselves.

Its responsibilities include:

- discovering Open Engineering repositories
- collecting published `metadata.yaml` files
- validating metadata against Open Engineering conventions
- resolving relationships across repositories
- constructing a graph of the ecosystem
- generating multiple visualization and interchange formats

The generated outputs make it easier for humans and software agents to understand how the Open Engineering ecosystem is connected.

---

# Position within Open Engineering

```text
                    Open Engineering Conventions
                               │
                               │ defines schemas
                               ▼
                    Open Engineering Ecosystem
                               │
                               │ generates repository metadata
                               ▼
         open-engineering-*/source/metadata.yaml
                               │
                               │ distributed metadata
                               ▼
                      Open Engineering Map
                               │
        ┌──────────────────────┼──────────────────────┐
        │                      │                      │
        ▼                      ▼                      ▼
     Validation           Relationship Graph      Diagnostics
        │                      │                      │
        └───────────────┬──────┴───────────────┬──────┘
                        ▼                      ▼
                  Generated Maps       Machine-readable outputs
```

---

# Responsibilities

This organization is responsible for:

- repository discovery
- metadata aggregation
- metadata validation
- relationship resolution
- graph construction
- provenance tracking
- diagnostics generation
- ecosystem visualization
- graph export
- Markdown generation
- Mermaid generation
- GraphML generation
- JSON-LD generation

It deliberately does **not** define metadata schemas or modify authoritative metadata.

---

# Authority Boundaries

| Concern | Authority |
|----------|-----------|
| Metadata schema | Open Engineering Conventions |
| Engineering identifiers | Open Engineering Registries |
| Repository metadata generation | Open Engineering Ecosystem |
| Repository implementation | Owning GitHub organization |
| Ecosystem graph and projections | **Open Engineering Map** |

When source metadata conflicts, the Map records diagnostics instead of silently changing data.

---

# Generated Outputs

The map generator can produce projections such as:

- JSON
- JSON-LD
- GraphML
- Mermaid diagrams
- Markdown documentation
- diagnostics reports
- reproducible source lock files

These outputs are deterministic: identical source metadata always produces identical results.

---

# Design Principles

Open Engineering Map is built around several principles:

- **Source metadata is authoritative**
- **Preserve provenance**
- **Never silently rewrite metadata**
- **Deterministic generation**
- **Composable outputs**
- **Traceable diagnostics**
- **Standards-based graph formats**
- **Automation-first**
- **Open by design**

---

# Relationship with Other Organizations

| Organization | Responsibility |
|--------------|----------------|
| Open Engineering Conventions | Metadata schemas and relationship vocabulary |
| Open Engineering Ecosystem | Generation of repository metadata |
| Open Engineering Registries | Canonical engineering identifiers |
| Open Engineering Map | Discovery, validation, graph construction, visualization |

Together these organizations separate **authoring**, **validation**, **registration**, and **visualization** into independent responsibilities.

---

# Example Pipeline

```text
GitHub Organizations
        │
        ▼
Repository Discovery
        │
        ▼
metadata.yaml
        │
        ▼
Validation
        │
        ▼
Relationship Resolution
        │
        ▼
Graph Construction
        │
        ▼
Generated Outputs
```

---

# Repository

The primary implementation repository is:

> https://github.com/open-engineering-map/source

It contains the complete pipeline responsible for:

- discovering repositories
- validating metadata
- building the ecosystem graph
- generating documentation
- exporting graph formats
- producing diagnostics

---

# Vision

Open Engineering Map enables both humans and AI agents to explore the Open Engineering landscape as a connected graph rather than as isolated repositories.

As the ecosystem grows, the Map provides a continuously generated, traceable, reproducible, and navigable view of the relationships that emerge across Open Engineering while leaving ownership of the underlying metadata exactly where it belongs: with the source repositories.
