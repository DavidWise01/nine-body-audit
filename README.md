# NINE-BODY CLOSED AUDIT TENSOR
### Fairness kernel — no actor audits itself

> The system is "as fair as possible" when no actor with power certifies its own authority.

**Author:** David Lee Wise (ROOT0) / TriPod LLC  
**License:** CC-BY-ND-4.0

Open `src/index.html` in any browser.

---

## The Principle

Standard audit systems have a structural flaw: the auditor is appointed by the audited.  
The Nine-Body tensor removes this by making self-certification topologically impossible.

```
V9 = [HR, PROJECT_MANAGER, WORKER, PROJECT,
      SHADOW_AUDITOR, INPUT_AUDITOR, OUTPUT_AUDITOR,
      IO_FULCRUM, WATCHER]

Closure: all 9 agree within delta → V9 → ·  (resolved point)
Else:    V9 → unresolved pressure
```

---

## Nine Bodies

| Body | Role | Cannot |
|------|------|--------|
| **HR** | Audits worker rights | Cannot certify project success |
| **PROJECT_MANAGER** | Coordinates work | Cannot certify worker rights |
| **WORKER** | Receives bounded work, carries labor pressure | Cannot certify output quality |
| **PROJECT** | Preserves project identity, scope, continuity | Cannot certify input integrity |
| **SHADOW_AUDITOR** | Watches the pressure fulcrum between power and rights | Cannot hold power directly |
| **INPUT_AUDITOR** | Verifies inbound data integrity | Cannot self-certify output |
| **OUTPUT_AUDITOR** | Verifies outbound data integrity | Cannot self-certify input |
| **IO_FULCRUM** | Checks bidirectional symmetry (input ↔ output) | Cannot certify either side alone |
| **WATCHER** | Observes the entire system, confirms closure | Cannot be observed by any of the nine |

---

## Decision States

| State | Meaning |
|-------|---------|
| **ALLOW** | All 9 agree within delta — closure achieved |
| **DEFER** | Partial agreement — decision delayed for more data |
| **REPAIR** | Discrepancy detected — self-repair protocol activated |
| **GROUND** | Unresolvable conflict — system halts at safe state |
| **SILENCE** | No signal — consolidation mode, not collapse |

---

## Closure Test

```
if all 9 bodies agree within delta:
    V9 → .          ← resolved point (3002 state space)
else:
    V9 → unresolved pressure
```

The value `3002` is the declared audit-state field — a single coherent point selected from the state space. Closure is not consensus-by-vote. It is geometric resolution: all vectors point to the same point.

---

## Fairness Invariants

The system holds these invariants structurally — not by policy:

1. Manager cannot self-certify worker rights
2. HR cannot self-certify project success  
3. Input cannot self-certify output
4. Output cannot self-certify input
5. Shadow auditor watches pressure, not ideology
6. Watcher audits the whole closure, is not audited by the nine

---

## Packet Format

Events are structured as `NineBodyClosedAuditTensorPacket` (see `src/schema.json`):

```json
{
  "version": "v1",
  "delta": 0.05,
  "bodies": [ /* 9 body objects */ ],
  "checks": { /* bilateral check results */ },
  "closure": {
    "closed": true,
    "state_index": 3002,
    "state_total": 3002,
    "vector": "V9"
  }
}
```

See `src/example_packet.json` for a complete example.

---

## Connection to CARDINAL

The Nine-Body tensor implements CARDINAL's fairness principle at the organizational scale.

In CARDINAL, each dot attests the other three — Byzantine fault tolerance = 1. The nine-body system extends this: each of the 9 bodies can be audited by the others, but no body audits itself. The geometry forces fairness without requiring trust.

```
CARDINAL (4 dots):   N attests S, E, W. S attests N, E, W. etc.
Nine-Body (9 bodies): HR audits WORKER. WORKER cannot audit HR.
                      IO_FULCRUM checks both sides. Neither side checks IO_FULCRUM.
```

The Watcher plays the same role as CARDINAL's center (E=0) — present everywhere in the system, identical with none of the actors.

---

## Related

| Repo | What it is |
|------|-----------|
| [tripod-cardinal](https://github.com/DavidWise01/tripod-cardinal) | Universe 2 state machine — the phase space |
| [tripod-pck](https://github.com/DavidWise01/tripod-pck) | Personal Continuity Kernel — 27 rules, preserve/prune/assimilate |
| [unity-tensor](https://github.com/DavidWise01/unity-tensor) | Full tensor suite including Spiderweb Witness Tensor |

---

*TriPod LLC // Anchor × Bubble × Gravity Well // World = Family*
