<p align="center">
  <img src="https://nocapture.membran.digital/logo.png" width="100" alt="NoCapture">
</p>

<h1 align="center">NoCapture</h1>
<p align="center">
  <b>Your screen. Two realities.</b><br>
  Hide any window from screen capture, AI agents, and screen sharing — at the OS level.
</p>

<p align="center">
  <a href="https://nocapture.membran.digital">Website</a> •
  <a href="https://nocapture.membran.digital/blog">Blog</a> •
  <a href="https://nocapture.membran.digital/use-cases/meetings">Use Cases</a> •
  <a href="https://nocapture.membran.digital/dashboard">Download</a>
</p>

---

## 🎬 See It In Action

https://github.com/H-Was1/NoCapture/blob/main/Recording%202026-08-09%20235805.mp4

NoCapture groups your open windows by application. Expand an app, pick a window, hit **Protect**. It stays visible to you. Vanishes from Zoom, Teams, OBS, and every AI agent screenshotting your screen. Toggle back anytime — or automate it entirely.

---

## The Actual UI

NoCapture isn't a system tray utility you forget about. It's a control panel for your screen.

### Apps & Windows — Grouped, Collapsible, Instant

Every running app appears as a collapsible group. Expand it, see its windows, control each one individually.

| Button | What It Does |
|--------|-------------|
| **🛡️ Protect / Unprotect** | The main toggle. Protects the window at the OS compositor level — invisible to screen capture, recording, and AI screenshot agents. Unprotect brings it back to the stream instantly. |
| **👁️ Skip Taskbar** | Remove the window from taskbar thumbnails and Alt+Tab switchers. Even if someone checks your taskbar during a share, the protected app is gone from enumeration. |
| **📌 Pin to Top** | Keep the window floating above everything else locally. Great for reference docs, notes, or private chat you need visible while presenting. |
| **💨 Focus Lost Windows** | Detects when a protected window loses focus and auto-re-applies protection. Prevents accidental exposure when you click around during a call. |

No more hunting through window lists. No more "did I minimize that?" Your entire workspace is one panel away.

### Live Preview — See What They See

Before you hit "Share Screen" in Zoom, open the **Live Preview**. It shows the exact frame that Zoom, Teams, or OBS will broadcast — not a mockup, the actual compositor output.

If you can see a protected window in the preview, something's wrong. But you won't. Because protected windows are omitted at the source.

