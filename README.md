# Sentient Mechanics Toy Model – Draft 1 Specification

## Project Name
`sentient-toy-model`

## Purpose
To create the simplest possible computational toy model that demonstrates a plausible isomorphic mapping between:

- A subject-centered reality of goal-directed sentient agents (**teleons**) that exchange qualia according to their relatively fixed telos, and  
- An object-centered reality of emergent "physical" structures (elementary particle-like entities, atom-like bound states, molecule-like composites) obeying apparent conservation laws and dynamics.

The model must show that **higher-level structures (e.g., "molecules") can emerge from smaller coalitions of teleons than the lower-level structures (e.g., "atoms") they compose**, consistent with the user's insight that more telic coordination is required to produce stable microscopic entities than macroscopic ones.

## Core Philosophical Constraints
1. **Teleons are the sole ontological primitives** (Ruliad nodes = individual teleons).
2. Each teleon has:
   - An internal state representing its current **qualescape** (input qualia from connected teleons).
   - A relatively fixed **telos** (decision kernel / update rule) mapping qualescape → output qualia.
3. **No bare information or abstract bits** – all "information" is experiential from the inside.
4. Spacetime, particles, fields, and chemistry emerge from persistent patterns in teleon dynamics.
5. Higher physical stability at microscopic scales arises from **larger, more tightly coordinated coalitions** of teleons, not more primitives.

## Minimal Viable Model Goals (Version 0.1)
1. Define a small set of teleon types with distinct, fixed teloi.
2. Allow teleons to form dynamic connections (experienced as quale exchange).
3. Run a discrete-time multiway evolution (lightweight Ruliad slice).
4. Show emergence of:
   - Stable "elementary particle" states (highly coordinated large clusters with rigid behavior).
   - "Atom-like" bound states (even larger, more complex coalitions).
   - "Molecule-like" composites (smaller coalitions of the above, with richer but inherited dynamics).
5. Visualize or log patterns that resemble binding, excitation, and reaction.

## Technical Stack (Draft 1)
- Language: **Python 3.11+**
- Core libraries: `numpy`, `networkx`, `matplotlib`, `pygame` (for optional real-time visualization)
- No external dependencies beyond the standard scientific stack
- Structure as a pure library + optional scripts for simulation and visualization

## Key Components

### 1. `teleon.py`
```python
class Teleon:
    def __init__(self, teleon_id: int, telos_type: str, initial_state: int)
    
    # Properties
    id: int
    telos_type: str                     # e.g., "fermion_A", "boson_link", "attractor"
    state: int                          # discrete quale value (0 to N_QUALIA-1)
    connections: List[int]              # IDs of teleons it directly influences
    
    def update(self, input_qualescape: Dict[int, int]) -> int
        # Fixed rule based on telos_type mapping input dict → output quale