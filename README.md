# Civil 3D MCP

**AI assistants that work with the drawings open in Autodesk Civil 3D 2020–2027 — and with DXF files.**

Civil 3D MCP is a free [MCP](https://modelcontextprotocol.io) server for Windows. Claude, ChatGPT, Cursor, VS Code, Windsurf,
Gemini, Codex and other AI assistants use it to read and work with the drawings open in Civil 3D on your PC, through a small
Civil 3D plug-in that only programs of your own Windows account can reach, and to read, check, compare and write DXF files
without Civil 3D.

**Status: no release is available yet, and Civil 3D MCP has not been tested in a real Civil 3D.** Reading Civil objects is implemented; creating or editing them is not.

**Download (once released):** [the latest release](https://github.com/SHMH-MCPs/civil3d-mcp-releases/releases/latest) — run
`Install-CIVIL3D-MCP.cmd` from it (no administrator rights needed). Then start Civil 3D; if it asks
"Security - Unsigned Executable File" about Civil3DMcp.dll, choose Always Load.

## What it does
- **Drawings:** open, create, save (only when you ask), units, statistics, drawing properties, system variables
- **Entities:** list, count, filter, read every property; create lines, polylines, arcs, circles, splines, text, MTEXT,
  hatches, dimensions, multileaders, tables, 3D solids; move, rotate, scale, mirror, copy, arrays; offset, join, split, extend
- **Organisation:** layers, layer states, linetypes, text and dimension styles, blocks, attributes, dynamic blocks, groups
- **Sheets:** layouts, viewports, PDF plotting, DXF and WBLOCK export
- **References:** external references and every dependency (images, underlays, fonts, plot styles) with missing files
- **Quality:** drawing checks with findings by handle, comparison with a standard drawing, purge, audit
- **Many drawings at once:** inspect, export or update text in DWG files without opening them
- **Any other part of Civil 3D's .NET API**, checked against a catalogue of every 2020–2027 release

Anything that erases, purges, replaces, closes or overwrites is shown as a preview first and needs your OK. Every change is
one Civil 3D transaction and one undo step, read back and reported as verified or not. Running commands, AutoLISP and API
methods is off unless you switch it on.

## Versions
| Civil 3D | Plug-in build | Status |
|---|---|---|
| 2026 | R25 (.NET 8) | **tested** in Civil 3D 2026 (25.1s): read self-test 36/36, write self-test 89/89 |
| 2025 | R25 (.NET 8) | designed for, **not yet tested** |
| 2021–2024 | R24 (.NET Framework) | designed for, **not yet tested** |
| 2020 | R23 (.NET Framework) | designed for, **not yet tested** |
| 2027 | R26 (.NET 10) | designed for, **not yet tested** |

Civil 3D-based products (Civil 3D, Architecture …) run the plug-in as plain Civil 3D. Civil 3D LT has no .NET API and cannot.

Civil 3D is a trademark of Autodesk, Inc. Civil 3D MCP is not affiliated with or endorsed by Autodesk. Nothing of Autodesk is
included: the plug-in uses the Civil 3D installed and licensed on your PC.
