# FastAPI Best Practices

FastAPI done right. Async patterns, dependency injection, Pydantic v2 models, middleware, background
tasks, and project structure for production APIs.

## Install

### Cursor IDE

```
/add-plugin fastapi-best-practices
```

### Claude Code

```
/plugin install fastapi-best-practices
```

### Skills only (any agent)

```bash
npx skills add ofershap/fastapi-best-practices/fastapi-best-practices
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

### Skills

- **fastapi-best-practices** - FastAPI done right. Async patterns, dependency injection, Pydantic v2
  models, middleware, and project structure.

### Rules

- **best-practices** - Always-on rules that enforce current FastAPI patterns

### Commands

- `/audit` - Scan your codebase for FastAPI anti-patterns

## Why This Plugin?

AI agents are trained on data that includes outdated patterns. This plugin ensures your agent uses
current FastAPI best practices:

- Uses def for CPU-bound and async def for I/O-bound instead of making everything async or sync
- Uses Depends() instead of global variables for databases and config
- Uses Pydantic v2 (field_validator, ConfigDict) instead of deprecated v1 patterns
- Uses lifespan instead of deprecated @app.on_event
- Uses APIRouter and project structure instead of a single main.py
- Uses BackgroundTasks instead of asyncio.create_task for fire-and-forget work

## License

MIT
