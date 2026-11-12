# 🦉 Barn Owls Nest

**A nest of ideas for software engineering projects, with an AI twist.**

Here I build small, focused, dependency-light building blocks for backend systems, mostly in Go,
and put them together into larger services. Each library does one thing, is tested on its own,
and can be used without the rest of the nest.

## Principles

- **Small and composable.** Each library is useful by itself, and they combine into services.
- **Few dependencies.** Use the standard library first and add dependencies only when they pay for themselves.
- **Use the infrastructure you already run.** PostgreSQL and the filesystem can carry more than people expect.
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

### 🧰 Go libraries

| Repo | What it is |
|------|------------|
| [go-actorlib](https://github.com/barnowlsnest/go-actorlib) | Actors on top of goroutines and channels |
| [go-asynctasklib](https://github.com/barnowlsnest/go-asynctasklib) | Async tasks with retries, state hooks and worker pools |
| [go-circuitbreakerlib](https://github.com/barnowlsnest/go-circuitbreakerlib) | Circuit breaker for HTTP, gRPC and TCP dependencies |
| [go-connpoollib](https://github.com/barnowlsnest/go-connpoollib) | `net.Conn` connection pool |
| [go-ringbufferlib](https://github.com/barnowlsnest/go-ringbufferlib) | Ring (circular) buffer |
| [go-datalib](https://github.com/barnowlsnest/go-datalib) | General-purpose data structures |
| [go-configlib](https://github.com/barnowlsnest/go-configlib) | Map flags and env vars to struct fields (built on viper) |
| [go-logslib](https://github.com/barnowlsnest/go-logslib) | Minimal logging with few dependencies |

### 🤖 AI-assisted engineering

| Repo | What it is |
|------|------------|
| [cc-skills-golang-fork](https://github.com/barnowlsnest/cc-skills-golang-fork) | Forking the  https://github.com/samber/cc-skills-golang - the agent skills for idiomatic, production-grade Go |
