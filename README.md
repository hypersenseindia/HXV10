# HXV10 &mdash; Hypersense Final (Stable)

The v10 build of the Hypersense Termux toolkit: a dialog-driven performance console for mobile gaming, with an activation gate, an auto-start hook and a watchdog that restarts the tweak loop if it dies.

**Non-root.** Everything runs from `$HOME`; nothing is written to `/system`.

## Features

- `dialog`-based menu, with a plain CLI fallback when `dialog` is missing
- Activation-bound, time-locked start
- Auto-start integration and a watchdog process
- Structured config in `~/.hypersense/` with logs alongside
- Termux-safe under `set -o nounset` / `pipefail`

## Install

```bash
pkg update -y && pkg install -y git dialog
git clone https://github.com/hypersenseindia/HXV10
cd HXV10
bash HypersenseFinal_Stable.sh
```

The script writes `~/HypersenseFinal_Stable.sh` on first run and executes it from there.

## Files

```
HypersenseFinal_Stable.sh    bootstrap + main program
~/.hypersense/               config, state and logs (created on first run)
```

## Notes

- Activation is local and time-locked; there is no server call.
- Termux only. It will not run under a normal Android shell without Termux's package set.
- Performance scripts cannot change what the device firmware allows. Treat the gains as tuning, not magic.
---

<p align="center">
  <sub>Built by <b>AG HYDRAXFF</b> &mdash; HYPERSENSEGLOBAL &middot;
  <a href="https://www.instagram.com/hydraxff_yt/">@hydraxff_yt</a></sub>
</p>