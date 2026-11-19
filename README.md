# Studio Shutdown Protocol

Studio Shutdown Protocol is an interactive Windows utility designed to protect studio audio interfaces and reference monitors from high-amplitude transient pops and thumps during computer shutdown.

Instead of powering off immediately, it displays a high-contrast, full-screen checklist that requires you to zero your audio interface knobs and switch off your monitors before Windows shuts down.

## Features

- **Enforced Interactive Checklist:** Requires confirming two physical hardware steps before shutdown is enabled:
  1. Set the audio interface knobs to zero.
  2. Turn off the reference monitors.
- **Visual LED Indicators:** Each checklist item features a status LED that switches from red to green upon confirmation. The **SHUT DOWN COMPUTER** button remains disabled until both items are green.
- **10-Second Cancellable Countdown:** Starts a 10-second countdown before executing a clean, non-forced Windows shutdown (`shutdown /s /t 0`), allowing programs with unsaved work to prompt you first.
- **Studio-Ready Full-Screen UI:** A dark, borderless, always-on-top (`-topmost`) interface with Windows DPI awareness designed for dim studio environments.
- **Keyboard Shortcuts:** Press `1` and `2` to toggle checklist items, and `Esc` to cancel an active countdown or exit the application.
- **Shutdown Result Verification:** Checks the `shutdown.exe` exit code and displays an error dialog if Windows rejects the request instead of failing silently.

## How It Works

This tool is a standalone launcher you run manually at the end of a studio session—it does **not** hook into or replace the standard Windows Start menu shutdown.

1. Launch `StudioShutdownPro.exe`.
2. Zero your audio interface potentiometers and power off your reference monitors.
3. Click each item on screen (or press `1` and `2`) to turn both indicators green.
4. Click **SHUT DOWN COMPUTER** to start the 10-second countdown (press `Esc` or **CANCEL** at any time to abort).

## Development Note

AI-assisted tools were utilized in the generation and structuring of this project's source code and documentation. All code has been reviewed, compiled, and tested by the author.
