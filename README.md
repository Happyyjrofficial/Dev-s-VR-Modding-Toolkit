# Dev's VR Modding Toolkit

**Version:** v1.5  
**Support server:** [discord.gg/devtaggering](https://discord.gg/devtaggering)

---

## Features

### Anti-Cheat Remover
- Removes anti-cheat files and objects based on a large database of known names.
- Two modes:
  - **Folder mode**: select a game folder, creates a `*_clean` copy with anti-cheat files renamed to `.bak`.
  - **File mode**: select a `data.unity3d` file, removes anti-cheat objects (requires UnityPy).
- Optional content scan for keywords: `anticheat`, `antidll`, `antideletion`, `antidisable`, etc.
- Logs every removed item with path/name.

### Library Injector
- Injects a `.so` library into a chosen architecture folder.
- Simple copy operation with logging.

### APK Decompiler/Compiler
- Decompiles an APK using `apktool`.
- Compiles a decompiled folder back into an APK.
- Requires `apktool` in system PATH.

### Metadata String Editor
- Separate GUI for editing `global-metadata.dat`.
- Browse, load, search, replace strings.
- Optional deobfuscation via `deobfuscator.dat` (format: `obfuscated=original` per line).
- After deobfuscation, saves as `global-metadata-deobfuscated.dat` and creates `RENAME_TO_global-metadata.dat.txt`.

### Photon Spammer
- Sends repeated HTTP requests to Photon region endpoint (default `us`).

### PlayFab Spammer
- Creates multiple PlayFab accounts using:
  - CustomID
  - AndroidDeviceID
  - iOSDeviceID
- Configurable device type, account count, and optional display names.

### Logging
- All operations are logged in the GUI.
- Option to save log to a text file.

### Modern Dark GUI
- Scrollable canvas with sections.
- Loading screen for long operations.
- Dark theme using ttk styling.

---

## Requirements

- Python 3.x
- Python packages:
  - `tkinter` (usually included)
  - `requests`
  - `UnityPy` (optional, for unity3d anti-cheat removal)
- External tools:
  - `apktool` (for APK decompile/compile)
  - `Il2CppDumper` (not integrated, but recommended for advanced metadata work)

---

## Usage

Run the script:
