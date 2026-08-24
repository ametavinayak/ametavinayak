<div align="center">

# Vinayak Ameta

**Systems that have to keep being right.**

Production astrology computation · chess engines · applied ML · first-principles simulation

[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:vinayak3971@gmail.com)

</div>

---

## About

I build things that run unattended and have to be correct — a computation engine serving a live business, a chess engine where every change passes a statistical significance gate, a physics simulator that returned a negative result I published rather than buried.

My working rule: **a claim isn't real until it's been measured against an independent oracle.** Most of what follows is here because it survived that.

---

## Selected work

### Vedic astrology computation engine
A production ephemeris and chart-calculation engine serving a live astrology business — 64 REST endpoints covering OTP auth, wallets, payments, consultation sessions and real-time call tokens. Multi-language chart rendering (English / Hindi / Bengali) as vector output.

The interesting part was a licensing problem, not an astrology one: the industry-standard ephemeris ships under AGPL, which makes commercial distribution impossible. I replaced it with an open alternative and then had to *prove* the replacement was numerically equivalent — **17,893 oracle checks** across planetary positions, house systems, divisional charts and dasha timelines before I'd trust it.

[**→ Architecture & verification notes**](https://github.com/ametavinayak/kundli-architecture)

### UCI chess engine with NNUE evaluation
C++ engine, ~22k LOC. **Measured 3194 anchored Elo** against a gauntlet of published engines in the 3050–3350 band.

Every single change is gated by [SPRT](https://en.wikipedia.org/wiki/Sequential_probability_ratio_test) — sequential hypothesis testing that stops a match as soon as a patch is proven better or worse. It means most of my ideas get rejected by the data, which is the point. Several documented experiments here are *negative* results kept on the record, including one where the engine got 14% slower and I voided the entire prior rating measurement rather than quote a number I no longer believed.

### Electron-beam interference lithography simulator
Multi-fidelity (1D / 2D / 3D) first-principles simulator for a proposed nanolithography technique.

**The result was negative** — single-beam interference is not feasible for the target regime, and the simulation says why. Rather than drop it, I quantified the parallel-array pathway that *does* work, so the null result is usable by whoever tries next.

[**→ Repository**](https://github.com/ametavinayak/ebil-sim)

### Domain-specialised language model
QLoRA fine-tune of Qwen3-8B for astrology consultation, self-built corpora, served behind a local inference API and deployed to a live site.

Its most useful finding was unflattering: a paired evaluation harness showed that **four successive rounds of corpus work produced no measurable quality change.** I report the grounding score my instrumented run actually measured, not the higher number from the run I couldn't reproduce.

### Also
Counselling call/chat platform (Flutter + FastAPI, shipped to production) · operations ontology and reconciliation engine for a repacking business · IVR call-detail monitoring with dead-air alerting · a football video-editing pipeline with measured retention benchmarks.

---

## Tech

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white)

---

## Stats

<div align="center">

![](https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=ametavinayak&theme=github_dark)

![](https://github-readme-activity-graph.vercel.app/graph?username=ametavinayak&theme=github-compact&hide_border=true&area=true)

<sub>Most of my work is in private repositories — commercial engines and client systems.<br>
The public repo count is small on purpose; the contribution graph is the honest measure.</sub>

</div>
