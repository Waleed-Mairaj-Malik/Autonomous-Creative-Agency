# Baby-AGI : Multi-Agent Creative Agency

A lightweight implementation of the **BabyAGI** multi-agent architecture, built as a learning project to understand autonomous task-driven agent loops.

## Pipeline

```
Interview -> Prompt Optimization -> Visual Rendering (via Pollinations AI)
```

Three core functions drive the loop:

- **`execution_agent()`** — does the work for the current task
- **`task_creation_agent()`** — decides the next task
- **`prioritization_agent()`** — cleans/reorders the task queue

The pipeline is linear with a hard stop once the poster renders, so it can't loop infinitely.

## How It Works

1. Ask the user for a creative brief.
2. Convert the brief into comma-separated image tags using local keyword matching (no external LLM needed).
3. Send the tags to Pollinations AI and display the generated poster.

## Tech Stack

Python 3, `collections.deque`, `urllib.parse`, Pollinations AI, `IPython.display` (Jupyter/Colab).

## Running

Open in Jupyter/Colab and run the cell — you'll be prompted for a creative brief, then the poster is generated and displayed automatically.

## Purpose

Built to explore how task execution, task creation, and prioritization can be split into separate agent responsibilities and looped together toward a goal.
