# FastAPI Best Practices

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skills](https://img.shields.io/badge/skills.sh-fastapi--best--practices-blue)](https://skills.sh/ofershap/fastapi-best-practices/fastapi-best-practices)

FastAPI done right. Async/sync endpoint selection, `Depends()` for dependency injection, Pydantic v2 models, lifespan context managers, `BackgroundTasks`, `APIRouter`, `Annotated` types, and production project structure.

> AI coding assistants make every endpoint async, use global variables instead of `Depends()`, generate Pydantic v1 decorators, and put all routes in a single file. This plugin enforces the patterns that make FastAPI production-ready.

## Install

### Cursor / Claude Code / Windsurf

```bash
npx skills add ofershap/fastapi-best-practices/fastapi-best-practices
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

| Type | Name | Description |
|------|------|-------------|
| Skill | `fastapi-best-practices` | 10 rules for async patterns, Depends(), Pydantic v2, lifespan, APIRouter, and more |
| Rule | `best-practices` | Always-on behavioral rule that enforces current FastAPI patterns |
| Command | `/audit` | Scan your codebase for FastAPI anti-patterns |

## What Agents Get Wrong

| What the agent writes | What FastAPI best practice is |
|-----------------------|------------------------------|
| `async def` for everything | `async def` for I/O, `def` for CPU-bound |
| Global `db` variable | `Depends(get_db)` dependency injection |
| `@validator`, `class Config` | `field_validator`, `ConfigDict` (Pydantic v2) |
| `@app.on_event("startup")` | `lifespan` context manager |
| All routes in `main.py` | `APIRouter` with organized modules |
| `asyncio.create_task()` | `BackgroundTasks` for fire-and-forget work |
| `return {"error": "not found"}` | `response_model` + `status.HTTP_404_NOT_FOUND` |

## Related Plugins

- [python-best-practices](https://github.com/ofershap/python-best-practices) - Python 3.12+ type hints, Pydantic v2, uv, pathlib
- [vibe-guard](https://github.com/ofershap/vibe-guard) - Security guardrails for API endpoints

## Author

[![Made by ofershap](https://gitshow.dev/api/card/ofershap)](https://gitshow.dev/ofershap)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/ofershap)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github&logoColor=white)](https://github.com/ofershap)

## License

MIT
