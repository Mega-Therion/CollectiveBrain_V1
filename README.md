# CollectiveBrain_V1

Decentralized multi-agent collective brain system implementing spec-driven development, unified memory layer, and DCBFT consensus protocol.

## 🧠 Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      Orchestrator                            │
│  Decomposes objectives → 3-5 sub-goals → Assigns to workers │
└─────────────────────────────────────────────────────────────┘
                              │
        ┌─────────────────────┼─────────────────────┐
        ▼                     ▼                     ▼
┌───────────────┐     ┌───────────────┐     ┌───────────────┐
│   Worker:     │     │   Worker:     │     │   Worker:     │
│   Research    │     │   Finance     │     │   Analysis    │
└───────────────┘     └───────────────┘     └───────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                   Unified Memory Layer                       │
│  Working │ Session (Redis) │ Semantic (Milvus) │ Relational │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                     DCBFT Consensus                          │
│  N >= 3f + 1  │  Byzantine Fault Tolerant  │  66% Quorum    │
└─────────────────────────────────────────────────────────────┘
```

## 🚀 Quick Start

```bash
# Run orchestration
python main.py orchestrate "Build a vector search capability"

# Run consensus vote
python main.py consensus "Deploy to production"

# Check system status
python main.py status
```

## 📦 Modules

| Module | Description |
|--------|-------------|
| `orchestrator.py` | Decomposes objectives into sub-goals |
| `worker_pool.py` | Specialized worker agents |
| `memory_layer.py` | 4-tier memory (Working, Session, Semantic, Relational) |
| `consensus_engine.py` | DCBFT Byzantine Fault Tolerant voting |

## 🔧 Production Integration Points

- **LLM Decomposition**: Replace stub in `orchestrator.py` with GitHub Models API
- **Redis**: Connect `SessionMemory` for live task state
- **Milvus**: Connect `SemanticMemory` for vector search
- **Neo4j**: Connect `RelationalMemory` for knowledge graphs
