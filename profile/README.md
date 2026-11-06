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

## Planned in stages

1. **Shared presence:** apps report their riders' positions on shared routes and see the
   riders of other apps. Simple to adopt, no accounts. Good for social rides.
2. **Shared physics (later):** apps send power and cadence, and the server calculates speed with
   one common physics model. The same rules for everyone, so fair races, rankings and
   anti-cheat become possible.

Later topics include events and races, optional accounts, and rankings.

## Principles

- **Open:** protocol spec, reference server and client libraries are open source. The server
  is meant to be AGPL-3.0, and the client libraries and spec use permissive licenses, so any
  app can integrate, open source or not.
- **Neutral:** no app owns the network. Everyone can self-host it.
- **Minimal data:** share only what riding together needs, and store nothing that isn't required.
- **Interoperate, don't merge:** we welcome every app the way it is.

## Status

Early design. Nothing is ready to use yet. We are drafting the first version of the
protocol and server and looking for app developers who want to take part.

If you build an indoor cycling app and want your riders to meet others, you're welcome
here. Watch this organisation or get in touch with the maintainers.

---

OpenBikeNet is inspired by [OpenBikeControl](https://openbikecontrol.org), the open protocol
for bike controllers, but is an independent project.
