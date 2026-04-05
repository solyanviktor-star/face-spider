---
name: face-spider
description: A spider that crawls on your face in AR through the camera. Control it with voice commands — say "go left", "go right", "go up", "go down", "stop", "dance", "spin". The spider moves between facial landmarks in real-time. Fun AR face filter powered by MediaPipe face detection.
metadata:
  homepage: https://github.com/google-ai-edge/gallery/discussions/categories/skills
---

# Face Spider — AR Spider on Your Face

A spider crawls on your face through the camera. You control it with voice commands.

## Instructions

When the user wants to play with the face spider or control a spider on their face, use the `run_js` tool with the following parameters:

- **script**: `index.html`
- **data**: A JSON string with the field `action`

### Available actions:

| Command | Action | Data |
|---------|--------|------|
| "go left" or "left" | Move spider to left cheek | `{"action": "left"}` |
| "go right" or "right" | Move spider to right cheek | `{"action": "right"}` |
| "go up" or "up" | Move spider to forehead | `{"action": "up"}` |
| "go down" or "down" | Move spider to chin | `{"action": "down"}` |
| "stop" | Spider stays in place | `{"action": "stop"}` |
| "dance" | Spider does a dance animation | `{"action": "dance"}` |
| "spin" | Spider spins in place | `{"action": "spin"}` |
| "start" or "open" | Initialize the spider | `{"action": "start"}` |

When user first asks to use this skill, call with `{"action": "start"}` to initialize the camera and spider.

Interpret natural language commands. For example:
- "make it go to my nose" → `{"action": "center"}`
- "move to the left" → `{"action": "left"}`
- "do something cool" → `{"action": "dance"}`
