# Eventmodelers Build Kits

Build kits that connect [Eventmodelers](https://eventmodelers.ai) event-modeling boards to autonomous
coding agents. Each kit installs a real-time agent and a set of skills that pick up slice status
changes on a board, implement the slice in a target stack, and report the work back — turning an
event model into working code.

This is the [Cratis](https://www.cratis.io) fork of
[Nebulit-GmbH/Eventmodelers-Build-Kits](https://github.com/Nebulit-GmbH/Eventmodelers-Build-Kits),
adding a build kit for the Cratis stack alongside the upstream kits.

## Kits in this repository

| Kit | Target stack |
| --- | --- |
| [`build-kit-cratis-csharp`](./build-kit-cratis-csharp/) | Cratis Arc + Chronicle vertical slices in .NET / C# (added in this fork) |
| [`build-kit-axon`](./build-kit-axon/) | Axon Framework (upstream) |
| [`build-kit-node`](./build-kit-node/) | Node.js (upstream) |
| [`build-kit-supabase`](./build-kit-supabase/) | Supabase (upstream) |
| [`modeling-kit`](./modeling-kit/) | Agent-assisted event modeling on the board itself (upstream) |

The Cratis kit turns board slices into event-sourced, CQRS vertical slices — commands, events, read
models, projections, and reactors implemented the Cratis way and verified with `dotnet build` and
`dotnet test`. See [its README](./build-kit-cratis-csharp/README.md) for setup and usage.

## The Cratis ecosystem

The Cratis kit builds on:

- [Chronicle](https://github.com/Cratis/Chronicle) — an event-sourcing database and processing runtime with a first-class .NET SDK and additional TypeScript, Kotlin/Java (JVM), and Elixir clients — with a Python client coming soon — plus pluggable storage-provider implementations including MongoDB (default), PostgreSQL, SQL Server, and SQLite.
- [Arc](https://github.com/Cratis/Arc) — an opinionated CQRS application framework for ASP.NET Core; works with or without event sourcing.
- [Components](https://github.com/Cratis/Components) — React components aligned with Arc patterns.

Everything Cratis publishes today is MIT licensed and free to use.

## License

All kits are MIT licensed — see the license files in the individual kit directories.
