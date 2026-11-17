# Glide Files

The file manager of the [Glide desktop](https://github.com/Glide-Desktop): tabs,
archives, file operations with undo, Trash on every volume, phones and cameras,
and the file chooser behind `xdg-desktop-portal-glide`.

## Build

```sh
cargo build --release
```

The shared crates come from a tag of
[glide-libs](https://github.com/Glide-Desktop/glide-libs). To build against a
checkout of glide-libs next to this one, create `.cargo/config.toml` (ignored
by git):

```toml
[patch."https://github.com/Glide-Desktop/glide-libs"]
glide-app = { path = "../glide-libs/crates/glide-app" }
glide-config = { path = "../glide-libs/crates/glide-config" }
glide-sdk = { path = "../glide-libs/crates/glide-sdk" }
glide-theme = { path = "../glide-libs/crates/glide-theme" }
```

Split from the Glide monorepo with its history in November 2026.
