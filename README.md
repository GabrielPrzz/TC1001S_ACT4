# 🎯 Cannon Game

A simple arcade shooting game built with Python's `turtle` graphics library and the `freegames` package. Click to launch a ball and knock out incoming targets before they cross the screen.

## Description

Blue targets scroll in from the right side of the screen at random heights. Click anywhere to fire a red ball — it launches with velocity based on where you click and arcs under gravity. Hit all the targets to keep playing; miss one and the game ends.

## Requirements

- Python 3.x
- [`freegames`](https://pypi.org/project/freegames/) library

Install the dependency with:

```bash
pip install freegames
```

## How to Run

```bash
python cannon.py
```

## Controls

| Input | Action |
|-------|--------|
| **Mouse click** | Launch the ball toward the clicked position |

Click closer to the bottom-left to shoot at a shallow angle; click higher or further right to launch faster and steeper.

## Gameplay

- **Targets** (blue dots) spawn on the right edge at random heights and drift left continuously.
- **Click** anywhere on the screen to fire the red ball from the bottom-left corner.
- The ball travels in an arc, pulled downward by simulated gravity.
- A target is **destroyed** when the ball comes within 13 pixels of it.
- The game **ends** when any target reaches the left edge of the screen.
- The ball can only be re-launched once it leaves the screen boundaries.

## Project Structure

```
cannon.py     # Main game file
```

## Customization Ideas

- **Target speed** — Increase the `target.x -= 0.5` value to make targets move faster.
- **Spawn rate** — Lower the `randrange(40)` threshold to spawn targets more frequently.
- **Gravity** — Adjust `speed.y -= 0.35` to change how steeply the ball arcs.
- **Ball size / hit radius** — Change the `> 13` collision threshold or the `dot(6, ...)` size.
- **Multiple balls** — Extend the code to allow several balls in flight at once.

## License

This project is based on the [freegames](https://github.com/grantjenks/free-python-games) library by Grant Jenks, released under the Apache 2.0 License.
