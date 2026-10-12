# Personal module routing

This fork is based on Bobby Nicholas's MIT-licensed Omaland at
`ec232b6aa2e31b2f089ad89b653cd706989865b9`:
https://github.com/bobby-nicholas/omaland.

The license, authorship and upstream history remain unchanged. Personal
Full opacity window rules now share the existing managed block in
`~/.config/hypr/looknfeel.lua`; no FileView writes `hyprland.lua`. The same
generated Lua drives preview and persisted state. Hand-edited opacity in the
personal block is recognized on reload.

Use the arch-setups installer for pinned installation, menu reconciliation and
backups. It preserves unrelated JSONC menu entries and unmarked custom desktop
entries. Disable closes the editor and removes its launcher/menu references;
saved visual settings remain personal configuration. Removal backs up the real
personal module, entrypoint and integration files before removing source.

Existing users with an old Omaland block in the package entrypoint should review
and restore that entrypoint through the setup's supported configuration migration;
this fork deliberately never edits it to remove old blocks.

Regression verification: `node test/run.js` exercises the Lua reader and checks
Full opacity round-trips through the personal configuration body.
