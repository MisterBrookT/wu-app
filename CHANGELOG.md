# Changelog

## v0.2.1 — 2026-06-05 (afternoon)

### Out mode — GTD + Atomic Habits
- **Three-layer task view**: Today / This Week / Someday, with a smooth sliding tab indicator.
- **TaskItem animations**: check draws in (200ms stroke-dashoffset) → strikethrough → row collapses out (350ms).
- **Promote button** ↑: move tasks up a layer (Someday→Week→Today).
- **Inbox Clarify panel**: click any inbox item → panel slides in from right → press 1/2/3 to decide the layer → item moves to tasks, inbox marked done.
- **HabitsSection**: collapsible, streak counter, 7-day heat dots, check-in with spring emoji bounce, identity toast ("I am the kind of person who…").
- **Data**: `tasks.md` (three-layer GFM checklist) + `habits.json` (structured habit data).

### In mode — Stoic
- Ambient breathing animation (8s cycle, pauses while typing) — like candlelight, not a strobe.
- Philosophy quote library (19 quotes from Marcus Aurelius, Laozi, Confucius, etc.) appears 8s after writing stops. Click to dismiss.
- Multi-turn conversation: reply bar in ReflectionPane, Enter to send, Escape to clear. Wu's reflection is aware of today's tasks and inbox captures.

### Zero-friction onboarding
- First launch automatically creates `~/Documents/Wu` — no folder picker needed.
- Vault path visible in Settings → Preferences, with a "Change…" option.

### Global
- Mode switch animation upgraded (filter brightness + saturate, 420ms transition).
- In/Out mode badge (replaces Reflect/Act).

## v0.2.0 — 2026-06-05

### Reflect / Act dual-mode
- **Reflect mode** (warm) — the existing writing + AI reflection surface, now clearly named.
- **Act mode** (cool) — new two-column view: today's tasks on the left, quick Capture to inbox on the right.
- **Shift+Tab** switches between modes instantly, from anywhere — even inside the editor.
- The whole app shifts color tone: warm amber (Reflect) ↔ cool blue-grey (Act).
- Mode badge in the bottom-right corner shows which mode you're in.

### Wu identity
- Renamed from Mira to **Wu（悟）** throughout the app.
- Empty-state wordmark changed to italic serif (Wu).
- Tooltip and onboarding text updated.

### Codebase
- Crate renamed `mira` → `wu`, lib renamed `mira_lib` → `wu_lib`.
- Updater endpoint now points to `wu-app` public releases repo.
- Local project directory renamed `mira/` → `wu/`.

## v0.1.0 — 2026-06-03

First public release. 🐾

### Features
- **Mirror / Manage dual mode** — `⌘.` to switch between writing surface and notebook manager
- **AI Reflection** — press `⌘R` to ask Mira to reflect on your current note (streams token-by-token)
- **GTD Inbox capture** — press `⌘I` anywhere in mirror mode to instantly capture a thought to `inbox.md`
- **Dog avatar** — walking dog cursor while Mira is thinking; sits quietly when done
- **Smart auto-organize** — after reflection, Mira auto-tags notes and moves them to the right folder
- **Memory index** — reflections and index entries accumulate in `.mira/`, making Mira smarter over time
- **Onboarding** — 5-step guided checklist for new users
- **i18n** — English, 中文, 日本語, 한국어
- **License system** — free tier with built-in OpenRouter key; premium unlocks Claude models
- **Auto-updater** — silent background updates via GitHub Releases
- **System theme** — follows macOS dark/light mode automatically

### Technical
- Tauri 2 + React 18 + CodeMirror 6
- Refactored App.tsx into `useVault` / `useNotes` / `useOnboarding` / `useReflection` hooks
- ESLint + Prettier configured
