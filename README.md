# Home Assistant Automation Blueprints

This repository contains a collection of Home Assistant automation blueprints created to enhance and simplify your smart home experience. These blueprints are designed to work together, providing a robust motion-based lighting system with manual override (Do Not Disturb) capabilities.

## Available Blueprints

### 💡 Smart Motion Lighting - Main Controller

Automatically turns lights ON when motion is detected and OFF after a configurable delay. This automation only runs when the "Auto Mode" (Input Boolean) is enabled, allowing for flexible control over when the automation should be active.

[![Import to Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Flpsouza%2Fha-automation-blueprints%2Fmain%2Fmotion_light_control.yaml)

-   **Workflow:** Motion detected → Light ON (if Auto Mode enabled) → Motion stops → Wait delay → Light OFF.
-   **Companion:** Works best with the **DND Override** blueprint.

---

### 🌙 Smart Motion Lighting - DND Override

Intelligently manages the "Auto Mode" boolean. It enables "Do Not Disturb" (DND) mode when lights are manually turned OFF while motion is detected (preventing the light from turning back on immediately), and re-enables "Auto Mode" when lights are manually turned ON.

[![Import to Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Flpsouza%2Fha-automation-blueprints%2Fmain%2Fmotion_light_control_dnd.yaml)

-   **Workflow:** Light manually ON → Auto Mode enabled | Light manually OFF (while presence detected) → DND Mode enabled.
-   **Requirement:** Must use the same **Input Boolean** and **Motion Sensor** as the Main Controller.

## Getting Started

To get started with these blueprints:

1.  Ensure you have an **Input Boolean** created in Home Assistant to act as the "Auto Mode" switch.
2.  Click the **"Import to Home Assistant"** button for both blueprints above.
3.  Your Home Assistant instance will open and guide you through the import process.
4.  Create two automations using these blueprints, linking them to the same light, motion sensor, and input boolean.
