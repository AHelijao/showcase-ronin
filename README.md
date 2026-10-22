# Ronin — showcase

**Portfolio:** [ahelijao.github.io](https://ahelijao.github.io/) · Chapter I  
**Private source:** access required (links below)

> Docs-only public view. No binaries, no API keys, no full source tree.

## Elevator

**AI translator** in two shells: a lightweight **desktop** app, plus a **portable Android** twin — same idea (glossary-aware, terminal-inspired), different platform.

## Need

| Pain | Response |
|------|----------|
| Context switches for translation | Always-on lightweight app |
| Models rewrite protected terms | Custom **glossary** — listed terms stay untouched |
| Desktop-only limits mobility | **Android** portable version (Kotlin) |
| Cloud-only assistants | Local model path (e.g. Ollama-class) as a design option on desktop |

## Architecture (sanitized)

### Desktop

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

### Portable — Android app

```text
┌─────────────────────────────┐
│  Android UI (Kotlin)        │
│  terminal / high-contrast   │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│  Same product rules         │
│  EN↔FR · glossary · jargon  │
└─────────────────────────────┘
```

Same product contract: efficient translation, preserve technical vocabulary, stay out of the way.

## What this demonstrates

- Ship a real **local product**, not only a notebook
- Bind an LLM with **business rules** (glossary), not raw chat
- Packaging on **desktop** and a **native Android** port

## Stack

**Desktop:** `Python` · desktop UI · `Ollama`-style local inference · JSON glossary · `PyInstaller`  
**Mobile:** `Kotlin` · Android (native) · terminal-style UX

## Explicitly not in this repo

Application source, APKs, models, icons/build artifacts, credentials.

## Full source (private)

Access required. Implementations live in **private** repositories:

- Desktop: [Project-Ronin](https://github.com/AHelijao/Project-Ronin)
- Android portable: [Portable-Ronin](https://github.com/AHelijao/Portable-Ronin)

Without collaborator access, GitHub will show **404**. To request access: email [helijao.andriamandranto@gmail.com](mailto:helijao.andriamandranto@gmail.com), message on [LinkedIn](https://linkedin.com/in/helijaoa), or open an issue on **this** showcase repo — I’ll grant access case by case.

---

← back to [portfolio](https://ahelijao.github.io/) · Helijao Andriamandranto
