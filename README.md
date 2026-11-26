# Lune — Unraid Community Applications Templates

Official Unraid Community Applications (CA) template repository for [Lune](https://github.com/LuneServer/lune) (*Your universe. Your media.*).

## Templates

- [`templates/lune.xml`](templates/lune.xml) — Lune Media Server (`ghcr.io/luneserver/lune:latest`)

## Notes for Unraid Users

- **Permissions:** Defaults to `PUID=99` (`nobody`), `PGID=100` (`users`), and `UMASK=002`. The container entrypoint automatically syncs ownership on `/data` and grants supplementary group access to `/dev/dri` when passed through.
- **Ports:** Defaults to `LUNE_EDGE_MODE=local` on port `5863`. Ports `80` and `443` are left blank by default so they do not conflict with the Unraid WebGUI — if you enable built-in ACME HTTPS (`LUNE_EDGE_MODE=acme`), assign a custom `br0` IP or map free host ports.
- **Hardware Transcoding:** If your Unraid server has an Intel QuickSync or AMD VAAPI GPU, enter `/dev/dri` in the **Hardware Transcoding GPU** advanced field.

## Support

- Issues & feature requests: [LuneServer/lune/issues](https://github.com/LuneServer/lune/issues)
