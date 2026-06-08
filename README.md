# 🏡 Home Assistant Blueprints

Welcome to my personal collection of Home Assistant blueprints. The goal here is simple: build automation blueprints that are **powerful, reliable, and entirely self-contained**—meaning zero messy dependency chains or endless external helpers to clog up your dashboard.

---

## 🔌 Featured Blueprint: Smart Climate with Occupancy Control

An all-in-one climate manager designed for "dumb" appliances (space heaters, window ACs, portable fans) connected to smart plugs. It bridges the gap between basic motion switches and full HVAC scheduling.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Frport%2Fha-blueprint%2Fblob%2Fmain%2Fsmart-climate.yaml)

### ✨ Core Features

* 🗓️ **Native Embedded Scheduling:** Configure allowed runtime hours and active days of the week right inside the blueprint UI. No external Home Assistant Schedule helpers needed.
* 🚶 **Smart Occupancy Binding:** Turns the appliance on when room presence is detected—but only if your specified user rules are met.
* 👥 **Multi-User Match Logic:** Flexibly manage shared rooms. Configure the system to run if **Any** assigned user is home or require **All** assigned users to be present.
* 🌍 **Proximity Device Pre-Op:** Seamlessly pairs with the modern Home Assistant Proximity device integration. It automatically detects when you are actively traveling *towards* home and pre-heats or pre-cools the room before you arrive.
* 🚨 **Wattage Fail-Safe Loop (Optional):** If your smart plug monitors power, this safety system checks real-time wattage. If the plug activates but draws 0W (e.g., the heater's physical knob is off or it got unplugged), it shuts off the plug immediately to protect components. It also handles mid-run power drops.
* ⏳ **Vacancy Auto-Off & Manual Override:** Includes a customizable empty-room safety shutdown timer. Need it to run continuously for a specific task? Flip an optional dashboard toggle helper to pause the auto-off countdown.
* 📲 **Targeted Device Notifications:** Sends clean, grouped push alerts directly to your mobile device via the Home Assistant Companion App.

---

## 🛠️ Configuration Blueprint Matrix

The automation evaluates your environment using a strict optimization hierarchy to prioritize energy savings:
