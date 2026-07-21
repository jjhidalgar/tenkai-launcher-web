# 0.6.0

- **21 new languages** — the app is now localized in Portuguese (Brazil & Portugal), Hindi, Indonesian, German, Japanese, Korean, French, Vietnamese, Turkish, Italian, Arabic, Traditional & Simplified Chinese, Dutch, Swedish, Thai, Polish, Russian, Filipino, Malay, and Romanian (previously English and Spanish only).
- **Pick your language in-app** — all new languages are selectable from Settings and registered for per-app locale switching.
- **Automatic crash reports** — a new feature lets you help improve the app by sending anonymous crash reports. You can opt-out through settings.
---

# 0.5.0

- **New Gesture**: Spreading two fingers apart ("squeeze out") on the home screen now directly opens widget edit mode.
- **Built-in Icons**: System Actions and Quick Actions (e.g., WiFi, DND, Bluetooth toggles) now have default built-in icons, showing appropriate visuals automatically.
- **Improved Brightness Math**: Fixed a bug where brightness settings were excessively bright. The slider now uses Hybrid Log-Gamma curve conversion to match human perception and standard Android slider behaviors.
- **Visual & Translation Polish**: Added correct plural forms for Spanish translations and cleaned up unused localization assets.
---

# 0.4.0

- **Tenkai Capsules** — a new Compose-native home-screen widget that shows live text built from tokens like `{time}`, `{date}`, `{battery}`, `{charging}`, `{wifi}`, `{volume}`, `{track}` and `{artist}`. Customize font, size, weight, colors, background, border, shadow, alignment, and an optional icon, with a live preview as you edit. Set an optional tap action, or leave it non-tappable.
- **Tenkai Action Icons** — a new tappable home-screen icon that runs any action (launch an app, toggle a setting, open a pie…). It can use the app's own icon and scales to fill the widget as you resize it.
- **Widget Automations** — home-screen widgets (including Capsules) can now appear or hide automatically based on live system state: Wi‑Fi (any/specific SSID/not connected), Bluetooth (audio or selected devices), battery & charging, power saver, ringer mode, Do Not Disturb, and wired headset. A redesigned, more visual editor makes rules easy to build.
- **Free Draw mode** — a new home-pie assignment mode. Draw lines across the wallpaper to split the screen into custom areas, then tap an area to assign a pie to it.
- **App-wide font** — choose a font family used throughout the launcher, and set an independent launcher text size that ignores your phone's system font scaling. Tenkai Capsules can override the font family and weight per-capsule.
- **Classic Docks redesign** — a reshaped Classic Docks settings screen for managing app-icon docks on the home screen, with quick-access buttons to control the dock.
- **App drawer improvements** — cleaner frame, new context-menu options to add apps to a Classic Dock, a Space, or a Virtual Space, and settings integration.
- **Fresh-install home screen** — new installs now start with clock and date Capsules placed at the top of the first space, with tap actions wired to your clock and calendar apps.
- **Redesigned premium pages** — each premium feature now has its own explanation page with a live preview of the feature and a direct link to upgrade. Clicking a locked feature takes you straight to its page.
- **Improved tutorials & help** — clearer introduction flow, better "edit pies" and "open app drawer" walkthroughs, and updated examples.
- **Quick settings & control dock** — improved quick-settings toggles and unified control dock.
- **Larger, better-scaled pies** — pies now use geometric-mean scaling for more consistent proportions, plus a new pie font-size setting.
- **New system icons** — additional Material Symbols available to assign to actions and buttons.
---

# 0.3.0

- **Classic Dock**: A brand-new feature providing a traditional home screen dock. Customize appearance (opacity, lines, spacing), show notification badges (with options to filter out silent notifications), and configure easily with real-time preview and setup dialogs.
- **Multiple Widgets per Virtual Space**: Place and position multiple widgets inside a single Virtual Space. Resize, align, and organize them dynamically.
- **Pie Action Badges**: Get notification badges directly on the Pie menu slices for quick updates on unread notifications.
- **Work Profile Support**: Fixed work profile app icon overrides so that apps in the work profile map and cache icons independently.
- **Visual & UI Refinement**: Updated icons for Space, Virtual Space, and widget editing; fixed alignment issues in the settings screens.
- **Localization**: Added full Spanish translations for the new classic dock and widget options.
---

# 0.2.0

- **Subpie placement presets** — one tap configures the whole subpie behavior at once, shown as selectable cards in Pie settings:
  - **Locked**: the subpie stays exactly where the parent opened and never follows your finger.
  - **Follow Finger (default)**: the subpie starts trailing your finger once you commit to a swipe.
  - **Follow Finger (Center Button)**: the subpie follows your finger while keeping the center button under it, so a quick swipe lands ready on the center action.
- **Advanced pie behavior settings** — for fine-tuning beyond the presets:
  - **Subpie Placement**: open a subpie in the *Same Location* as its parent, or *Cursor* placement that travels in the swipe direction.
  - **Cursor placement**: choose whether the subpie appears centered on your finger or at its inside edge (default) — the inside edge softens the "teleport" jump.
  - **Pie Limit Barrier**: an invisible ring — move past it in any direction and the whole pie drags along with your finger (Inner Circle ±1px, 20/40/60/80%, or Outer Circle).
  - **Same-direction Barrier**: turn on a barrier placed only in the direction you were already swiping (so a long opening swipe no longer traps you far from center), with a configurable barrier distance.
