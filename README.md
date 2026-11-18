# <Project Name> — Research Agent

> ODSC × Nebius Hackathon submission · Challenge: *Build a research agent that brings its sources*

**One-line pitch:** <What question does your agent answer, and for whom?>

- **Demo video (2–3 min):** <link>
- **Team:** <names / GitHub handles>

## The problem
<Who is the user? What research task does the agent help them finish? Why does it matter?>

## How it works
```
question → plan queries → Tavily search → select & dedupe evidence → Nebius Token Factory synthesis → answer with citations
```
- **Query planning:** <how the agent decides what to search and when to stop>
- **Evidence handling:** <how sources are filtered, deduplicated, checked>
- **Safety:** <how web content is kept separate from trusted instructions>
- **Trade-offs:** <latency, cost, reliability>

## Required services
| Requirement | How we use it |
|---|---|
| Nebius Token Factory (inference) | Model: `<model name>` — <role in the agent> |
| Tavily (real-time web search) | <how results feed the model and how links survive into answers> |

## Setup
```bash
git clone <repo-url>
cd <repo>
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env   # add your keys — never commit them
python src/agent.py "Your research question here"
```

## Example
**Question:** <example question>
**Answer (excerpt):** <answer with [1], [2] citations>
**Sources:** [1] <url> · [2] <url>

## Failure / insufficient-evidence case
<Show what the agent does when search returns nothing useful or a tool fails.>

## Judging criteria map
| Criterion | Weight | Where to look |
|---|---|---|
| Sourced and verifiable answers | 30% | Example above, demo 0:00–… |
| Works end to end | 25% | Setup, demo |
| Usefulness | 20% | The problem |
| Agent design | 15% | How it works |
| Use of Token Factory and Tavily | 10% | Required services |

## License
MIT
