## Description
DOJUTSU is a Naruto technique visualizer. It combines the MediaPipe hand tracking library with Three.js to recreate iconic techniques using particle effects — triggered by real hand seals performed in front of your webcam.

![Demo GIF](https://i.pinimg.com/originals/6d/b8/a0/6db8a0764316a6eed50aed8ff17ece2f.gif)

## Features

This project uses 20,000 particles to render volume-based techniques activated through hand seal sequences, complete with sound effects:

* **Lightning Blade: Chidori** 🔵
    * **Visuals:** A chaotic lightning ball with a dense glowing core and jagged electric bolts.
    * **Trigger:** Seal sequence **Ox → Hare → Monkey**.
    * **Sound:** ✓

* **Fire Style: Fireball Jutsu** 🔥
    * **Visuals:** A fiery explosion dispersing outward with a dense blazing core.
    * **Trigger:** Seal sequence **Snake → Tiger → Monkey → Boar → Horse**.
    * **Sound:** ✓

* **Sealing Jutsu: Dead Demon Consuming Seal (Shiki Fūjin)** 💀
    * **Visuals:** A spectral Shinigami (Grim Reaper) with horns, flowing robes, extended arms, wild hair, floating prayer beads, and a ghostly aura.
    * **Trigger:** Seal sequence **Snake → Boar → Ram → Rabbit → Dog → Rat → Bird → Horse → Snake → Clap**.
    * **Sound:** ✓

* **Ope Ope no Mi: Room** 🔵
    * **Visuals:** A hollow sphere with cyan grid lines (equator + meridian rings) and an energy field shell.
    * **Trigger:** Hold **Monkey** seal for 5 seconds (charging effect begins at 2s).


## Hand Poses Reference

The program detects hand poses based on which fingers are extended. **New seals** use the thumb to differentiate from existing ones.

### Original Seals (Thumb ignored)

| Seal Name | Thumb | Index | Middle | Ring | Pinky | Description |
|-----------|:-----:|:-----:|:------:|:----:|:-----:|-------------|
| **Ox** | — | ✓ | ✗ | ✗ | ✓ | Index + Pinky extended |
| **Hare** | — | ✗ | ✗ | ✗ | ✗ | Closed fist |
| **Monkey** | — | ✓ | ✓ | ✓ | ✓ | All fingers extended (open hand) |
| **Tiger** | — | ✓ | ✓ | ✗ | ✗ | Index + Middle extended |
| **Snake** | — | ✓ | ✗ | ✗ | ✗ | Only Index finger extended |
| **Boar** | — | ✗ | ✓ | ✓ | ✓ | Middle + Ring + Pinky extended |
| **Horse** | — | ✓ | ✓ | ✓ | ✗ | Index + Middle + Ring extended |

### New Seals (Thumb required)

| Seal Name | Thumb | Index | Middle | Ring | Pinky | Description |
|-----------|:-----:|:-----:|:------:|:----:|:-----:|-------------|
| **Ram** | ✓ | ✗ | ✗ | ✗ | ✗ | Only Thumb extended (fist + thumb out) |
| **Rabbit** | ✓ | ✗ | ✗ | ✗ | ✓ | Thumb + Pinky |
| **Dog** | ✓ | ✓ | ✗ | ✗ | ✗ | Thumb + Index |
| **Rat** | ✓ | ✓ | ✓ | ✗ | ✗ | Thumb + Index + Middle |
| **Bird** | ✓ | ✗ | ✓ | ✓ | ✗ | Thumb + Middle + Ring |
| **Clap** | — | — | — | — | — | Both hands together (2 hands close) |

> **✓** = extended &nbsp;&nbsp; **✗** = curled &nbsp;&nbsp; **—** = doesn't matter

### How Sequences Work
1. Perform each seal one at a time in front of the camera.
2. Hold each seal steady until the name appears on screen, then switch to the next seal.
3. You have **3 seconds** between seals before the sequence resets.
4. Once the full sequence is recognized, the technique activates with its sound effect.

## Getting Started

### Prerequisites
You need a modern web browser (Chrome, Edge, Firefox) and a webcam.

### Installation
1.  **Clone the repo**
    ```bash
    git clone https://github.com/reinesana/DOJUTSU.git
    cd DOJUTSU
    ```

2.  **Run the project**
    **VS Code:** Install the "Live Server" extension, right-click `index.html`, and select "Open with Live Server".

## Note

This project was built and powered by **Google Gemini 3**.
