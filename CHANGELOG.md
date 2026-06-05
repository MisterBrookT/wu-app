# Changelog

## v0.2.0 — 2026-06-04

### Renamed
- Product officially renamed to **Wu（悟）** — ancient wisdom, daily practice.
- Updated `productName`, `identifier`, i18n strings, and package name across the codebase.

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
