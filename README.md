# UE5 ProDJLink Plugin

**Beat Link Trigger / Pioneer Gear Support for Unreal Engine 5**

This plugin links **Unreal Engine 5** with Pioneer CDJs and DJM mixers via [Beat Link Trigger](https://github.com/Deep-Symmetry/beat-link-trigger). It supplies a Blueprint-friendly interface and asset system for synchronizing gameplay, visuals, and other events with DJ equipment.

⚠️ **Disclaimer:** I am not affiliated with Pioneer, and this plugin is provided for educational/experimental purposes only.

---

## ✨ Features
- Connects Unreal Engine to Pioneer CDJs and mixers over Pro DJ Link.
- Uses OSC as the transport layer (requires UE5 OSC plugin).
- Includes an interface (`IProDJLinkListener`) for subscribing actors to DJ sync events.
- Events provide **Info objects** containing tempo, beat, looping, track metadata, and more.

---

## 📦 Requirements
1. **Unreal Engine 5** (tested with UE5).
2. **OSC Plugin** (comes with UE5, enable it in Plugins).
3. **Beat Link Trigger** running on your system.
   - Make sure it detects your Pioneer setup.
   - A preset file for linking it with this plugin is included.

---

## ⚙️ Installation & Setup
1. Install and enable the **OSC plugin** in Unreal.
2. Install **Beat Link Trigger** and confirm it can see your CDJs/DJM.
3. Install the included **Beat Link Trigger** preset file.
4. Copy this plugin into your UE5 project’s `Plugins/` folder.
5. Place a **BP_ProDJLinkManager** into your level.  
   - Default settings should work with the included Beat Link Trigger preset.  
   - You may adjust IP and port if needed.  
   - Changing internal settings is not recommended unless you also edit the preset file.
6. Any Actor that needs to respond to DJ events should:  
   - Implement the `IProDJLinkListener` interface.  
   - Handle incoming events (tempo, beat, looping state, track title, etc.).

---
