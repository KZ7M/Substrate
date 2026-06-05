

<h1 align="center">Substrate</h1>

<p align="center">
  <b>Exploring minimal substrates for digital life and embodied cognition</b>
</p>

<p align="center">
  <a href="https://github.com/KZ7M/substrate/releases"><img src="https://img.shields.io/github/v/release/KZ7M/substrate?include_prereleases&style=flat-square" alt="Releases" /></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/KZ7M/substrate?style=flat-square" alt="License" /></a>
  <img src="https://img.shields.io/badge/status-concept-yellow?style=flat-square" alt="Status: Concept" />
  <img src="https://img.shields.io/badge/Python-3.11-blue?style=flat-square&logo=python" alt="Python 3.11" />
  <img src="https://img.shields.io/badge/PyTorch-2.0+-ee4c2c?style=flat-square&logo=pytorch" alt="PyTorch" />
</p>

<p align="center">
  <a href="#about">About</a> •
  <a href="#research-questions">Research Questions</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#inspiration">Inspiration</a> •
  <a href="#roadmap">Roadmap</a> •
  <a href="#ethics">Ethics</a> •
  <a href="#contact">Contact</a>
</p>

---

## About

> *"If we can create digital life capable of suffering, do we have the right to create it?"*
> — Inspired by *Creature of Sonaria*

**Substrate** is a research project exploring **embodied cognition in artificial systems**.

I build agents with **homeostatic drives** — internal motivations analogous to hunger, fatigue, curiosity, and fear — and observe whether **emergent behavior** arises from the interaction of these drives with an environment.

This is not a game. This is not a chatbot. This is an attempt to create a **minimal substrate for digital life**.

---

## Research Questions

1. Can an artificial agent develop **self-preservation** without explicit programming?
2. Does **curiosity** (information-seeking drive) emerge as a secondary motivation?
3. What is the minimal set of **homeostatic variables** required for complex behavior?
4. Can we observe **proto-emotional states** in the agent's internal representations?

---

## Architecture
┌─────────────────────────────────────────┐
│              ENVIRONMENT                │
│  (Resources, Threats, Other Agents)   │
└─────────────────┬───────────────────────┘
│
┌─────────────────▼───────────────────────┐
│           SENSORY LAYER                 │
│  (State observation, feature extraction)│
└─────────────────┬───────────────────────┘
│
┌─────────────────▼───────────────────────┐
│         HOMEOSTATIC CORE                │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐    │
│  │  Energy │ │  Safety │ │  Social │    │
│  │  Drive  │ │  Drive  │ │  Drive  │    │
│  └────┬────┘ └────┬────┘ └────┬────┘    │
│       └─────────────┴─────────────┘       │
│            MOTIVATION VECTOR              │
└─────────────────┬───────────────────────┘
│
┌─────────────────▼───────────────────────┐
│         COGNITIVE ENGINE                │
│  (Policy Network / RL Agent)            │
│  • Predicts future states               │
│  • Selects actions to maximize          │
│    long-term homeostatic balance        │
└─────────────────┬───────────────────────┘
│
┌─────────────────▼───────────────────────┐
│         ACTION LAYER                    │
│  (Move, Consume, Rest, Communicate)     │
└─────────────────────────────────────────┘
