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

This pattern is perfect for **board voting decisions** where we need:
- Multiple AI perspectives on complex business decisions
- Peer review to catch individual AI errors/biases
- Synthesized recommendation with confidence score

## Key Files to Port to TypeScript

| File | Purpose |
|------|---------|
| `backend/council.py` | 3-stage orchestration logic |
| `backend/openrouter.py` | Parallel AI queries |
| `backend/storage.py` | Conversation persistence |
| `CLAUDE.md` | Architecture decisions & gotchas |
| `frontend/src/components/Stage*.jsx` | UI for deliberation stages |

## Integration Plan for Equity Holder AIPA

1. **Port council logic** to `src/council/` (TypeScript)
2. **Use Oracle ATP** instead of JSON files for enterprise audit trail
3. **Adapt prompts** for board voting analysis (not general Q&A)
4. **Add document parsing** for board packs (PDF, Word, Excel)
5. **Deploy on Oracle Cloud** using existing $0/month infrastructure

## Target Use Case

AI Personal Assistant for equity holders in AI/Innovation startups:
- Analyze board meeting agendas
- Review financial documents
- Provide voting recommendations with reasoning
- Track voting history and outcomes

---
*Archived: December 2025*  
*Original: github.com/karpathy/llm-council*  
*Project: Equity Holder AIPA*
