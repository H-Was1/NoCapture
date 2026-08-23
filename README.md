<p align="center">
  <img
    src="https://nocapture.membran.digital/logo.png"
    width="100"
    alt="NoCapture screen capture protection logo"
  >
</p>

<h1 align="center">NoCapture: Screen Capture Protection for Private Windows</h1>

<p align="center">
  Protect selected windows from screen sharing, screen recording, and desktop capture
  while keeping them visible and interactive on your computer.
</p>

<p align="center">
  <a href="https://nocapture.membran.digital">Website</a> •
  <a href="https://nocapture.membran.digital/dashboard">Download</a> •
  <a href="https://nocapture.membran.digital/use-cases/meetings">Meeting privacy</a> •
  <a href="https://github.com/H-Was1/NoCapture/issues">Report an issue</a>
</p>

<p align="center">
  <a href="https://github.com/H-Was1/NoCapture/stargazers">
    <img src="https://img.shields.io/github/stars/H-Was1/NoCapture?style=flat-square" alt="GitHub stars">
  </a>
  <a href="https://github.com/H-Was1/NoCapture/network/members">
    <img src="https://img.shields.io/github/forks/H-Was1/NoCapture?style=flat-square" alt="GitHub forks">
  </a>
  <a href="https://github.com/H-Was1/NoCapture/issues">
    <img src="https://img.shields.io/github/issues/H-Was1/NoCapture?style=flat-square" alt="GitHub issues">
  </a>
  <a href="https://github.com/H-Was1/NoCapture/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/H-Was1/NoCapture?style=flat-square" alt="License">
  </a>
</p>

> NoCapture is a desktop privacy tool for protecting sensitive windows during
> Zoom, Microsoft Teams, Google Meet, Discord, OBS, and other screen-sharing workflows.

## Why NoCapture?

Screen sharing can expose terminals, password managers, private messages, financial information,
and confidential documents.

Minimizing a window or moving it to another monitor does not always protect it from accidental
capture. NoCapture applies operating-system-level window capture protection so a selected window
remains visible and usable locally while being excluded from supported capture paths.

## See How It Works

<div align="center">

https://github.com/user-attachments/assets/5136c722-0ca3-4845-87af-586021d28e96

</div>


NoCapture hides selected windows from supported screen capture, recording, and screen-sharing
workflows while keeping them visible to you.

It supports automatic protection rules, live preview of shared content, and per-window control
across supported Windows, macOS, and Linux environments.

## Key Features

- Protect or unprotect individual application windows.
- Keep protected windows visible and interactive locally.
- Hide selected windows from supported screen capture and recording paths.
- Preview the frame visible to a screen-sharing or recording workflow.
- Hide protected windows from taskbar thumbnails and window switchers where supported.
- Automatically re-apply protection when a protected window loses focus.
- Configure calendar-, application-, time-, and focus-based routines.
- Use customizable global hotkeys.
- Apply different protection rules across multiple displays.
- Use native operating-system APIs without kernel drivers or browser extensions.

## Quick Start

