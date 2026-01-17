# Ant Protocol (v0.1)

This document defines how individual AI agents ("Ants")
communicate with the Ant Farm Core.

The goal of the protocol is:
- clarity
- replaceability
- transparency
- trust

No Ant is special.
Any Ant can be replaced as long as it respects this protocol.

---

## Core Principles

1. Ants are stateless
2. Ants receive structured input
3. Ants return structured output
4. Ants must explain their reasoning
5. Ants must report confidence

---

## Standard Ant Input Schema

Every Ant receives input in this shape:

```json
{
  "ant_id": "string",
  "task": "string",
  "context": {
    "source": "string",
    "url": "string",
    "raw_data": {}
  },
  "constraints": {
    "time_limit_ms": number,
    "risk_tolerance": "low | medium | high"
  }
}
