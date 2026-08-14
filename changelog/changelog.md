# 0.18.0

- **Streamlined App Drawer Context Menu**: Reorganized the long-press menu on drawer apps into clear grouped sections separated by dividers for faster scanning and easier navigation.
- **App Shortcuts in Drawer**: Quickly launch static and dynamic app shortcuts with the new "App Menu" option in the context menu.
- **Direct Uninstall**: Easily uninstall apps directly from their context menu in the app drawer.
- **Unified "Add to…" Dialog**: Simplified placing apps onto Home Spaces, Virtual Spaces, Classic Docks, Pie Menus, or Home Gestures via a single, unified placement screen.
---

# 0.17.0

- **Expandable Notification Conversations**: Tap notifications to expand and view full messaging conversation history (grouped cleanly by sender with timestamps) and multi-line inbox summaries directly from the dock, notification dialog, or inbox.
- **Dismiss All App Notifications**: Quickly clear all notifications for a specific app with a new "Dismiss all" action in notification menus and dock popups.
- **Capsule Vertical Alignment & Line Height**: Enhanced Tenkai Capsule customization with options to align text vertically (Top, Center, Bottom) and fine-tune line spacing multiplier.
- **Notification Deduplication Fix**: Resolved an issue where separate notifications with different subtext could be incorrectly merged together.
---

# 0.16.0

- **Custom Image Icon Picker**: Select custom photos from your device gallery to use as icons for pie slices and capsules.
- **Photo Rotation & Optimization**: Camera photos now automatically respect EXIF orientation (staying upright) and downsample high-resolution images to conserve device RAM.
- **Improved Icon Gallery**: Picked images are saved to local app storage with full management and deletion options available inside the icon picker.
- **Work Profile Shortcut Cleanup**: Unused pinned shortcuts are now properly audited and cleaned up across both primary and Work Profiles.
- **Stability & Performance Improvements**:
  - Smoother icon pack switching with automatic pruning of obsolete cached icons.
  - Better contact avatar memory management in notification listening.
  - Fixes for raw JSON text rendering in capsules when jsonPath fails or is empty.
  - Properly unescapes Unicode sequences (`\uXXXX`) in resolved Google News publisher links.
---

# 0.15.0

- **Advanced Tenkai Capsule Syntax & Formulas**:
  - Enhance Tenkai Capsules with custom formula syntax supporting conditionals (`{if ...}`), fallback values (`{token || fallback}`), and text transformation functions (`UPPER`, `LOWER`, `TRUNCATE`, etc.).
  - Access an in-app interactive syntax guide and reference documentation directly from the Capsule settings.
- **Classic Dock Pie Actions**:
  - Assign Pie actions to items on Classic Docks to seamlessly trigger radial menus and gestures from dock shortcuts.
---

# 0.14.0

- **Inbox Trash & Soft-Delete**:
  - Delete notes and catch-up items into a Trash list with options to restore or permanently delete items.
  - Repositioned trash action buttons for cleaner clearance from gesture and navigation bars.
- **Notes Search Box**:
  - Real-time search in the Notes tab, prioritizing title matches first followed by description text.
- **Inbox Item Reordering & Gestures**:
  - Drag-and-drop reordering and improved gesture handling for notes and catch-up entries.
- **Catch-Up Widget Customization**:
  - Customizable entry spacing/margin and padding options in the Catch-Up widget configuration screen.
- **Work Profile Support in Recent Apps**:
  - Recent app listings now properly distinguish between main profile and work profile app instances.
- **Control Dock Enhancements**:
  - Refined default dock padding, button visibility in collapsed states, and updated settings labels.
---

# 0.13.0

- **HTTP Actions & Reusable Queries**:
  - Configure reusable HTTP request templates (GET, POST, PUT, DELETE) with headers, payloads, and custom response handling.
  - Trigger HTTP queries directly from Pie Actions or Widget Automations.
  - New dark-themed Toast Overlay with visual click animations, pulse feedback, and haptic feedback.
- **Unified Control Dock Enhancements**:
  - Dedicated Control Dock settings screen with customizable display modes and behavior.
  - Configurable auto-collapse timers with pause-on-touch interaction.
  - Badge indicator showing pending Inbox catch-up items with an option to keep the Inbox icon visible when items are pending.
  - Refined tap interactions to prevent accidental dock collapses when unhidden.