- **Redesigned tutorial** — the guide is now split into **Beginner** and **Advanced** sections. The new *Pies & Subpies Placement* tutorial walks you through the three presets on live mini-pies, then lets you apply the one that feels best in one tap.
- **Smarter app search** — the app drawer now normalizes accents/diacritics, so searching "cafe" matches "Café" and results are more consistent.
- **Fixed** a bug where a subpie could open twice when using instant access within a pie.
- **Better default pies on initial install** — Fresh installations and configuration resets now set up a rich 4-pie layout (Main, Social, Utilities, Productivity) with dynamic vendor app discovery (e.g. Phone, Browser, Camera, Music, Calendar), global package deduplication, slice padding fallback constraints, and a cohesive monochrome white icon scheme.
---

# 0.1.0

- No changes.

---

# 0.0.14

- **Custom pie icons:** Each pie can now have its own icon. It appears in the pie list and is used automatically wherever that pie opens as a nested sub-pie. You can set it from the pie editor or override just the slice icon.
- **Smarter icon overrides:** The action editor now clearly separates a *Custom Slice Icon* (this slice only) from a *Custom Global App Icon* (that app everywhere, including the app drawer), each with a preview and the icon's name. Pie actions can override the target pie's icon too.
- **>Pressing outside< behavior:** New setting controlling what a second-finger tap outside an open pie does — *Nothing*, *Close Pie*, or *Go to parent pie* (steps back through nested sub-pies). A long press outside always closes the pie.
- **Better back navigation:** When you step back to a parent pie, it now reappears where the current pie is, so your finger stays near the center.
- **Delete confirmation:** Deleting a pie or removing a widget now requires a second tap to confirm, preventing accidental deletion.
- **Action type icons:** The action-type dropdown in the pie editor now shows an icon for each type (App, Pie, System, Shortcuts, etc.).
- **Restart Launcher:** New button in Settings to cleanly close and relaunch the app to apply changes or recover from issues.
- **Icon fixes & polish:** Icon packs now apply immediately; the selected pack is correctly restored on startup/reset; icon search works with spaces (e.g. "face messenger") and shows the selected icon's name; app icons are centered with their label when labels are always shown.
- **Multi-activity apps:** Apps that expose several launcher activities (e.g. Calculator++) now show the correct per-activity icon in pies and menus.
- **Spanish localization:** The new "Pressing outside behavior" and "Restart Launcher" settings are now fully translated to Spanish.
- Fixed spurious/double haptic feedback when navigating between pies.
---

# 0.0.13

- Minor changes
---

# 0.0.12

- **Virtual Spaces** — Define ephemeral boxes containing your own customized widgets, and pop them up as floating overlays straight from a pie slice whenever you need them. Add, edit, name, and resize each space.
- **Lock Screen action** — A new system action that turns off and locks the screen (requires enabling the new accessibility service).
- **Improved widget creation menu** — Now includes a search box and a live preview of each widget before you add it.
- **A-Z bar placement** — New setting to move the alphabet navigation bar to the left edge of the screen (defaults to the right).
- **Better shortcut search** — Improved app search when picking apps for shortcuts.
- **Pie editing improvements**:
  - New pies now start with 2 slices.
  - Slice labels always show in the editing preview, regardless of your display settings.
  - The appearance section is hidden while a slice's action isn't fully configured.
- **Material Symbols** — System and quick actions now use Material Symbols icons for a cleaner look.
- **Icons on special settings buttons** for easier navigation.
- **Clearer premium features** — Each premium feature now has a short title and a one-line description (more pies, premium themes, custom icon packs, contextual menus, multiple touch zones, hide apps, virtual widget spaces).
- **Smoother subscriptions** — Reworked payment and grace-period handling: your settings are preserved but premium features are gracefully disabled at runtime when a subscription lapses, with clearer grace-period messaging.
- Changelog is now rendered with formatting, like the in-app help guides.
---

# 0.0.11

- **Settings Reorganization**: Reorganized the settings layout into five clean tabs: General, Home, Pies, Drawer, and About.
- **In-App Changelog**: Added a "What's New" viewer in the About tab to read update history directly inside the app.
- **Visual Slice Editor**: Select, edit, and reorder slices by tapping directly on the visual pie preview instead of just using a list.
- **Easier App Selection**: Added search boxes to both the hidden apps selection menu and the edit slice app picker.
- **Global Icon Overrides**: Created a new screen under General settings to centrally view, edit, or remove all custom app icons.
- **Tutorial & Phrasing Improvements**:
  - Re-wrote tutorials to match the new settings organization.
  - Added pages for assigning pies to home screen zones and setting the default launcher.
  - Updated helper graphics (like the Squeeze gesture guide) and added clear action buttons at the end of help screens.
- **Widget Dock Control**: Added an option to hide/show the "Add Widget" (+) button in the quick dock, and polished the widget edit mode UI.
- **Haptic Feedback**: Added haptics when transitioning to a cursor-centered subpie.
- **Drawer Layout Units**: Made app drawer icon and label size settings consistent with the main pie configurations.
---

# 0.0.10

Here is the new release of Tenkai Launcher!

- Add app from drawer to pie
- Configurable Pie Sizes
- Render help pages with some format

---
