# 🎯 AIdeazz Reference: Karpathy's LLM Council

## Why This Code Is Here

Reference copy of [Andrej Karpathy's llm-council](https://github.com/karpathy/llm-council) for the **Equity Holder AIPA** project.

## Key Pattern: 3-Stage Multi-LLM Deliberation

```
Stage 1: Multiple AIs give independent opinions (Gemini, Claude, Grok)
    ↓
Stage 2: Each AI reviews and ranks the others (anonymized to prevent bias)
    ↓
Stage 3: Chairman AI synthesizes final recommendation
```

## Key Files to Port to TypeScript

| File | Purpose |
|------|---------|
| `backend/council.py` | 3-stage orchestration logic |
| `backend/openrouter.py` | Parallel AI queries |
| `backend/storage.py` | Conversation persistence |
| `CLAUDE.md` | Architecture decisions & gotchas |
| `frontend/src/components/Stage*.jsx` | UI for deliberation stages |

## Integration Plan

1. Port council logic to `src/council/` (TypeScript)
2. Use Oracle ATP instead of JSON files
3. Adapt prompts for board voting decisions
4. Add document parsing for board packs

---
*Archived: December 2025 | Original: github.com/karpathy/llm-council*