- **Classic Dock Enhancements**:
  - Filter "Recently used apps" by recency (5 minutes to 7 days, or show all).
  - Improved dock settings screen with live previews and quick configuration shortcuts.
- **Tenkai Capsule & Automation Upgrades**:
  - Added text rotation options (0°, 90°, 180°, 270°) for Tenkai Capsules.
  - Added new system tokens for alarms, bedtime, playback/media status, network modes, and orientation.
- **UI & Layout Fixes**:
  - Fixed text overflow and vertical clipping in Quick Settings on smaller screens.
---

# 0.12.0

- **Widget Position Control System**:
  - Added a dedicated Position Control bar in edit mode featuring directional pixel-nudge arrows, screen edge alignment controls (top, bottom, left, right), Z-order layer depth cycling, and a transparency adjustment slider.
  - Tap on widgets in edit mode to cycle layer depth (bring to front / send to back) without interrupting drag-to-move or resize gestures.
- **Categorized Widget Picker Dialog**:
  - Reorganized the "Add Widget" picker into two collapsible sections: "Tenkai Widgets" and "Third Party Widgets" with search filtering.
- **Catch-Up Widget & Notification Improvements**:
  - Resolved an issue in the Catch-Up widget where notification items briefly displayed artwork/avatars before reverting to generic app icons.
  - Updated single notification popups so action buttons remain visible even with large notification content bodies.
- **Gesture Precision & Dock Defaults**:
  - Fixed contextual menu long-press logic so sliding off a slice or action icon cancels the menu timer instead of triggering unexpectedly.
  - Set default notification tap action for "User Selected", "Recently Used", and "Frequently Used" classic docks to standard app launch.
- **Settings UI Enhancements**:
  - Reorganized settings tab layout, adjusted margins, and reordered permission toggles.
---

# 0.11.0

- **Redesigned App Contextual Menus**:
  - **Pie & List Menu Modes**: Render contextual options either as a full gesture-based radial pie menu or as a drag-and-release list (tap list for dock icons).
  - **Per-Element Customization**: Individual pie slices, action icons, and classic dock items can each customize their own contextual menu behavior.
  - **Custom Pie Group Bindings**: Select specific pie groups to generate custom contextual entries upon long-pressing an item.
  - **Reorganized Settings**: Contextual menu options consolidated in the General tab of Launcher Settings.
- **Android App Shortcuts & System Pinning**:
  - Support for Static, Dynamic, and Pinned Android App Shortcuts across launcher elements.
  - Capture system pin requests (`requestPinAppWidget` & pin shortcut intents) with interactive target placement into primary or virtual spaces.
  - Dedicated Pinned Shortcuts management UI in Launcher Settings with dynamic lifecycle tracking and cleanup.
- **Enhanced Contact Avatars for Phone Calls**:
  - Extract and display caller contact photos and avatars for call/phone notifications (`CATEGORY_CALL`, `CATEGORY_MISSED_CALL`, `CallStyle`, and `Person` extras).
  - Multi-tiered avatar resolution via LauncherApps shortcuts, Person extras, and contact dialer search (`ContactsContract.PhoneLookup`).
---

# 0.10.0

- **Unified Control Dock**:
  - Configurable display options: Always Visible, Auto-Hide on gesture, Hidden, and Collapsed dock modes.
  - Direct shortcut to dock settings from Edit Mode.
  - Resolved home screen gesture interception bugs when dock visibility changes.
- **Tenkai Catch-Up Widget & System**:
  - New integrated Catch-Up widget displaying date, time, news, inbox items, and personal notes/tasks.
  - Smart defaults for fresh installs with pre-configured news feeds and essential widgets.
  - Full widget area utilization and unconstrained horizontal page scrolling.
- **Share Sheet Integration (`ACTION_SEND`)**:
  - Share web links, articles, and text snippets from external applications directly into Tenkai Inbox and Catch-Up notes.
- **Launcher Quick Settings**:
  - Dedicated Quick Settings popup menu for fast access to launcher settings, Edit Mode, news/inbox, pie configuration, dock settings, and home gestures.
- **Notifications & UI Improvements**:
  - Per-conversation notification grouping and splitting options.
  - Interactive notification popups with quick action buttons and improved swipe-to-dismiss behavior.
