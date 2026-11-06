# ProteinBuilder — downloads

Standalone builds of **ProteinBuilder**, the cage-design app. Nothing to install
beyond the app itself: no Python, no conda, no command line.

## Which file do I need?

| Your computer | Download |
| --- | --- |
| Mac, Apple silicon (M1 / M2 / M3 / M4) | `ProteinBuilder-arm64.dmg` |
| Mac, Intel processor (2018 or newer) | `ProteinBuilder-x86_64.dmg` |
| Windows 10 / 11 | `ProteinBuilder-windows.zip` |

**Not sure which Mac you have?**  → Apple menu → *About This Mac*.
"Chip: Apple M…" means Apple silicon; "Processor: Intel…" means Intel.

**Macs need macOS 14 (Sonoma) or newer.** On an older macOS the app will not
start. For Intel Macs that effectively means 2018 or later, since those are the
oldest machines Sonoma supports.

The `.zip` files are the same apps, for passing around on a USB stick or in a
shared folder when downloading isn't convenient.

## Installing on a Mac

1. Open the `.dmg` and drag **ProteinBuilder** into **Applications**.
2. The first time you open it, macOS says:

   > "ProteinBuilder is damaged and should be moved to the Trash."

   In the Terminal, once:

   ```bash
   xattr -dr com.apple.quarantine /path/to/ProteinBuilder.app
   ```

   (Copying the app from a USB stick instead of downloading it avoids this
   warning entirely — the warning comes from the download, not the app.)

## Installing on Windows

Unzip and run `ProteinBuilder.exe`. Windows SmartScreen will warn that it's from
an unrecognised publisher, for the same reason as above: click **More info →
Run anyway**.

## Using it

- Double-click the app. A browser tab opens at `http://localhost:8501`.
  Everything runs **on your own machine** — nothing is uploaded anywhere.
- Click the app icon again at any time to open another tab on the same session.
- **To quit:** close the browser tab. The app shuts itself down about a minute
  later. (It has no window of its own, so there is nothing else to close.)
- **You need an internet connection** to fetch structures from the PDB and to
  load the 3D viewer.
- Sequence design with ProteinMPNN runs on a free Colab GPU rather than on your
  laptop — the ProteinMPNN tab gives you the notebook and the files to upload.
- If the app misbehaves, the log is at `~/Library/Logs/ProteinBuilder.log`
  (macOS); send it along with any bug report.

## Source code

The source lives in a private repository — ask the team for access.
