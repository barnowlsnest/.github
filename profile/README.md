# 🦉 Barn Owls Nest

**A nest of ideas for software engineering projects, with an AI twist.**

Here I build small, focused, dependency-light building blocks for backend systems, mostly in Go,
and put them together into larger services. Each library does one thing, is tested on its own,
and can be used without the rest of the nest.

## Principles

- **Small and composable.** Each library is useful by itself, and they combine into services.
- **Few dependencies.** Use the standard library first and add dependencies only when they pay for themselves.
- **Human-designed, AI-assisted.** I make the design, the architecture and the core decisions myself. AI agents help me find bugs, review and refactor code, and write some of the implementation, so I get clean results faster.

## Projects

### 🌩️ Stratus: streaming on a write-ahead log

An append-only record stream served over gRPC and stored in a write-ahead log, with dedup keys,
monotonic IDs and live tailing.

| Repo | What it is |
|------|------------|
| [stratus](https://github.com/barnowlsnest/stratus) | gRPC server and CLI for the stream |
| [stratus-ui](https://github.com/barnowlsnest/stratus-ui) | Web console for Stratus servers |
| [ts-stratus](https://github.com/barnowlsnest/ts-stratus) | TypeScript client |
| [go-wallib](https://github.com/barnowlsnest/go-wallib) | The write-ahead log underneath |

### 🐘 PGQS: backends built on PostgreSQL

A toolkit for building services where PostgreSQL is the only infrastructure you need: one
database for state, events and coordination.

| Repo | What it is |
|------|------------|
| [pgqs-harness](https://github.com/barnowlsnest/pgqs-harness) | Shared foundation: pools, `LISTEN/NOTIFY`, migrations, generic DAO |
| [pgqs-tenants](https://github.com/barnowlsnest/pgqs-tenants) | Multi-tenancy with one schema per tenant and lifecycle events |
| [pgqs-leaderelection](https://github.com/barnowlsnest/pgqs-leaderelection) | Leader election backed by PostgreSQL |

### 🤖 AI-assisted engineering

| Repo | What it is |
|------|------------|
| [cc-skills-golang-fork](https://github.com/barnowlsnest/cc-skills-golang-fork) | Forking the  https://github.com/samber/cc-skills-golang - the agent skills for idiomatic, production-grade Go |
