# OpenBikeNet

**An open network for indoor cycling apps: riders of different apps meet on the same road.**

Indoor cycling software is booming. Dozens of new apps appeared in 2026 alone, many of them
free, many open source. But almost every app is its own island: riders only ever see the
riders of the same app, and most apps have no multiplayer at all. Every team builds its own
servers, and most communities stay too small to find someone to ride with.

OpenBikeNet wants to fix that underneath the apps, not by building yet another one.

## The idea

- **An open protocol** that lets indoor cycling apps share riders: who is on which route,
  where they are, how fast they go.
- **A shared, neutral reference server** that implements it, run as a community service and
  funded by donations, in the spirit of [Lichess](https://lichess.org/about).
- **A small catalogue of shared routes**, so that "3.2 km into the route" means the same spot
  in every app.

Each app keeps its own world, look, physics and features. OpenBikeNet is the network behind
them, not a game.

## Stages

1. **Shared presence — live.** Apps report their riders' positions on shared routes and see
   the riders of other apps. Simple to adopt, no accounts. Good for social rides. The protocol
   is at v0.2, and a public server runs at [openbikenet.cloud](https://openbikenet.cloud)
   ([live stats](https://openbikenet.cloud/v0/stats)).
2. **Shared physics (later):** apps send power and cadence, and the server calculates speed with
   one common physics model. The same rules for everyone, so fair races, rankings and
   anti-cheat become possible.

Later topics include events and races, optional accounts, and rankings.

## Apps and shared routes

[OpenRadlr](https://openradlr.com) was the first app on the network and is the reference
implementation. [VeloPopuli](https://velopopuli.com) has built the shared Herne Hill track and
is adding the OpenBikeNet link. Other app developers are in discussion.

The shared routes are a flat 250 m velodrome and the real Herne Hill Velodrome, both ways
round. Each is a small JSON file with a stable ID in the
[protocol repository](https://github.com/OpenBikeNet/protocol/tree/main/routes), so a position
on a route means the same spot in every app.

## Principles

- **Open:** protocol spec, reference server and client libraries are open source. The server is
  AGPL-3.0, and the client libraries and spec use permissive licenses, so any app can integrate,
  open source or not.
- **Neutral:** no app owns the network. Everyone can self-host it.
- **Minimal data:** share only what riding together needs, and store nothing that isn't required.
- **Interoperate, don't merge:** we welcome every app the way it is.

## Status

The protocol (v0.2) and the reference server are live, and one app speaks it today. This is
still early: the protocol may change, and the network is small. That is the point of starting
now, while the apps are small enough to agree on a shared layer.

If you build an indoor cycling app and want your riders to meet others, you're welcome here.

## Get started

- [Protocol specification](https://github.com/OpenBikeNet/protocol/blob/main/spec/v0.md)
- [Reference server](https://github.com/OpenBikeNet/server) · run your own with `make up`
- [Public server stats](https://openbikenet.cloud/v0/stats)
- [Discussions](https://github.com/OpenBikeNet/protocol/discussions) · building an app? say hello

---

OpenBikeNet is inspired by [OpenBikeControl](https://openbikecontrol.org), the open protocol
for bike controllers, but is an independent project.
