# The Rigby Foundation

Open tools for a private internet, and an operating system written from the
ground up, because why not.

[rigby-foundation.org](https://rigby-foundation.org) · [NuggetVPN](https://nugget.rigby-foundation.org)

---

## 🍗 Nugget — the VPN stack

A free, good-looking client for the subscription you already have, and
everything around it.

| Repo | What |
|------|------|
| [**NuggetVPN**](https://github.com/Rigby-Foundation/NuggetVPN) | The desktop client for Windows, macOS and Linux (Wails v3 + React 19). Every proxy core is compiled **into** the app as a Go library: no bundled executables, nothing downloaded or shelled out to at runtime. |
| [NuggetVPN-Mobile](https://github.com/Rigby-Foundation/NuggetVPN-Mobile) | The Android client, native Kotlin + Jetpack Compose, on sing-box. VLESS/Reality, VMess, Trojan, Shadowsocks, Hysteria2, TUIC, WireGuard. |
| [nuggetsync](https://github.com/Rigby-Foundation/nuggetsync) | Zero-knowledge sync backend for NuggetVPN, in Rust. *"Stupid, but reliable."* |
| [nuggetpanel](https://github.com/Rigby-Foundation/nuggetpanel) | A redesigned [Remnawave](https://docs.rw/) panel in the Nugget look; talks to an unmodified Remnawave backend. AGPL-3.0 fork, not affiliated with Remnawave. |
| [TodayCore](https://github.com/Rigby-Foundation/TodayCore) | Experimental sing-box core with the modern Xray-core features needed to speak to current Xray deployments, as client and server. Beta. |
| [nuggetvpn-www](https://github.com/Rigby-Foundation/nuggetvpn-www) | [nugget.rigby-foundation.org](https://nugget.rigby-foundation.org) |

## 🖥️ sic — an operating system

A monolithic kernel in C for **x86_64**, **32-bit big-endian PowerPC** (G4
PowerMacs) and **aarch64**, with its own system call ABI, its own file system,
and a userland that runs DOOM, tcc, Python and Ren'Py games. Boots on real PCs
from UEFI or legacy BIOS.

| Repo | What |
|------|------|
| [**sic**](https://github.com/Rigby-Foundation/sic) | The kernel: SMP, preemptive processes and threads, copy-on-write fork, signals, ptys and job control; a VFS with tmpfs, **zaefs**, FAT and ext2/3/4; NVMe, AHCI, IDE and UFS disks; an IPv4 stack with TCP and BSD/Unix sockets; HD Audio; loadable modules. |
| [zaeboot](https://github.com/Rigby-Foundation/zaeboot) | The bootloader, in Zig: x86_64 UEFI, arm64 UEFI and legacy BIOS. |
| [musl](https://github.com/Rigby-Foundation/musl) | musl 1.2.5, ported to sic's system call ABI. |
| [zae](https://github.com/Rigby-Foundation/zae) | **Z**AE **A**ll-purpose **E**nvironment, the userland: init, shell, core tools, zaefs tools, insmod/rmmod, and ports (tcc, DOOM, Python 2, busybox, libc++). |
| [zwm](https://github.com/Rigby-Foundation/zwm) · [zgl](https://github.com/Rigby-Foundation/zgl) · [zde](https://github.com/Rigby-Foundation/zde) | Window server, OpenGL 2.1 on the host GPU (virgl), and a desktop with SDL2 and Ren'Py ports. |

The projects meet only through the sic ABI and a sysroot, so each builds on
its own. Contributing? Read the `CODE_OF_CONFLICT` first.

## ⚡ Karui — a web framework

| Repo | What |
|------|------|
| [**Karui**](https://github.com/Rigby-Foundation/Karui) | Full-stack TypeScript with its own JSX runtime: islands, SSR and file-based routing, zero runtime dependencies, 7.6 kB gzipped. `npx @rigbyhost/karui create my-app` |
| [KaruiDocs](https://github.com/Rigby-Foundation/KaruiDocs) | The docs (English and Russian), built with Karui itself. |
| [www](https://github.com/Rigby-Foundation/www) | [rigby-foundation.org](https://rigby-foundation.org) |

---

<sub>Write working code, don't break userspace.</sub>
