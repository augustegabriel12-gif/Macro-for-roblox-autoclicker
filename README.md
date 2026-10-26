# Roblox Macro Studio

A lightweight desktop macro recorder for Windows, built with Python and Tkinter. Record keyboard actions, mouse clicks, and sampled mouse movement; replay macros; run an auto-clicker; or repeat a selected key.

> **Camera movement note:** Roblox may lock the cursor or process camera input differently from normal desktop mouse movement. This app records relative mouse deltas and amplifies them slightly during playback, but camera rotation may still be imperfect or unsupported in some Roblox experiences. If the camera does not behave correctly, disable camera movement in your macro and use keyboard/click actions instead.

## Features

- Record and replay keyboard presses and releases.
- Record mouse clicks with screen coordinates.
- Sample mouse movement, with denser sampling while a mouse button is held.
- Relative mouse movement playback for a best-effort camera movement attempt.
- Repetition count and playback speed controls.
- Auto-clicker with configurable interval.
- Key repeater with a **Choose a key** capture dialog, including Space and supported special keys.
- Emergency stop with **F8**.
- Save and load macros as JSON.
- English interface by default, with French available in Settings.
- Dark and light appearance themes.

## Requirements

- Windows 10 or later recommended.
- Python 3.10 or later.
- `pynput`.

## Run from source

1. Install Python from [python.org](https://www.python.org/downloads/). During setup, enable **Add Python to PATH**.
2. Download or clone this repository.
3. Open PowerShell in the project folder.
4. Install the dependency:

   ```powershell
   py -m pip install -r requirements.txt
   ```

5. Start the app:

   ```powershell
   py Roblox_Macro_Studio.py
   ```

If `py` is unavailable, try replacing it with `python`.

## Controls

- **F6**: start/stop recording (the default recording hotkey can be changed in the app).
- **F7**: clear the macro.
- **F8**: emergency stop for playback and repeating tools.
- Playback waits three seconds before starting, so you can focus the target window.

## GitHub release packaging

The repository includes the Python source, dependency list, license, ignore rules, and this README. A Windows executable is not included; run from source using the instructions above.

## Safety and compatibility

- Test macros in a safe window before using them in a game.
- Avoid infinite repeats unless you can stop the app reliably.
- Synthetic input may not be accepted by every game or anti-cheat/input system.
- This project is an independent community tool and is not affiliated with or endorsed by Roblox.