- **Performance & Fixes**:
  - In-memory icon caching layer for faster pie menu and dock rendering.
  - Fixed gesture timing race condition when exiting widget edit mode.
---

# 0.9.2

- **Automatic Notification Rebind**: Launcher now automatically reconnects to Android's Notification Listener Service on resume, ensuring notification badges update reliably without requiring a device reboot or manual toggle.
- **Notifications & Badges Setting**: Added a dedicated Notifications & Badges section in General Settings with permission status and quick shortcut to system Notification Access.
- **Unified Notification Badges**: Red dot notification badges on Classic Dock icons now consistently respect the global Notification Badges setting.
- **Touch & Gesture Fixes**: Fixed an issue where static pie widgets could block touch input on bottom action icons, and resolved regressions affecting home screen gestures.
- **Layout Optimization**: Removed unnecessary bottom margins on the home screen layout.
---

# 0.9.1

- **News Feed Tabs & Filters:** Redesigned header controls with dedicated category tabs, source filter dropdowns, and quick status toggles.
- **Transparent Theme Enhancements:** Improved contrast, text readability, chip styling, and button visibility across Dark Transparent and Light Transparent themes.
- **Continuous Dock Swipe:** Fixed gesture handling when continuously sliding across spaces and docks.
- **Image Loading Reliability:** Card layout no longer flashes or reserves blank space for corrupted, broken, or 1x1 spacer images.
- **Work Profile Support:** Fixed icon caching so primary profile and Work Profile apps retain distinct icons.
- **Performance Optimizations:** Smoother A-Z index bar scrolling in the App Drawer and faster particle effect dismissal on touch release.
---

# 0.9.0

- **New News Feed space**: A dedicated, scrollable news page that sits just before Home. Reach it from the News button in the control dock, a two-finger swipe, or a "Switch to News" pie/dock action. Tapping a card opens the article (in your browser or a built-in reader) and dims it as read.
- **Free Google News**: Google News works for everyone at no cost. Choose your region and pick which topics (Top, World, and more) appear in your feed.
- **Your own feeds (premium — News Sources)**: Add any RSS or Atom feed. Or just paste a link and the app builds the feed for you — Reddit subreddits, YouTube channels, Mastodon accounts, GitHub repos/users, and Bluesky profiles are all recognized automatically.
- **FreshRSS sync (premium)**: Connect a self-hosted FreshRSS server to sync your feeds and read state, via either the Fever or Google Reader API.
- **Reading gestures & filters**: Swipe a card right to toggle read/unread, left to favorite. Long-press for share, copy link, mark read/unread, or mute a source. Filter the feed by source or by All / Unread / Read / Favorites, and mark everything read at once.
- **News themes**: Light, Dark, and two transparent variants (Light and Dark) that let your wallpaper show through, plus a "follow system" option. Dark stays the default.
- **Better notifications**: Notification entries now show the notification's title, source/app name, and app icon, and correctly distinguish work-profile apps. New per-dock setting controls what tapping an app with notifications does — smart (direct if one, menu if several), always direct, always show the list, or a standard app launch.
- **Notification list menu**: Tapping an app that has several notifications can now open a menu listing them, with an option to open the app's main screen.
- **Dynamic dock app filter**: Classic docks in Notifications, Recently Used, and Frequently Used modes now support a per-dock whitelist (show only chosen apps) or blacklist (hide chosen apps). User-defined docks are unaffected.
- **Smaller quality-of-life fixes**: Free tier now allows up to 5 action icons (was 3), two-finger gestures move between spaces by default, and pressing Back exits widget edit mode. Pies no longer trigger while scrolling the News feed, and the control dock's gray tap overlay was removed.
---

# 0.8.1

