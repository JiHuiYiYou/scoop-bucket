# scoop bucket — JHYY (机会翼游)

A personal [Scoop](https://scoop.sh) bucket for the JHYY compiler.
**Not** the [Scoop Main](https://github.com/ScoopInstaller/Main) bucket — inclusion
there is a separate decision.

## Install

```powershell
scoop bucket add jhyy https://github.com/JiHuiYiYou/scoop-bucket
scoop install jhyy
```

This installs the same Burn bundle that is attached to the
[GitHub release](https://github.com/JiHuiYiYou/JiHuiYiYou-compiler/releases)
(`jhyy-installer-<version>.exe`); Scoop verifies its SHA-256 before running it.

**MSYS2 is not required** — since v4.1.0 the installer bundles a minimal native
ucrt64 toolchain (gcc + binutils + CRT) under `C:\Program Files\JHYY\toolchain\`.

## Update

```powershell
scoop update
```

The manifest's `autoupdate` block resolves the newest tag from the upstream tags
page and the checksum from the release's `SHA256.txt` — both regexes are
exercised against the live pages.

## Uninstall

```powershell
scoop uninstall jhyy
```

⚠️ This is a **per-machine** install (it writes to `C:\Program Files\JHYY` and to
the machine PATH) ⇒ it needs elevation (UAC prompt).

## Other channels

- winget: `winget install JiHuiYiYou.JHYY`
- direct download:
  <https://github.com/JiHuiYiYou/JiHuiYiYou-compiler/releases/latest>

## License

MIT — see the [LICENSE](https://github.com/JiHuiYiYou/JiHuiYiYou-compiler/blob/main/LICENSE)
of the main repository.
