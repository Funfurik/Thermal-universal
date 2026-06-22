# Danger Thermal Universal — changelog

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
