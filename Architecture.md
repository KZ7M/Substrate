# System Architecture

## Core Principles

1. **Homeostasis first**: All behavior serves internal balance
2. **No explicit goals**: Agent defines its own objectives
3. **Emergence over engineering**: Complex behavior from simple rules
4. **Observability**: We can inspect internal states, "read the mind"

## Homeostatic Variables

| Variable | Range | Depletion | Critical? |
|----------|-------|-----------|-----------|
| `energy` | 0-100 | Over time, action cost | Yes (death at 0) |
| `safety` | 0-100 | Proximity to threats | No (flight, not death) |
| `information` | 0-100 | Novelty of environment | No (curiosity drive) |
| `social` | 0-100 | Isolation | No (optional for v1) |

## Action Space

- `move(direction, speed)` — costs energy
- `consume(resource)` — restores energy
- `rest()` — restores energy, no info gain
- `observe()` — gains information, no energy cost
- `communicate(agent, signal)` — social, costs energy

## Reward Function

Not external. Derived from homeostatic gradient:

reward = Σ(w_i * Δhomeostasis_i / Δt)


Agent maximizes **rate of homeostatic improvement**.

## Cognitive Engine (v1)

- **Policy**: PPO or SAC
- **State**: [energy, safety, info, social] + sensory input
- **Action**: discrete or continuous action space
- **Memory**: none (v1), then RNN/Transformer

## Future Extensions

- **Episodic memory**: "Where did I find food before?"
- **World model**: Predict environment dynamics
- **Meta-learning**: Adapt drives themselves
- **Multi-agent**: Social dynamics, culture
