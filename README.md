<h1 align="center">KFIST</h1>
<p align="center">
  Reverse engineering for Windows binaries, device tools, and firmware.
</p>
<p align="center">
  <img alt="Windows PE" src="https://img.shields.io/badge/Windows%20PE-141414?style=flat-square" />
  <img alt=".NET" src="https://img.shields.io/badge/.NET-141414?style=flat-square" />
  <img alt="Qt" src="https://img.shields.io/badge/Qt-141414?style=flat-square" />
  <img alt="MediaTek" src="https://img.shields.io/badge/MediaTek-141414?style=flat-square" />
  <img alt="Firmware" src="https://img.shields.io/badge/Firmware-141414?style=flat-square" />
  <img alt="Protocols" src="https://img.shields.io/badge/Protocols-141414?style=flat-square" />
</p>

I take a program apart until the structure is clear, then write that structure down so it can be read without the binary open.

## What I reverse

| Area | What I open | What the note shows |
| --- | --- | --- |
| **Windows native** | 32-bit and 64-bit EXEs and DLLs, including packed modules | Sections, imports, exports, delayed loads, and the call sites that do the real work |
| **.NET desktop** | WPF and WinForms tools | CIL flow, where the UI stops, and where native code starts |
| **Qt clients** | Qt desktop tools | Windows, workers, and the requests the client sends |
| **Flash stacks** | MediaTek Boot ROM and download-agent libraries | Public exports, the session object, and the stage the tool is in |
| **Device clients** | Service and login tools | How identity is built, what is stored on disk, and how the tool reaches the phone |
| **Protocols** | HTTPS and WebSocket clients | Message shape, update checks, and command paths |
| **Firmware** | Device images and embedded filesystems | Layout, the files that matter, and how the image is packed |

## How a note is written

The same order every time, so a note stands on its own.

1. **Triage.** File type, hashes, architecture, entropy, and whether a packer is sitting on the code.
2. **Format.** Sections, entry point, imports, exports, and libraries loaded later.
3. **Structure.** The objects that own the work. Sessions, stages, and the functions that move them.
4. **Boundary.** Where native code, managed code, and the network meet.
5. **Result.** Names, offsets, and flow. Keys, tokens, and private material stay out of the write-up.

## Toolchain

| Job | Tools |
| --- | --- |
| Static | Ghidra |
| Debug | x64dbg, WinDbg |
| Managed | ILSpy, dnSpy |
| Dynamic | Frida, when the sample is mine to run |
| Notes and builds | Python, C, C#, Qt |

## Scope

Study of software I am allowed to open. Notes describe how a program is built. They do not publish keys, credentials, or steps that break someone else's lock.
