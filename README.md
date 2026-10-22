# Ronin — showcase

**Portfolio:** [ahelijao.github.io](https://ahelijao.github.io/) · Chapter I  
**Private source:** not linked (IP / full app)

> Docs-only public view. No binaries, no API keys, no full source tree.

## Elevator

Desktop **AI translator** — terminal-inspired UI, local-first, glossary-aware. Built to stay in the writing flow when language and jargon mix.

## Need

| Pain | Response |
|------|----------|
| Context switches for translation | Always-on lightweight desktop app |
| Models rewrite protected terms | Custom **glossary** — listed terms stay untouched |
| Cloud-only assistants | Local model path (e.g. Ollama-class runtime) as a design option |

## Architecture (sanitized)

```text
┌─────────────────────────────┐
│  Desktop UI (Tk / terminal) │
│  themes · fonts · shortcuts │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│  Translation service        │
│  prompt + glossary merge    │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│  Local / remote LLM runtime │
└─────────────────────────────┘
```

**Also explored:** Android port notes (Kotlin) for a portable “terminal” twin — same product idea, different shell.

## What this demonstrates

- Ship a real **local product**, not only a notebook
- Bind an LLM with **business rules** (glossary), not raw chat
- Packaging mindset (desktop distributable)

## Stack

`Python` · desktop UI · `Ollama`-style local inference · JSON glossary · packaging (`PyInstaller`) · optional Android port study

## Explicitly not in this repo

Application source, models, icons/build artifacts, credentials.


## Full source (private)

Access required. The implementation lives in a **private** repository:

- [Project-Ronin](https://github.com/AHelijao/Project-Ronin)

Without collaborator access, GitHub will show **404**. To request access: email [helijao.andriamandranto@gmail.com](mailto:helijao.andriamandranto@gmail.com), message on [LinkedIn](https://linkedin.com/in/helijaoa), or open an issue on **this** showcase repo — I’ll grant access case by case.

---

← back to [portfolio](https://ahelijao.github.io/) · Helijao Andriamandranto
