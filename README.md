<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/images/huglab-logo-dark.png">
  <img src="docs/images/huglab-logo-light.png" alt="huglab" width="240">
</picture>

# TrickShot

**Screenshots for IT and developer work: capture, explain, and share them without leaking secrets.**

[**⬇ Download the latest version**](https://github.com/huglab-dev/TrickShot-app/releases/latest)

macOS 14 or later · Apple Silicon and Intel · Free

<br>

<img src="docs/images/hero-editor.png" alt="The TrickShot editor with a web console screenshot annotated with numbered steps, a highlighted value, a label and a curved arrow" width="880">

</div>

<br>

## Why TrickShot

- **Made for technical screenshots.** Terminals, admin consoles and settings pages, explained with steps, arrows and labels in a few clicks.
- **Secrets get blurred for you.** Smart redact reads the screenshot and hides passwords, keys, tokens and personal data before you share it.
- **Everything stays on your Mac.** No account, no analytics, no uploads. Text recognition runs on-device.

## Capture

TrickShot lives in the menu bar. Each capture opens in its own editor window, so several screenshots can be open at once.

| Shortcut | Action |
|:---:|---|
| <kbd>⌥</kbd> <kbd>⇧</kbd> <kbd>1</kbd> | **Capture Area.** The screen freezes while you select, so menus and tooltips stay in the picture. |
| <kbd>⌥</kbd> <kbd>⇧</kbd> <kbd>2</kbd> | **Capture Window.** One window with clean edges, even when others cover it. |
| <kbd>⌥</kbd> <kbd>⇧</kbd> <kbd>3</kbd> | **Capture Full Screen.** The display under the pointer. |
| <kbd>⌥</kbd> <kbd>⇧</kbd> <kbd>4</kbd> | **Copy Text.** Reads the text in an area and puts it on the clipboard. |
| <kbd>⌥</kbd> <kbd>⇧</kbd> <kbd>5</kbd> | **Capture Scrolling Area.** Keeps capturing while you scroll and stitches it into one tall picture. |

All shortcuts can be changed in Settings. While you select an area, a loupe shows the pixel position and color, the arrow keys move one pixel at a time, <kbd>C</kbd> copies the color as hex, and <kbd>Space</kbd> switches to window mode.

You can also open your own pictures: from Finder, with **Open Image…** in the menu, or with **New from Clipboard**.

## Annotate

<p align="center">
  <img src="docs/images/toolbar.png" alt="The TrickShot editor toolbar: copy, save, pin, rounded corners, the drawing tools, Smart redact, color, and the color, size and zoom readout" width="880">
</p>

Every tool has a one-key shortcut. Shapes stay movable and editable, and every change can be undone.

| Key | Tool | Key | Tool |
|:---:|---|:---:|---|
| <kbd>V</kbd> | Select | <kbd>T</kbd> | Text, in a box or plain |
| <kbd>A</kbd> | Arrow, straight or curved | <kbd>N</kbd> | Step number |
| <kbd>L</kbd> | Line | <kbd>B</kbd> | Blur, soft or pixelated |
| <kbd>R</kbd> | Box, outline or filled | <kbd>S</kbd> | Spotlight |
| <kbd>O</kbd> | Ellipse | <kbd>M</kbd> | Magnifier |
| <kbd>P</kbd> | Pen | <kbd>C</kbd> | Crop |
| <kbd>H</kbd> | Highlighter | <kbd>K</kbd> | Cut out strip |
| | | <kbd>E</kbd> | Extract text |

Tools you rarely use can be hidden under the wrench and brought back with **Customize Toolbar**. **Cut out strip** removes a band from the middle of a long log and joins the rest. **Pin to screen** keeps a screenshot floating above your other windows while you work.

## Smart redact

<p align="center">
  <img src="docs/images/smart-redact.png" alt="A terminal screenshot before and after Smart redact: the IP address, the database connection string, the access key, the token and the bearer token are blurred" width="880">
</p>

Click the eye in the toolbar. TrickShot reads the text in the screenshot and blurs everything the active profile is set to find. Check the result, then remove a box or add your own.

- **Secrets:** passwords and private keys, including the password in connection strings such as `postgres://user:password@host`; API keys and tokens (AWS, GitHub, Slack, OpenAI, JWTs, long hex and base64 strings); IP and MAC addresses; links and domain names.
- **Personal and company data:** e-mail addresses, phone numbers, street addresses, Swedish personnummer and organisationsnummer, card numbers, IBAN, bankgiro and plusgiro.
- **Your own lists:** words and regular expressions, such as customer names or ticket numbers.

<p align="center">
  <img src="docs/images/redact-settings.png" alt="TrickShot Settings, Redact tab: the IT-Default profile with passwords and API keys switched on" width="560">
</p>

Profiles keep different combinations, for example one for internal IT work and one for sharing outside the company. Right-click the eye to switch. Blur is burned into the exported file, so the person who gets it cannot undo it.

## Save and share

- <kbd>⌘</kbd> <kbd>C</kbd> copies the finished picture, and <kbd>⌘</kbd> <kbd>S</kbd> saves it as a PNG.
- Pick a tag when you save and it becomes the start of the file name, for example `acme_2026-11-09_22-01-33.png`. A script that sorts files can then route each screenshot to the right folder.
- Recent screenshots stay editable from the menu, annotations included, for as long as your retention setting keeps them.

## Install

1. Download **TrickShot-x.y.z.dmg** from [Releases](https://github.com/huglab-dev/TrickShot-app/releases/latest), open it and drag **TrickShot** to **Applications**.
2. Open TrickShot. macOS blocks it the first time, because the app is signed with a self-signed certificate and is not notarized by Apple. Close the warning.
3. Open **System Settings → Privacy & Security**, scroll to **Security** and choose **Open Anyway** next to TrickShot.
4. When TrickShot asks for **Screen & System Audio Recording**, allow it in System Settings. Then quit TrickShot and open it again.

Each release has a `.sha256` file next to the DMG. To check your download:

```bash
shasum -a 256 -c TrickShot-x.y.z.dmg.sha256
```

## Updates

When a new version is out, **Update Available** appears at the top of the TrickShot menu, and **Settings → About** shows it too. Both open the release page here. TrickShot never downloads or installs anything by itself, and each new version needs the **Open Anyway** approval again.

## Privacy

TrickShot has no account and no analytics, and your screenshots are never uploaded. Text recognition uses Apple's on-device Vision framework. Recent screenshots are kept in `~/Library/Application Support/TrickShot` for the period you choose in Settings, and you can turn that off.

The only network request is the update check. At most once a day, when TrickShot starts or its menu opens, it asks GitHub for the latest release on this page and reads only the version number and the link. Turn it off under **Settings → About**; the **Check Now** button there still works.

TrickShot needs the **Screen Recording** permission to take screenshots. It does not record video or audio.

---

<div align="center">

TrickShot is made by Hugo Bjurström at [huglab](https://github.com/huglab-dev). It is free to download; the source code is not public.<br>
TrickShot is an independent project and is not affiliated with or endorsed by Apple.

</div>
