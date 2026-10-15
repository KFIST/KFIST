<h1 align="center"><a href="https://farhadkhan.in">Farhad Khan</a></h1>
<p align="center">
  Reverse engineering for Windows binaries, device tools, and firmware.<br>
  <a href="https://farhadkhan.in">farhadkhan.in</a>
</p>

The binary stays on the bench. The note is what gets kept: names, offsets, and the path through the program.

## What gets opened

| | |
| --- | --- |
| **Windows** | Packed EXEs and DLLs. Sections, imports, delayed loads, and the call that does the work. |
| **.NET** | WPF and WinForms. Where the screen ends and native code begins. |
| **Qt** | Desktop clients. The window, the worker, and the request that leaves the machine. |
| **Flash stacks** | MediaTek Boot ROM and download-agent libraries. Exports, the session, and the stage. |
| **Device clients** | How a service tool builds identity, what it stores, and how it reaches the phone. |
| **Protocols** | HTTPS and WebSocket. Message shape, update checks, and command paths. |
| **Firmware** | Image layout, the filesystem, and the files that matter. |

## How a note runs

`triage` — file type, hashes, architecture, entropy, and whether a packer is in the way.

`format` — sections, entry point, imports, exports, and libraries loaded later.

`structure` — the objects that own the work. Sessions, stages, and the functions that move them.

`boundary` — where native code, managed code, and the network meet.

`result` — names, offsets, and flow. Keys and tokens stay out of the note.

## Bench

Ghidra · x64dbg · WinDbg · ILSpy · dnSpy · Frida · Python · C · C# · Qt
