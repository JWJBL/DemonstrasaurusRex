# Privacy Policy — Demonstrasaurus Rex

**Effective date:** May 14, 2026
**Last updated:** May 14, 2026

## In one sentence

Demonstrasaurus Rex collects no data, transmits no data, and contains no
remote code. Everything stays on your device.

## What the extension does

Demonstrasaurus Rex is a Chrome extension that lets you build interactive
click-through walkthroughs of any website. You explicitly start a recording
on a chosen tab, manually capture each step as a screenshot, edit the
result, and export the whole walkthrough as a single self-contained HTML
file. All processing happens on your computer.

## What data the extension handles

While, and only while, you have explicitly started a recording session,
the extension stores the following in your browser's local IndexedDB
(under the extension's own origin, `chrome-extension://<extension-id>/`):

- **Screenshots** of the recorded tab's visible viewport, captured when
  you press 📸 Capture Step or the Alt+Shift+S keyboard shortcut.
- **The URL of the recorded page**, so the editor can show you which
  page each step came from.
- **Text you typed into input fields on the recorded page**, so the
  editor can auto-suggest a caption like *Type "hello@example.com" into
  Email*. Exception: text typed into password fields (`<input
  type="password">`) is never captured. Password-field interactions are
  recorded only as a generic caption like *Enter password into Password*.
- **Click coordinates and metadata about the element you clicked**
  (tag name, accessible label, CSS selector), so a hotspot can be placed
  at that location in the editor.

None of this data is transmitted anywhere. It exists only on the device
where you recorded it.

## What the extension does NOT do

- **No network transmission.** The extension never sends any user data,
  screenshots, URLs, click data, or telemetry to any server. There are
  no `fetch`, `XMLHttpRequest`, WebSocket, or any other outgoing
  network calls to any third party.
- **No analytics.** No Google Analytics, Mixpanel, Amplitude, Segment,
  or any other tracking SDK.
- **No advertising.** No ad networks, no tracking pixels.
- **No accounts.** No sign-up, no log-in, no email collection.
- **No sync.** Walkthroughs are not synced between browsers or devices.
  Data exists only in the browser where it was recorded.
- **No background activity.** The recorder script runs only on a tab
  where you have explicitly started a recording; it stops when you stop
  the recording or close the tab.
- **No remote code execution.** The extension loads no scripts from any
  external server. The exported HTML viewer is generated from a bundled
  local template and is itself self-contained.

## Where data lives

All recorded walkthroughs and their screenshots live in your browser's
local IndexedDB. They are scoped to the extension and are inaccessible
to other websites or extensions. They persist across browser restarts
until you delete them.

## Your controls

- **Delete a single walkthrough.** Open the extension popup; click
  **Delete** next to the walkthrough in the list.
- **Delete every walkthrough.** Open the extension popup; click
  **Delete all data** in the footer. This permanently removes every
  saved walkthrough and screenshot.
- **Uninstall the extension.** Removing Demonstrasaurus Rex from
  `chrome://extensions` clears the extension's IndexedDB data per
  Chrome's normal uninstall behavior.

## Exported walkthrough files

When you press **Export HTML**, the extension produces a self-contained
.html file on your computer that includes your screenshots and captions
as inline data. The file has no network dependencies — recipients can
open it offline.

Once you share an exported file (by email, chat, file share, upload to
your own server, etc.), what happens to it is outside the scope of this
extension and this policy.

## Permissions and why we ask for them

| Permission | Why |
|---|---|
| `activeTab` | To inject the recorder and capture screenshots on the tab you choose to record. |
| `scripting` | To inject the recorder content script into the recorded tab. |
| `storage` | To use `chrome.storage.session` to remember the active recording's ID across service-worker restarts. Nothing is synced. |
| `tabs` | To look up the active tab's ID and URL when you start a recording, to capture screenshots, to open the editor, and to clean up if you close the recorded tab. |
| `downloads` | To save the exported HTML file to your computer. |
| `webNavigation` | To detect when the recorded tab navigates, so the recorder can be re-injected on the new page. |
| `host_permissions: <all_urls>` | So that capture and injection can work on any site you choose to record. The extension never reads page content or runs on a tab unless you have explicitly started a recording on that tab. |

None of these permissions are used to transmit any data.

## Children's privacy

Because the extension collects no data of any kind, it does not
knowingly collect data from children under 13 — or anyone else. It is
suitable for users of any age, subject to ordinary Chrome Web Store
age requirements.

## Changes to this policy

If material changes are made, the **Last updated** date at the top of
this page will change and the new policy will be posted at the same URL.
For non-material changes (typos, clarifications), the policy will be
silently updated.

## Contact

If you have questions about this policy or the extension's data
practices, contact: **john-wheaton@hotmail.com**.
