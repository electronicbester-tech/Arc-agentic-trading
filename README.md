# Arc Agentic Trading

A practical demo of agent‑based commerce on Arc using USDC as native gas and value, Circle infrastructure for wallets and Gateway, and Gemini for reasoning and planning. This README provides a complete overview but intentionally uses abstract naming and slightly altered sequencing to prevent direct replication by competitors.

---

## Mission and Principles

- **Mission:** Demonstrate how an autonomous agent can coordinate, pay, and settle on Arc with deterministic finality.  
- **Principles:**  
  - Determinism and auditability.  
  - Safety through separation of off‑chain reasoning and on‑chain execution.  
  - Limited disclosure: navigation details are intentionally abstracted.  
  - Extensibility for arbitrage, market‑making, or developer tools.

---

## High‑Level Architecture

```mermaid
flowchart LR
    subgraph OffChain[Off‑chain agent]
        P[AI Planner]
        O[Orchestrator]
        W[Programmable Wallets & Data Gateway]
        X[x402 Micropay Endpoint]
        P --> O
        O --> W
        O --> X
        O --> R[Chain Endpoint]
    end

    subgraph OnChain[Arc L1]
        S[Settlement Core]
        T[(Native Token)]
        V[Venue]
        S --- T
        S --> V
    end

    R --> S
