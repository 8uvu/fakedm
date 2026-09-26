# FakeDM for Revenge

Injects fake local messages, calls, system messages, reactions and embeds into
any DM or channel — directly through Discord's own FluxDispatcher. Fakes persist
across restarts and re-inject automatically when Discord drops them.

Mobile port of the [Equicord fakeDM](https://github.com/Equicord/Equicord/tree/main/src/userplugins/fakeDM)
plugin by **8uvu aka Epitaph**.

## Install

Paste this URL into Revenge's plugin URL box (Plugins → ➕ → paste):

```
https://8uvu.github.io/fakedm/
```

Or add the plugin repository index to your plugin browser:

```
https://8uvu.github.io/fakedm/index.json
```

## Features

- **Fake messages** — any member (or pasted user ID) as sender, custom time & date, replies, image attachments, embeds (title / description / color / image)
- **Fake calls** — caller + receiver, missed or with duration
- **System messages** — joined, left, name change, icon change, pinned, joined server
- **Fake reactions** — any message ID + emoji, as any user
- **Batch conversations** — paste a `[14:30] Me: hey` / `[14:31] Name: sup` script and inject the whole conversation at once
- **Persistence** — fakes survive restarts; they re-inject on startup into channels where Discord dropped them
- **Fakes manager** — per-channel clear, delete individual fakes, edit cached fakes

## Notes

- Works with [MessageLogger](https://8uvu.github.io/msglog/dev.8uvu.message-logger/):
  clearing fakes dispatches an `mlDeleted` marker so logged fakes don't turn red.
- Edits work on messages currently in Discord's cache (open the channel first).
- Fakes are **local only** — they exist on your device, never sent to Discord's servers.

## Building

```bash
pnpm install
node build.mjs
```
