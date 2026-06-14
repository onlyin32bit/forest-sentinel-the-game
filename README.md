# Forest Sentinel: Firebreak Command

A tactical wildfire containment game built with **Phaser 3** and custom Web Audio API procedural synthesis. 

Defend the **Community Safe Zone** (far-right column) from an encroaching wildfire spreading from the West. Establish network coverage, deploy firebreaks, and monitor the volatile winds to survive the 90-second containment window.

---

## 📋 Features

- **Phaser 3 Game Engine:** Direct canvas rendering of the $15 \times 10$ forest grid, interactive cells, dynamic range indicators, and custom particle effects (fire, smoke, and sonar sweeps).
- **Procedural Sound FX:** Dynamic Web Audio API sound generation. Synthesizes radar pings, tower deployments, backburn sizzles, fire crackles, and alarms natively without requiring any external assets.
- **Dynamic Wind Systems:** Fire spreads based on cellular automata rules influenced by a wind compass (North, South, East, West). Wind direction shifts every 12 seconds.
- **Data Analysis & Radar:** Scan localized cells to reveal incoming wind directions before they hit.
- **RF Network Mesh:** Construct tower nodes projecting a 3-tile Euclidean coverage circle.
- **Controlled Backburning:** Active forest cells within RF coverage can be burned to create permanent grey charcoal firebreaks that fire cannot cross.
- **Responsive Landscape HUD:** Glowing cyberpunk command console UI with real-time logs, live statistics, wind shift progress bars, and full desktop hotkey bindings.

---

## 🎮 How to Play

1. Open `index.html` in any web browser.
2. Select your active tool from the bottom panel or use keyboard shortcuts:
   - **`1`**: **Radar Scan** — Click on the grid to ping a location and reveal the next wind shift in the telemetry panel.
   - **`2`**: **Deploy RF** — Construct a network tower on a green forest tile (uses 1 RF charge; recharges every 15s).
   - **`3`**: **Backburn** — Click on any green tile inside a tower's green coverage circle to burn it, creating a grey firebreak.
3. Protect the far-right column (Safe Zone) for **90 seconds** to win.
4. If fire spreads to any tile in the safe zone, the shield fails and the mission is lost.

---

## 🛠️ Run Locally

You can launch a simple local web server to run the game:

### Using Python:
```bash
python3 -m http.server 8000
```
Then navigate to `http://localhost:8000`.

### Using Node.js:
```bash
npx http-server
```
Then navigate to the URL displayed in your terminal.
