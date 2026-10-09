# DES MP — Indore Division TNA Dashboard (pilot)

A bilingual, single-file dashboard reporting the **Indore Division pilot** of a Statistical Training Needs Assessment (TNA) for the **Directorate of Economics and Statistics (DES), Government of Madhya Pradesh**. Implemented by **Pahlé India Foundation (PIF)**.

**Live:** https://samuelddavid.github.io/DES-TNA-Indore-Dashboard/

This pilot was the proof of concept that became the [statewide dashboard](https://github.com/samuelddavid/DES-TNA-MP-Dashboard) covering all 52 districts.

## Overview

Field staff across 8 district offices in Indore Division (Block Level Investigators, Assistant Statistical Officers, District Statistical Officers) answered a training-needs survey. The dashboard turns those responses into seven views:

| Tab | What it shows |
|---|---|
| Overview | Respondent counts by post and district office |
| Respondent Profile | Experience, education, device and internet access, learning preferences |
| Competency Ratings | Self-assessed scores per post, with the full 0–3 distribution behind each average |
| Integrated Priorities | Themes ranked by a combined priority-and-gap score |
| Software Training | Demand for specific statistical and office software |
| Workshop Roadmap | Suggested sequencing for delivery |
| Learning Readiness | Constraints that shape how training can actually be delivered |

A district filter re-renders every view, and the seven competency themes are:

- Survey Operations and Field Data Collection
- Data Management, Scrutiny and Quality Assurance
- Digital Tools and Office Systems
- Statistical, Economic and Planning Concepts
- Data Analysis, Statistics and Software
- Coordination, Monitoring and Citizen Interface
- Reporting, Documentation and Communication

## Tech

One `index.html`. No build step, no framework, no dependencies, no external scripts or CDN calls.

- Charts are hand-built SVG, generated with `createElementNS` and driven by the data objects at the bottom of the file
- Bilingual throughout: every label carries its Hindi equivalent
- Filter state re-renders all tabs from the same in-memory data

Clone it and open `index.html`, or serve the folder with any static server. That is the whole setup.

## A note on the sample

N = 23 for the division. The dashboard says so on every screen and carries a persistent "small sample, treat as indicative only" warning, because a 1-respondent district cannot support a confident claim. The statewide version exists precisely because this one was too small to act on.

## Data

Aggregate figures only: counts by district and post, mean competency scores with their distributions, and theme-level priority and gap percentages. **No personal or individual-level data** — no names, contact details or employee identifiers appear in this repository.
