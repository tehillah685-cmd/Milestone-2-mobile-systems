# BioPulse Monitoring System

**COMP826 Mobile Systems Development: Milestone 2 (UI/UX role)**

BioPulse is a mobile emergency response system designed to improve personal safety through physiological monitoring and automated emergency escalation. It works alongside a proposed SkinGrip wearable patch that measures Galvanic Skin Response (GSR) to detect sudden threats and start an emergency workflow.

This repository contains the UI/UX design artefacts, the high-fidelity screens, a clickable prototype, usability evaluation material and project documentation.

## Live prototype

**https://tehillah685-cmd.github.io/Milestone-2-mobile-systems/**

Open this link on a phone to try the app. The prototype is `index.html` in the root of this repository.

## Key features

- User authentication and account management
- NFC tap-to-pair with the wearable patch
- Real-time GSR monitoring dashboard and vitals
- GSR spike detection with an escalation countdown
- Face ID / Touch ID cancellation of false alarms
- Emergency screen with location sharing and SOS escalation

## Repository structure

| Folder / file | Contents |
| --- | --- |
| `index.html` | The clickable prototype (single file, no installation needed) |
| [`personas`](personas) | User personas |
| [`user stories`](user%20stories) | User stories |
| [`branding`](branding)|Branding
| [`User Journey`](User%20Journey) | User journey map |
| [`BioPulse Wireframes`](BioPulse%20Wireframes) | Wireframe images |
| [`High Fidelity Screens`](High%20Fidelity%20Screens) | Final high-fidelity UI screens |
| [`Usability Metrics`](Usability%20Metrics) | Usability evaluation forms and results |
| [`Development methodology`](Development%20methodology) | Trello board evidence and process artefacts |
| `README.md` | This file |

## Design process

The design followed a user-centred approach:

**Personas → User Stories → User Journey Mapping → Wireframes → High-Fidelity Prototypes → Evaluation**

## How to run the prototype

The prototype is a single HTML file. It has no build step, no dependencies and no backend.

### Option 1: on a phone (recommended)
1. Open the live link above in your phone's browser (Chrome on Android, Safari on iPhone).
2. Optional: use *Share → Add to Home Screen* to launch it full screen.

### Option 2: on a computer
1. Download this repository (**Code → Download ZIP**) and unzip it.
2. Double-click `index.html` to open it in your browser.
3. To view it at phone size, press `F12`, then `Ctrl+Shift+M` (`Cmd+Shift+M` on Mac) and choose a phone such as *iPhone 14 Pro* or *Pixel 7*.

### Option 3: Android Studio emulator
1. In the repository folder, run `python3 -m http.server 8000`.
2. In the emulator's Chrome browser, go to `http://10.0.2.2:8000`.

### Option 4: iOS Simulator (Mac)
1. In the repository folder, run `python3 -m http.server 8000`.
2. In Simulator's Safari, go to `http://localhost:8000`.

An internet connection is needed for the intended fonts. Without one, the prototype still works with default fonts.

## Using the prototype

Every button works. On a computer, a screen list appears beside the phone. On a phone, the `...` button at the top right opens the same list.

To try the full alert flow:
1. Open **Notifications** (the Alert tab) and tap **Threat Detected**.
2. The spike alert appears, then a 5-second countdown starts.
3. Either tap **Disarm now (FaceID / TouchID)** to cancel, or let the countdown reach zero (or tap **Escalate Immediately**) to reach the **Emergency** screen.

You can jump to any screen by adding its name to the link, for example `#vitals`, `#spike`, `#countdown`, `#emergency`.

| Screen | Link ending |
| --- | --- |
| Welcome | `#welcome` |
| Login | `#login` |
| Create account | `#signup` |
| Forgot password | `#forgot` |
| NFC pairing | `#pair` |
| Dashboard | `#dashboard` |
| Vitals | `#vitals` |
| Notifications | `#alerts` |
| GSR spike detected | `#spike` |
| Escalation countdown | `#countdown` |
| Biometric cancel | `#cancel` |
| Alert cancelled | `#cancelled` |
| Emergency active | `#emergency` |
| Alert resolved | `#resolved` |

## Notes

- This is a UI/UX prototype. Biometric checks, NFC pairing, GSR readings, the map and emergency calling are **simulated**. Nothing is sent or stored, and no call is placed.
- The Vitals screen was added after the original screen set so that every tab in the navigation bar leads somewhere.
- Milestone 1 proposed Flutter as the implementation framework. This submission covers the UI/UX role, so the design is delivered as a browser-based prototype. See Section 4.7 of the final report.