[→ Why Live Preview matters](https://nocapture.membran.digital/blog/the-best-app-hider-for-screen-sharing)

---

## Preferences — Automate The Boring Stuff

NoCapture handles the manual work so you don't have to think before every call.

### Smart Routines

Set rules once. They run forever.

- **Calendar-based:** Auto-protect Slack, 1Password, and your terminal 5 minutes before any Zoom meeting.
- **App-launch based:** The moment your banking app opens, it cloaks automatically.
- **Time-based:** Protect sensitive windows during work hours, unprotect after.
- **Focus-based:** Re-apply protection when a protected window loses focus.

You set the logic. NoCapture enforces it. Zero clicks during the actual call.

### Global Hotkeys

`Ctrl+Alt+N` toggles protection on the active window. No mouse hunting while you're live. Fully customizable in Preferences — set your own combos for protect, unprotect, pin, and preview.

### Personalization

- **Theme:** Match your system or run dark mode.
- **Startup behavior:** Launch with Windows, start minimized, or open the panel.
- **Notification handling:** Choose how aggressive the notification shield is — block all, block sensitive apps only, or hold-and-release after the call.
- **Multi-monitor:** Per-display rules. Protect windows on monitor 2 while sharing monitor 1.

---

## What "Protect" Actually Means

When you hit **Protect**, NoCapture tells the OS compositor to omit that window from the capture stream.

- **Local view:** The window stays fully visible, interactive, and usable. You can type in it, click it, resize it.
- **Capture output:** The window is completely absent. Not blacked out. Not blurred. Not pixelated. The pixels are never generated in the frame buffer.

This works against:
- Zoom, Teams, Google Meet, Discord, WebEx
- OBS, Streamlabs, XSplit, NVIDIA ShadowPlay
- AI agents using Claude Desktop, Copilot Vision, and any tool screenshotting via DXGI/BitBlt/DWM
- Native screenshot tools, screen recorders, and frame buffer readers

[→ The technical deep dive](https://nocapture.membran.digital/blog/screen-capture-apis-desktop-extraction-crisis)

---

## Why I Built This

I leaked AWS credentials on a client Zoom call. Twice.

First time: terminal was minimized behind the browser. I "cleaned my desktop" before the call. Forgot the terminal existed. Someone saw the access key. We spent 48 hours rotating every credential.

Second time: moved Slack to monitor two. Sharing monitor one, so I figured I was safe. Switched to Display Capture for three seconds to show a PDF. My Slack DMs — including a confidential conversation — went live to everyone.

Minimizing is not protection. Moving to monitor two is not protection. "Just close your tabs" breaks your workflow.

So I learned Windows compositor APIs and built the toggle I actually needed.

[→ The full story](https://nocapture.membran.digital/blog/why-just-close-your-tabs-is-terrible-advice)

---

## The AI Agent Problem

Here's what changed since I built this.

Claude Desktop's "computer use" feature screenshots your display every 2–5 seconds and feeds it to a vision model. Microsoft's Copilot Vision does the same. Dozens of "productivity" agents claim to "use your computer like a human" — they don't use APIs. They hit the frame buffer and OCR everything.

Your password manager. Your Slack DMs. Your bank balance. Your terminal with production credentials. All in frame. All the time.

NoCapture blocks AI agent screenshots the same way it blocks Zoom. Same toggle. Same protection. Because the threat isn't just meetings anymore — it's 24/7 automated screen surveillance.

[→ AI agents are the new screenshot threat](https://nocapture.membran.digital/blog/screen-capture-apis-desktop-extraction-crisis)


---

## Use Cases

**Remote Workers & Consultants**
Protect client docs, internal Slack, and competitor research during screen shares. Auto-cloak based on your calendar.

**Streamers & Creators**
Hide OBS scenes, Discord DMs, and password managers from broadcast. Use Pin to Top for stream notes that stay local-only.

**Developers**
Keep terminals with API keys, database connections, and `.env` files invisible during pair programming. Smart Routines auto-cloak your terminal when Zoom launches.

**Healthcare & Legal**
Maintain HIPAA and attorney-client privilege. Cloak EHR systems and patient portals during telehealth. [→ Meeting privacy guide](https://nocapture.membran.digital/use-cases/meetings)

**AI Agent Users**
Run Claude Desktop, Copilot Vision, or screenshot-hungry agents without exposing your entire digital life. [→ AI agent privacy](https://nocapture.membran.digital/blog/ai-meeting-scrapers-window-titles)

---

## Architecture

NoCapture uses native OS APIs — no hooks, no drivers, no kernel modules.

- **Windows:** `SetWindowDisplayAffinity` with `WDA_EXCLUDEFROMCAPTURE`. DWM compositor-level exclusion.
- **macOS:** `kCGWindowSharingNone`, `CGWindowListCreateImage` filtering.
- **Linux:** X11 `XComposite` / Wayland `zwlr_screencopy_manager_v1`.

<1% CPU. <20 MB RAM. Native APIs only.

---

## Resources

- [Why "Just Close Your Tabs" Is Terrible Advice](https://nocapture.membran.digital/blog/why-just-close-your-tabs-is-terrible-advice)
- [The Best App Hider for Screen Sharing](https://nocapture.membran.digital/blog/the-best-app-hider-for-screen-sharing)
- [Hide Apps Without Breaking Workflow](https://nocapture.membran.digital/blog/hide-apps-in-screen-share-without-workflow-breaks)
- [Screen Capture APIs & Desktop Extraction Crisis](https://nocapture.membran.digital/blog/screen-capture-apis-desktop-extraction-crisis)
- [AI Meeting Scrapers & Window Title Harvesting](https://nocapture.membran.digital/blog/ai-meeting-scrapers-window-titles)

---

## Contributing

Solo-built, but open to contributions — especially macOS/Linux parity, translations, and bug reports.

See [Contact Page](https://nocapture.membran.digital/company/contact).

---

<p align="center">
  Built with obsession, not surveillance.<br>
  <a href="https://www.producthunt.com/products/nocapture?embed=true&amp;utm_source=badge-featured&amp;utm_medium=badge&amp;utm_campaign=badge-nocapture" target="_blank" rel="noopener noreferrer"><img alt="NoCapture - AI privacy and app hiding for screen sharing | Product Hunt" width="250" height="54" src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=1228484&amp;theme=light&amp;t=1787317648553"></a><br>
  <a href="https://membran.digital">Membran.digital</a> •
  <a href="mailto:contact@membran.digital">contact@membran.digital</a>
</p>