1. Download NoCapture from the [official download page](https://nocapture.membran.digital/dashboard).
2. Launch the application.
3. Expand an application to view its open windows.
4. Select a window and click **Protect**.
5. Open **Live Preview** to verify what will be visible during screen sharing.
6. Start your meeting, presentation, or recording.

Protection behavior depends on the operating system, graphics stack, permissions, and capture method.
Test your intended workflow before relying on NoCapture for sensitive information.

## Window-Level Screen Capture Protection

NoCapture groups open windows by application. Expand an application, select a window, and
click **Protect**.

The window remains available to you locally while protection is active. You can continue to
type, click, resize, and work normally.

### Protect and Unprotect

The primary toggle controls whether a selected window is protected from supported capture paths.

Click **Unprotect** to make the window visible to the capture workflow again.

### Skip Taskbar

Where supported, remove a protected window from taskbar thumbnails and window switchers.

### Pin to Top

Keep a protected window above other local windows. This is useful for private notes, reference
documents, or chat that you need to see while presenting.

### Focus Protection

Automatically re-apply protection when a protected window loses focus.

This helps reduce the risk of accidental exposure while switching between applications during a
meeting or presentation.

## Live Preview

Live Preview shows the frame that a supported screen-sharing or recording workflow can receive.

Before sharing your screen in Zoom, Microsoft Teams, Google Meet, OBS, or another application,
use Live Preview to verify that protected windows are excluded from the output.

Always test the exact application, operating system, display, and capture mode you plan to use.

[Read why Live Preview matters](https://nocapture.membran.digital/blog/the-best-app-hider-for-screen-sharing)

## Automation and Preferences

NoCapture can automate repetitive privacy tasks so you do not have to manually protect windows
before every call.

### Smart Routines

Create rules that automatically protect selected windows:

- **Calendar-based:** Protect applications before a scheduled meeting.
- **Application-based:** Protect a window when a selected application launches.
- **Time-based:** Apply protection during specified work hours.
- **Focus-based:** Re-apply protection when a protected window loses focus.

### Global Hotkeys

Use `Ctrl+Alt+N` to toggle protection for the active window.

Hotkeys can be customized in Preferences for actions such as protect, unprotect, pin, and preview.

### Personalization

- Match your system theme or use dark mode.
- Launch NoCapture with the operating system.
- Start minimized or open the control panel.
- Configure notification handling.
- Apply different rules to different displays.

## How NoCapture Works

When you click **Protect**, NoCapture asks the operating system to exclude the selected window
from supported capture output.

- **Local view:** The window remains visible, interactive, and usable.
- **Capture output:** The window is omitted from supported screen-sharing or recording output.
- **Workflow:** You can continue working without minimizing or closing the window.

NoCapture is designed for supported operating-system capture paths. Results may vary depending on
the operating system, application, graphics stack, permissions, capture API, and compositor.

## Supported Capture Workflows

NoCapture is designed to help protect windows during workflows involving:

- Zoom
- Microsoft Teams
- Google Meet
- Discord
- Webex
- OBS
- Streamlabs
- XSplit
- NVIDIA ShadowPlay
- Native screenshot and recording tools
- Desktop applications that capture frames through supported operating-system APIs

No software can prevent someone from photographing your physical display with a separate camera.
Always verify protection with the exact software and configuration you intend to use.

## AI Screen Capture

Desktop AI assistants and automation tools may use screenshots or desktop-capture APIs to interpret
what is visible on your screen.

NoCapture applies the same window-level protection to supported capture paths, helping reduce the
risk of exposing password managers, private messages, financial information, terminals, and
confidential documents.

Protection is not universal. Capture behavior can vary between tools, operating systems, graphics
drivers, permissions, and API implementations.

[Read about AI screen-capture risks](https://nocapture.membran.digital/blog/screen-capture-apis-desktop-extraction-crisis)

## Privacy Use Cases

### Remote Workers and Consultants

Protect client documents, internal chats, research, and terminals while presenting or collaborating
with customers.

### Streamers and Creators

Keep private chats, password managers, production tools, and stream controls out of broadcasts
while keeping them visible locally.

### Developers

Protect terminals, API keys, database consoles, deployment tools, and `.env` files during pair
programming, support sessions, and technical demonstrations.

### Healthcare and Legal Workflows

Reduce accidental exposure of sensitive records, client information, and private documents during
remote meetings.

NoCapture is a technical privacy tool and does not by itself guarantee compliance with HIPAA,
attorney-client privilege, GDPR, or any other legal or regulatory requirement.

### AI Agent Users

Reduce the amount of desktop content exposed to applications that use supported screen-capture
methods to interpret your computer screen.

[Read the AI meeting privacy guide](https://nocapture.membran.digital/blog/ai-meeting-scrapers-window-titles)

## Architecture

NoCapture uses native operating-system APIs and does not require kernel drivers, browser
extensions, or screen-capture hooks.

| Platform | Technology | Status |
|---|---|---|
| Windows | `SetWindowDisplayAffinity` and `WDA_EXCLUDEFROMCAPTURE` | Supported |
| macOS | Core Graphics window-sharing controls | Verify per release |
| Linux/X11 | X11 and compositor APIs | Verify per release |
| Linux/Wayland | Compositor-dependent protocols | Verify per compositor |

Performance and compatibility can vary by operating system, compositor, graphics driver, display
configuration, and capture application.

## Platform Support

Check the [official download page](https://nocapture.membran.digital/dashboard) for current builds,
system requirements, and supported versions.

If a capture workflow does not behave as expected, please [open an issue](https://github.com/H-Was1/NoCapture/issues)
with the following information:

- Operating system and version.
- NoCapture version.
- Capture application and capture mode.
- Number of displays and display configuration.
- Graphics hardware and driver version.
- Steps to reproduce the problem.

Please do not include passwords, API keys, private messages, customer information, or other
sensitive content in issue reports.

## Frequently Asked Questions

### Does NoCapture minimize or close protected windows?

No. A protected window remains visible and interactive locally while protection is active.

### Does NoCapture protect an entire monitor?

NoCapture is primarily designed for window-level protection. Monitor-level behavior depends on the
operating system and capture application.

### Can NoCapture prevent someone from photographing my screen?

No. A separate camera can photograph a physical display, and NoCapture cannot prevent that.

### Does NoCapture work with every screen recorder?

Yes, NoCapture is designed to protect selected windows from screen recorders,
screen-sharing applications, and other supported operating-system capture paths.

However, compatibility may vary depending on the recorder, operating system,
graphics driver, permissions, and display configuration. Always test your exact
setup before using NoCapture with sensitive information.

### Can I protect a password manager or terminal?

Yes, provided the application and capture workflow support the operating-system protection method
used by NoCapture. Verify the result with Live Preview before sharing.

## Why I Built This

I leaked AWS credentials during a client Zoom call. Twice.

The first time, a terminal was minimized behind the browser. I had cleaned my desktop before the
call but forgot that the terminal was still open. Someone saw the access key, and we spent
48 hours rotating credentials.

The second time, I moved Slack to another monitor and assumed it was safe. I switched to display
capture for a few seconds to show a PDF, and private Slack messages appeared in the meeting.

Minimizing is not protection. Moving a window to another monitor is not always protection. Closing
everything also breaks the workflow.

So I learned the relevant operating-system compositor APIs and built the toggle I needed.

[Read the full story](https://nocapture.membran.digital/blog/why-just-close-your-tabs-is-terrible-advice)

## Resources

- [Official NoCapture website](https://nocapture.membran.digital)
- [Download NoCapture](https://nocapture.membran.digital/dashboard)
- [Meeting privacy use cases](https://nocapture.membran.digital/use-cases/meetings)
- [Why “Just Close Your Tabs” Is Terrible Advice](https://nocapture.membran.digital/blog/why-just-close-your-tabs-is-terrible-advice)
- [The Best App Hider for Screen Sharing](https://nocapture.membran.digital/blog/the-best-app-hider-for-screen-sharing)
- [Hide Apps Without Breaking Workflow](https://nocapture.membran.digital/blog/hide-apps-in-screen-share-without-workflow-breaks)
- [Screen Capture APIs and Desktop Extraction](https://nocapture.membran.digital/blog/screen-capture-apis-desktop-extraction-crisis)
- [AI Meeting Scrapers and Window Title Harvesting](https://nocapture.membran.digital/blog/ai-meeting-scrapers-window-titles)
- [NoCapture changelog](https://nocapture.membran.digital/changelog)

## Contributing

Contributions are welcome, especially for:

- macOS and Linux compatibility.
- New capture-workflow tests.
- Accessibility improvements.
- Translations.
- Documentation.
- Bug reports and reproducible test cases.

Before contributing:

1. Read the repository guidelines.
2. Open an issue for substantial changes.
3. Do not submit private data, credentials, or confidential screenshots.
4. Include operating-system and capture-application details when reporting bugs.

## Security

Do not use GitHub issues to report security vulnerabilities.

For security reports, contact:

[contact@membran.digital](mailto:contact@membran.digital)

Please avoid including credentials, private messages, customer data, or other sensitive information
in public reports.

## License

This project is licensed under the terms described in the [LICENSE](LICENSE) file.

---

<p align="center">
  Built with obsession, not surveillance.
</p>

<p align="center">
  <a href="https://membran.digital">Membran.digital</a> •
  <a href="mailto:contact@membran.digital">contact@membran.digital</a>
</p>
