# Specification — Nine-Body Closed Audit Tensor

## Purpose

The tensor provides a closed fairness/audit structure where no actor with power audits itself and no data pathway validates itself alone.

## Vector

```text
V9 = [HR, P, WORKER, PROJECT, SHADOW, INPUT, OUTPUT, IO_FULCRUM, WATCHER]
```

## Closure Test

```text
if all 9 bodies agree within delta:
    V9 → .
else:
    V9 → unresolved pressure
```

## Body Roles

### HR

Audits worker rights and blocks assignments when rights integrity falls below threshold.

### PROJECT_MANAGER

Coordinates work but cannot certify worker rights.

### WORKER

Receives bounded work and carries labor pressure.

### PROJECT

Preserves project identity, story, scope, and continuity.

### SHADOW_AUDITOR

Audits the pressure fulcrum between power and rights.

### INPUT_AUDITOR

Verifies inbound data integrity.

### OUTPUT_AUDITOR

Verifies outbound data integrity.

### IO_FULCRUM

Checks bidirectional symmetry between input and output.

### WATCHER

Observes the entire system and confirms closure.

## 3002 State Space

The value `3002` is used as the declared audit-state field for this artifact. Closure is represented as one coherent point selected from the state field:

```text
. / 3002
```

## Decision States

```text
ALLOW
DEFER
REPAIR
GROUND
SILENCE
```

## Fairness Principle

The system is “as fair as possible” when:

- the manager cannot self-certify worker rights
- HR cannot self-certify project success
- input cannot self-certify output
- output cannot self-certify input
- the shadow auditor watches pressure, not ideology
- the watcher audits the whole closure
