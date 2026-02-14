## Description
DOJUTSU is a Naruto technique visualizer. It combines the MediaPipe hand tracking library with Three.js to recreate iconic techniques using particle effects — triggered by real hand seals performed in front of your webcam.

![Demo GIF](https://github.com/user-attachments/assets/8ad2b871-02c0-4b97-95f3-34682e745be0)

## Features

This project uses 20,000 particles to render volume-based techniques activated through hand seal sequences:

* **Lightning Blade: Chidori**
    * **Visuals:** A chaotic lightning ball with a dense glowing core and jagged electric bolts.
    * **Trigger:** Seal sequence **Ox → Hare → Monkey**.

* **Fire Style: Fireball Jutsu**
    * **Visuals:** A fiery explosion dispersing outward with a dense blazing core.
    * **Trigger:** Seal sequence **Snake → Tiger → Monkey → Boar → Horse**.

* **Ope Ope no Mi: Room**
    * **Visuals:** A hollow sphere with cyan grid lines (equator + meridian rings) and an energy field shell.
    * **Trigger:** Hold **Monkey** seal for 5 seconds (charging effect begins at 2s).

* **Domain Expansion: Malevolent Shrine**
    * **Visuals:** A dark, ominous domain with a blood-red floor, towering pillars, and a curved roof.

## Hand Poses Reference

The program detects the following hand poses based on which fingers are extended. Use one hand in front of the webcam:

| Seal Name | Index | Middle | Ring | Pinky | Description |
|-----------|:-----:|:------:|:----:|:-----:|-------------|
| **Ox** | ✓ | ✗ | ✗ | ✓ | Index + Pinky extended, middle + ring curled |
| **Hare** | ✗ | ✗ | ✗ | ✗ | Closed fist, all fingers curled |
| **Monkey** | ✓ | ✓ | ✓ | ✓ | All fingers extended (open hand) |
| **Tiger** | ✓ | ✓ | ✗ | ✗ | Index + Middle extended |
| **Snake** | ✓ | ✗ | ✗ | ✗ | Only Index finger extended |
| **Boar** | ✗ | ✓ | ✓ | ✓ | Middle + Ring + Pinky extended |
| **Horse** | ✓ | ✓ | ✓ | ✗ | Index + Middle + Ring extended |

> **✓** = finger extended &nbsp;&nbsp; **✗** = finger curled

### How Sequences Work
1. Perform each seal one at a time in front of the camera.
2. Hold each seal steady until the name appears on screen, then switch to the next seal.
3. You have **3 seconds** between seals before the sequence resets.
4. Once the full sequence is recognized, the technique activates.

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
