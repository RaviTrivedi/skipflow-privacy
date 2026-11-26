# SkipFlow Privacy Policy

Last updated: November 27, 2026 · Applies to version 0.1.0

SkipFlow - Ad Skipper for YouTube automatically attempts to click eligible native Skip buttons on `https://www.youtube.com/*`. No account with SkipFlow is required.

## Information processed on your device

While Auto Skip Ads is enabled, SkipFlow examines YouTube's player, ad indicators, button text, visibility, enabled state, and page structure to find eligible Skip buttons. It reads the current YouTube page URL in memory to recognize navigation, and reads video playback state and progress to observe the outcome of an attempt. It does not build or store a browsing or viewing history. These operations take place in your browser; SkipFlow does not transmit this information to its developer or a backend.

## Saved preference

The only value the extension writes to persistent storage is `autoSkipEnabled`, a boolean in `chrome.storage.local`. It remembers your Auto Skip Ads toggle in your Chrome profile. A missing preference defaults to enabled. SkipFlow does not use Chrome sync storage or send this preference to a server. It remains locally until cleared or the extension is uninstalled. Turning Auto Skip Ads off saves a disabled preference rather than deleting it.

## Diagnostics

Production console diagnostics are disabled. If a developer explicitly enables the local diagnostic flag, SkipFlow logs initialization, click attempts, button identifiers, observation outcomes and errors in the browser console. It does not upload or persist these logs in extension storage. Developer Tools may retain output according to your settings; review any logs before sharing them.

## Network, sharing, and tracking

SkipFlow contains no analytics, tracking pixels, advertising SDKs, telemetry, or backend integration. Its scripts, font, and images are bundled locally. It makes no independent external network requests and does not sell or transmit user information to third parties. Clicking YouTube's native button invokes YouTube's own functionality, which may produce YouTube network activity; this policy does not govern YouTube's or Chrome's own data practices.

SkipFlow does not read account credentials, cookies, payment information, or browser history through Chrome APIs. Information processed by SkipFlow is used solely for its disclosed ad-skipping feature and preference controls. That use follows the Chrome Web Store User Data Policy, including its Limited Use requirements.

## Permissions and control

The `storage` permission saves the preference. Content scripts run only on `https://www.youtube.com/*`; no additional host permissions are declared.

Turning off Auto Skip Ads stops automatic clicks, disconnects page observers, removes active player/navigation/resize listeners, and cancels pending outcome checks. Preference and page lifecycle listeners remain to support enabling without a reload. The last player reference and attempt guard stay in memory to prevent repeated attempts; no new page observations are made while disabled. A click already dispatched cannot be undone.

SkipFlow uses ordinary JavaScript-generated native button clicks. It does not override event trust, patch page event-listener registration, or bypass YouTube interaction checks. YouTube may require a manual click. After upgrading from the earlier experimental version, reload all open YouTube pages to remove previously installed hooks. Removing the extension clears its local extension storage; reload open pages to remove already loaded scripts.

## Changes and contact

This policy should be updated whenever SkipFlow's data practices change.

For privacy questions or support, contact [trivedirt555@gmail.com](mailto:trivedirt555@gmail.com).
