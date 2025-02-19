# graph-vis
d3.js based graph visualisation

# System Dependency Diagram - Functionalities

## 1. Visualization of System Dependencies
- The diagram represents a **network of nodes and links**.
- Nodes are **different shapes** (circle, rectangle, triangle, ellipse, diamond, star) with unique colors.
- Links (edges) connect nodes, representing **dependencies**.
- Links have **arrowheads** to indicate direction.

## 2. Interactivity

### Node and Link Interaction
- **Clicking a node** highlights it and dims all unconnected nodes/links.
- **Clicking the background (SVG)** resets the highlighting.
- **Hovering over a node** displays a tooltip with its ID.
- **Dragging a node** allows repositioning while the simulation updates.

### Zoom & Pan
- Users can zoom in/out and pan around the diagram.

## 3. Physics Simulation with D3.js
- The layout uses a **force-directed graph simulation**, where:
  - `forceLink` manages link distance.
  - `forceManyBody` controls repulsion between nodes.
  - `forceCenter` aligns nodes towards the center.
- The nodes move dynamically according to these forces.

## 4. User-Controlled Settings
A **toolbar** allows users to modify parameters:
- **Link Distance**: Adjusts how far apart connected nodes should be.
- **Charge Strength**: Controls node repulsion.
- **Alpha Decay**: Controls simulation speed.

## 5. Data-Driven
- The diagram loads its structure from an **external JSON file** (`data.json`).
- This file contains:
  - A list of **nodes** with IDs, colors, and shapes.
  - A list of **links** connecting those nodes.

## 6. Responsiveness & Animation
- Nodes and links have **smooth opacity transitions** when selected/deselected.
- Tooltips have a **fade-in/out effect**.
- Nodes and links update their positions dynamically when dragged or when simulation parameters change.

## 7. Use Cases
- **Visualizing software dependencies** (e.g., microservices, system architecture).
- **Network analysis** (e.g., social networks, infrastructure).
- **Data relationships** (e.g., database schema dependencies).
