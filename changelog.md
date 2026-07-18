# Danger Thermal Universal — changelog

## v4.9.20-alpha
- Internal cleanup: removed a leftover unused startup flag from the boot config; no change to thermal or overlay behavior
- Installation only on KernelSU / APatch / SukiSU — Magisk and Kitsune Mask are no longer supported

## v4.9.18-alpha
- Fix: the reboot fix shipped in 4.9.17 didn't fully take effect — the package still carried the old background-service binary, so after a reboot the FPS tile drew the overlay but only battery updated until you opened the WebUI once. The correct service binary (with the boot supervisor) is now bundled: tap the tile after a reboot and it counts FPS / frame time / GPU / DDR / NPU right away, no WebUI needed.
- Under the hood: moved to native Rust code, interface tidy-up, in-WebUI OTA updates, and a built-in statistics monitor.

## v4.9.17-alpha
- Fix: after a reboot, tapping the FPS-meter tile in the quick-settings shade now starts counting right away — you no longer have to open the WebUI first. The overlay's background service is brought up at boot instead of after the thermal setup finishes.

## v4.9.16-alpha
- New: built-in FPS / performance overlay (FPS, frame time, GPU/DDR/NPU load) — installs with the module, no separate app needed.
- The overlay and all thermal features are now completely free — no license key required.
- A license key is now needed only for the AI assistant chat.
- OTA updates are available to everyone.
- Overlay survives a reboot: the FPS service re-mounts debugfs and re-reads GPU memory on its own.
- Stability: bootloop self-recovery hardened, cleaner install, removed the diagnostic manifest file from the package.

## v4.8.9
- Fix: the license-key prompt was showing on every WebUI tab. It now appears only on the AI tab — thermal features keep working without a key.

## v4.8.8
- Fixed: after the 4.8.7 language update the WebUI AI chat froze on the "thinking…" indicator and never showed a reply. Resolved.
- The AI assistant still answers in your phone's system language.

## v4.8.7
- The WebUI now follows your phone's system language (full Russian / English interface).
- The AI assistant replies in your phone's system language.

## v4.8.6
- Copy button on every AI answer in the WebUI.
- Chat opens at the newest message (auto-scroll to bottom).
- AI assistant auto-reconnect — finds the server by itself, keeps working if the address changes.
- Anti-bootloop self-recovery: 3 failed boots in a row → the module auto-disables and saves a diagnostic log.
- Built-in WebUI AI assistant with per-device memory.
- Universal thermal throttling disable (Snapdragon).