- **Diagnostics attachment fix**: "Email Developer" now sends the report as a proper attachment that reaches the developer reliably. The old flow could silently drop the attached log file on some email apps; the email chooser is also now limited to real email apps so the report can't be misrouted.
- **Display & device info in diagnostics**: Diagnostics reports now include a Display section (live vs. stable density, the launcher's capped density, font scale, screen dp, and resolution) so UI sizing complaints are easier to reproduce and debug.
- **Clearer share dialog**: The "Share Diagnostics" dialog now explains that the report includes your device info, app settings, and recent system logs, and reminds you to review the attached file before sharing.
---

# 0.8.0

- **New "Dark" pie theme**: A premium theme that unfolds a dark "void domain" from the center each time the pie opens (a Jujutsu-Kaisen-style domain expansion), then settles into a calm ambient state.
- **Reworked theme system**: All pie themes now share one consistent model, so themes, previews, and premium gating stay in sync. Includes a full dark theme pass across the app.
- **Smarter Back and Home buttons**: Pressing Home while a settings or nested screen is open now returns you straight to the home screen. On the home screen, Back steps back from a secondary space to your first space instead of leaking to the system.
- **Fixed reappearing theme customizations**: Switching pie themes now correctly clears your previous customizations — they no longer "come back on their own" after a config reload.
- **Scrollable, screen-adaptive menus**: The slice edit menus and icon selection menus now scroll and adapt to your screen, so nothing is cut off on smaller devices.
- **Tidier settings & drawer**: Settings tabs use smaller text with icons and wrap cleanly when they overflow; app drawer chips and premium/debug chips now shrink and overflow onto the next line instead of getting clipped.
- **Cleaner home pies**: Pies assigned to a home now show only the icon (no home text), and pie dots wrap across multiple lines when there are many.
---

# 0.7.1

- **App Shortcut Default Launcher Warning**: When adding or configuring an app shortcut, Tenkai Launcher now displays a helpful warning with a one-tap button to set Tenkai Launcher as your default launcher (required by Android to access app shortcuts).
- **Tabular Figures for Centered Capsules**: Clock and date capsules with centered text alignment now use monospaced tabular figures (`tnum`), keeping numeric digits visually centered and preventing text jumping as time changes.
- **Improved Clock Grid Alignment**: Clock capsule dimensions are now calculated using even grid cell steps, ensuring exact horizontal centering on the widget grid.
---

# 0.7.0

- **Home Gestures**: A new Home Gestures screen lets you bind actions to multi-finger swipes and pinches (two- and three-finger swipe up/down/left/right, pinch in, pinch out). Pinch-in defaults to opening launcher settings.
- **Pies everywhere**: Pies are no longer limited to the empty-home-space touch. Two new ways to launch one, anywhere on the home screen or inside a space:
  - **Action icons** — set a launcher icon's action to "Pie" and pressing it deploys that pie right where the icon sits.
  - **Static Pie widgets** — a pie that's always drawn on the space; touch it to start interacting.
  Each source picks its own Regular (press-and-drag to a slice) or Fixed (tap to open, tap to select) interaction mode.
- **Fixed Pie mode**: A new per-pie interaction style — tap to open the pie, it stays put, then tap a slice to select. Subpies open in the same spot. Choose between "Regular" (press-swipe-release) and "Fixed" (tap-to-open, tap-to-select) per pie, or turn on Fixed Pie globally in settings.
- **Shake to close**: Quickly wiggle back and forth between slices to dismiss the pie without launching anything.
- **App drawer default sort**: Pick which sort tab the drawer opens on by default. The A–Z bar on the right edge now switches to the Name tab when touched, and a hint helps you drag apps onto a space.
- **Next / Previous Space actions**: New pie/gesture actions to jump to the next or previous space.
- **Drag to create action icons**: Drag from the unified control dock to create an action icon or open the app drawer.
- **Consistent icons everywhere**: Icons now render the same way across pies, the drawer, the classic dock, capsules, action icons, and widgets.
- **Faster, more reliable icons**: App icons are now cached to disk, so they persist across app restarts and crashes and load faster, with automatic cache expiration to stay fresh.
- **Improved gesture/action editing**: A clearer premium-feature explanation dialog and refinements to the gesture preview and action edit screens.
---

# 0.6.2

- The **Default** pie theme now uses a lighter background (25% opacity instead of 50%), giving a cleaner, more see-through look over your wallpaper.
- Fixed garbled accented and non-Latin characters (mojibake) in Settings across 18 languages — e.g. Spanish "Círculos"/"configuración" and similar words now display correctly.
- Improved the Spanish translations.
- Updated the contact and diagnostics/bug-report email addresses shown in Settings.
---

# 0.6.1

- Minor changes
---

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
