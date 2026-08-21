---
title: Graph Insights — What the Knowledge Graph Reveals
tags: [vatican-ii, graph, analysis, bth]
created: 2026-07-19
up: "[[000 - Vatican II MOC]]"
source: graphify knowledge graph (86 nodes, 209 edges, 16 communities)
---

# Graph Insights

> [!abstract] What this is
> Findings from running [graphify](graphify-out/graph.html) over the whole vault (86 nodes · 209 edges · 16 communities · 95% EXTRACTED). These are *structural* readings — patterns visible in how the notes connect, not in any single note. Open `graphify-out/graph.html` in a browser, or `graph.canvas` in Obsidian.

## The god nodes = the Council's stress points
Most-connected nodes (by edge count):
1. **Second Vatican Council** — 31
2. **[[Lumen Gentium]]** — 23
3. **[[Gaudium et Spes]]** — 16 · **[[Documents Index]]** — 16
5. **[[Dei Verbum]]** — 13
6. **[[Joseph Ratzinger]]** · **[[Yves Congar]]** — 12
8. **[[John XXIII]]** · **[[Henri de Lubac]]** — 11

> [!tip] Through-line
> Every controversy in the vault routes through the **same two documents — [[Lumen Gentium]] and [[Dignitatis Humanae]]**. The god-node ranking isn't cosmetic: those two texts *are* the Council's pressure points, and each fight below is a different actor pulling on one of them.

---

## Trace 1 — Lumen Gentium bridges both theological wings
`[[Lumen Gentium]]` has betweenness **0.154** (#2 hub); its neighbors span **5 communities**. The bridge is built from **who drafted it** — the roster crosses the future schism:

| Peritus | Edge to LG | Later wing |
|---|---|---|
| [[Gerard Philips]] | `shaped_by` | redactor (neutral) |
| [[Yves Congar]] | shaped | Concilium |
| [[Edward Schillebeeckx]] | shaped | Concilium |
| [[Karl Rahner]] | influenced_by (LG 16) | Concilium |
| [[Joseph Ratzinger]] | shaped | **Communio** |
| [[Henri de Lubac]] | influenced_by | **Communio** |

**Reading:** LG is the one document **both post-conciliar schools co-authored** before they split ([[06 - Reception Controversies & Hermeneutics|Concilium 1964 vs Communio 1972]]). The fight over Vatican II is really a fight over *how to read Lumen Gentium* — **People of God** (Congar/Concilium) vs **communion ecclesiology** (Ratzinger/de Lubac/Communio). Same text, two hermeneutics. The graph shows the seam where the reform coalition later tore.

---

## Trace 2 — The Collegiality → Nota Praevia → Black Week knot
Not a triangle — every path runs **through [[Lumen Gentium]]**:

```
Collegiality ──addresses──▶ Lumen Gentium ──appended_to──▶ Nota Praevia ──included──▶ Black Week
```

1. **Collegiality** (degree 8) is the fault line: `championed` by [[Yves Congar|Congar]], [[Hans Küng|Küng]], [[Edward Schillebeeckx|Schillebeeckx]]; `opposed` by [[Marcel Lefebvre]]. One INFERRED edge: **[[01 - Ecumenical Councils History|Vatican I]]** `centralized_authority_balanced_by` Collegiality — the concept exists to *correct* Vatican I.
2. It lives **inside [[Lumen Gentium]]** (also [[Christus Dominus]]) — doctrine being written into the dogmatic constitution.
3. The **Nota Explicativa Praevia** (degree 2) exists *only* to attach to LG — the brake clamping collegiality to "consent of its head," protecting papal primacy.
4. **[[03 - Preparatory Phase Schemata & Sessions|Black Week]]** is the delivery window — and it bundles **two brakes at once**: the Nota on LG **and** the postponed [[Dignitatis Humanae]] vote.

**Reading:** collegiality couldn't be stopped, so it was **annotated**. The Nota didn't delete the doctrine — it fenced it. That fence is what Lefebvre still rejected, and why LG reads two ways depending on whether you count the body or the note.

---

## Trace 3 — The Lefebvre / SSPX rejection cluster
Community 6 ("Religious Liberty & the SSPX Schism," 7 nodes) puts the doctrine's **architect and its enemy in the same room** — because a community forms around a shared *topic*, not a shared opinion:

| Node | Role |
|---|---|
| [[Dignitatis Humanae]] / Religious Liberty | the contested doctrine |
| [[John Courtney Murray]] | `drafted` it — architect |
| Francis Spellman | brought Murray — patron |
| [[Marcel Lefebvre]] | `rejected` it — enemy |
| Coetus Internationalis Patrum | Lefebvre `led` it — his bloc |
| SSPX | Lefebvre `founded` it — his vehicle |

**Lefebvre's edges = his objection list:** `rejected`→[[Dignitatis Humanae]], `opposed`→Religious Liberty, `opposed`→Collegiality. **Exactly the two Black Week targets.** His grievances land on the two most-contested votes.

**Two structural ironies the graph exposes:**
- `Lefebvre --appointed_by--> [[John XXIII]]` — a **preparatory-commission insider**, placed by the pope who launched the reform, who then rejected its two sharpest doctrines. Insider → schismatic in 7 edges.
- **SSPX (degree 1) and Coetus (degree 1) connect to nothing but Lefebvre.** A schism *is* a spur — a structure detached from the main body, attached only to its founder. Compare [[Lumen Gentium]]'s 23 edges across 5 communities: **rejection is a spur; reception is a web.**

---

## Bonus — hyperedges the graph found on its own
Group relationships it detected without being told:
- **The Four Constitutions** · **The Nine Decrees**
- **Black Week interventions** (Nota + LG + DH + UR + Paul VI)
- **Mixed commission on [[Dei Verbum]]** (Ottaviani + Bea + John XXIII)
- **Concilium founders** (Rahner, Küng, Schillebeeckx, Congar, Chenu)
- **Communio founders** (de Lubac, Ratzinger, von Balthasar, Daniélou)
- **Periti who shaped [[Lumen Gentium]]** (Philips, Rahner, Congar, de Lubac, Ratzinger, Schillebeeckx)

## Honest caveat
At ~16.6k words the corpus fits one context window — the graph's value here is **navigation and structural surprise**, not token savings. 24 nodes are weakly connected (isolated early councils, single observers) — expected for a hub-and-spoke topic.

## Links
[[000 - Vatican II MOC]] · [[06 - Reception Controversies & Hermeneutics]] · graph files in `graphify-out/`
