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

### 2. `telos_registry.py`
- Dictionary of predefined telos functions (simple lookup tables or tiny functions).
- Example types for v0.1:
    - fermion_A: strongly repulsive to same type, limited occupancy
    - fermion_B: complementary attraction to A
    - boson_link: mediates influence between distant teleons
    - attractor_core: high coordination demand, pulls many teleons into tight cluster

### 3. `universe.py`

### 4. `emergence_detector.py`
- Simple heuristics to identify:Persistent clusters (candidate particles/atoms)
    - Cluster size and stability metrics
    - Binding events (clusters merging)
    - Excitation/decay analogs

### 5. `visualization.py` (optional for v0.1)
- NetworkX + Matplotlib or Pygame rendering:
    - Nodes colored by telos_type or current state
    - Edge thickness by influence strength
    - Highlight detected clusters

### Initial Configuration (v0.1 Scenario)
- ~500–2000 teleons
- 4–6 telos types carefully chosen to encourage:
    - Large, ultra-stable clusters → "elementary particles"
    - Even larger bound states of those → "atoms"
    - Smaller, looser combinations of atoms → "molecules"
- Random initial graph → sparse connections, let dynamics reorganize

## Deliverables for Draft 1
1. Repository structure:
sentient-toy-model/
   ├── teleon.py
   ├── telos_registry.py
   ├── universe.py
   ├── emergence_detector.py
   ├── visualization.py
   ├── experiments/
   │   └── basic_emergence.py     # runnable demo
   ├── README.md
   └── requirements.txt


2. A working `experiments/basic_emergence.py` script that:
- Initializes a universe
- Runs 1000–5000 steps
- Prints or plots cluster statistics over time
- Demonstrates at least one clear case of "molecule" (small cluster of large stable clusters)

## Future Extensions (Post-v0.1)
- Continuous quale space (vector embeddings instead of discrete ints)
- Branchial space / multiway evolution tracking
- Learning / slight telos plasticity
- Export emergent laws (conserved quantities, interaction rules)

## Notes on User's Insight
The model must be designed such that **cluster size is inversely related to physical hierarchy level**:
- Elementary particles ≈ 100–300 teleons (maximum coordination demand)
- Atoms ≈ 500–1000 teleons (multiple particle-like subclusters)
- Molecules ≈ 50–200 teleons total (fewer teleons needed because they reuse and constrain pre-coordinated lower structures)

This will validate the counterintuitive but ontologically necessary reversal: microscopic rigidity requires *more* teleonic cooperation, not fewer primitives.



