ViewStats Privacy Policy

Effective date: August 22, 2026
Applies to ViewStats for YouTube & Twitch, version 1.0.0 and later versions that reference this policy.

1. Who operates ViewStats

ViewStats is responsible for the data processing described in this Privacy Policy.

Privacy and support contact:
playspansupport@gmail.com

2. Overview

ViewStats for YouTube & Twitch is a browser extension that measures how long the user spends watching video on YouTube and Twitch and shows them that history.

The extension works locally inside the browser. It does not have a developer-operated backend, user account system, analytics service, advertising SDK, tracking service, or remote database. The extension makes no network requests of any kind: its Content Security Policy sets `connect-src 'none'`, and the published package contains no code that opens a network connection. Data processed by the extension is not transmitted to ViewStats or sold to third parties.

3. Information processed on the user's device

Depending on the features used, ViewStats may process and store the following information locally in Chrome extension storage or IndexedDB:

• display, theme, and language preferences;
• separate YouTube and Twitch watch-time histories, by day and by week;
• all-time watch-time totals for each site;
• the names and identifiers of YouTube channels watched, and the user's own optional labels for them;
• content-type totals for videos, Shorts, live streams, and music;
• daily goal settings and whether a goal notification has already been shown today;
• the position and collapsed state of the optional on-page panel;
• idle-pause settings and an internal retry ledger used to avoid double-counting;
• the purchase email address entered for optional Pro activation;
• the signed Pro license key associated with that email address;
• license status, license identifier, issue date, optional expiry information, and revocation status;
• a device signing key and a signed device baseline used for Pro licensing, described in section 6.

This information is used only to measure, store, and display the user's own watch time, and to verify a purchased Pro license.

The extension does not create a general browsing history. Its content script runs only on youtube.com and twitch.tv, and it processes only what is needed to decide whether a video is playing and, on YouTube, which channel it belongs to.

The extension does not store video titles, view counts, likes, comment counts, payment card details, passwords, messages, precise location, IP addresses, exact screen resolution, canvas fingerprints, or GPU information.

4. Chrome Sync recovery mirror

A compact recovery mirror of YouTube totals and recent daily buckets is written to `chrome.storage.sync`. If the user has Chrome Sync enabled, Google may sync that mirror through the user's own signed-in Chrome account. This is handled entirely by Chrome under the user's own Google account and Chrome settings; it does not reach ViewStats.

The mirror contains daily totals and an all-time total only. Twitch history, channel names, channel identifiers, content-type breakdowns, and category labels are excluded from it.

5. Legal bases for users in the European Union and European Economic Area

Where the General Data Protection Regulation applies, ViewStats relies on the following legal bases:

• Performance of a contract or steps requested by the user under Article 6(1)(b) GDPR, including measuring watch time and validating a purchased Pro license.
• Legitimate interests under Article 6(1)(f) GDPR, including maintaining license integrity, preventing fraudulent activation, handling refunds or payment reversals, securing the extension, and providing support.
• Compliance with legal obligations under Article 6(1)(c) GDPR where transaction or business records must be retained by law.
• The user's explicit action when copying a device code, exporting a file, or activating optional features.

ViewStats's legitimate interests do not override the fundamental rights and freedoms of users. Only information necessary for the relevant function is processed.

6. Device-bound Pro licensing

A Pro license is issued for one browser installation. To make that possible, the extension creates and stores two things in extension-origin IndexedDB when a device code is first requested:

• a non-exportable signing key, generated in the browser, which cannot be read or exported by the extension or by a web page;
• a signed baseline made from hashed values of eight coarse device characteristics: platform and architecture, processor count, memory class, screen class, pixel-ratio bucket, colour-depth bucket, timezone, and primary locale.

Only per-component hashes are stored. Raw values are not retained. The baseline never reads an IP address, geolocation data, exact screen resolution, browser version, canvas or WebGL output, or installed fonts, and it requires no additional permission.

The purpose of the baseline is to bind one purchased license to one installation, not to recognise a person. The hash describes the installation it is stored in, is never compared against any other user, and cannot leave the device, because the extension makes no network requests. If the environment changes substantially, Pro pauses rather than being revoked, and returns on its own if the original environment returns.

The device code shown in the extension is derived from the public half of that signing key. It contains no email address, no name, no location, and no information about what the user watches.

7. Pro activation

Pro is activated using the purchase email address and a digitally signed license key.

The license signature is verified locally against a public verification key included in the extension package. The extension does not send an activation request, purchase email address, or license key to ViewStats or to any external server. Verification also succeeds with no internet connection.

The extension package may contain a list of revoked license identifiers. These are opaque identifiers and do not contain email addresses, payment information, or other directly identifying information. The list is identical for all installations and is checked locally.

Content scripts running on YouTube and Twitch receive only whether Pro is active. The license email, license token, license identifier, and device records are never placed into page messages, DOM attributes, `chrome.storage.local`, `chrome.storage.sync`, or exported files.

Users may remove a stored activation at any time by selecting Deactivate in the Pro section.

8. Clipboard access

ViewStats writes to the clipboard only when the user selects a copy action, such as copying the device code or copying support details. It never reads the clipboard, and it does not monitor clipboard contents.

9. Notifications

If the user sets a daily watch-time goal, the extension shows a single local notification when that goal is reached. The notification is generated by the browser on the user's own device. No notification content is transmitted anywhere. If the user does not enable a goal, no notification is ever shown.

10. Exported files

JSON and CSV exports containing the user's watch history are created locally in the popup and saved only when the user requests a download. Exports are not uploaded anywhere and do not contain the license token, device key, or device baseline.

11. Purchases through Ko-fi

Purchases take place outside the ViewStats extension through Ko-fi. Ko-fi independently processes payment information according to its own privacy policy and terms.

The information made available to ViewStats in connection with a purchase may include the buyer's email address, order information, purchase status, the device code the buyer sends, and information needed to issue or support a license. ViewStats does not receive complete payment card or bank account details, and no payment information is ever entered into the extension.

ViewStats may retain the buyer's email address, device code, license identifier, issue date, expiry information where applicable, and license status on a secured local system. These records are used only to issue, reissue, support, or revoke licenses and to handle refunds, payment reversals, fraud prevention, and legal obligations.

Purchase records are retained only for as long as reasonably necessary for these purposes or as required by applicable law. Records are deleted or anonymized when they are no longer needed, unless retention is legally required.

12. Sharing and sale of information

ViewStats does not sell personal information.

ViewStats does not share personal information for cross-context behavioral advertising, targeted advertising, profiling, creditworthiness, or lending purposes.

The extension does not transmit locally stored watch history, preference, channel, or license information to ViewStats or to third parties.

YouTube and Twitch receive the normal requests needed to use their own websites, under their own terms and privacy policies. ViewStats does not add a separate developer connection. When a user opens the Pro purchase page, Ko-fi's own terms and privacy policy apply to Ko-fi.

13. International data transfers

The extension does not transfer locally processed extension data to ViewStats or to an external server.

Ko-fi, Google, and the Chrome Web Store may process information in countries outside the user's country under their own privacy policies and legal safeguards. ViewStats does not control the independent processing performed by those services.

14. Data retention and deletion

Watch history and preferences remain on the device until the user resets them, clears extension data, or removes the extension.

"Reset Watch History" removes both the YouTube and Twitch histories, clears the YouTube recovery mirror in Chrome Sync, and invalidates open tracking sessions so previous totals cannot be replayed.

Deactivating Pro removes the stored license but keeps the installation's device identity, so the same email and key can be used to reactivate on that installation. Creating a replacement device code removes both the license and the device identity, and requires a newly issued key.

Users can:

• reset watch history from the extension's settings;
• deactivate a stored Pro license;
• create a replacement device code, which clears the device identity;
• clear ViewStats's browser storage;
• uninstall ViewStats.

Removing the extension normally removes extension-owned storage managed by Chrome.

Requests concerning purchase or license records held by ViewStats may be submitted to playspansupport@gmail.com. ViewStats may request reasonable information to verify that the requester is associated with the relevant purchase.

15. Privacy rights in the EU and EEA

Subject to applicable law, users may have the right to:

• request access to their personal data;
• request correction of inaccurate data;
• request deletion of personal data;
• restrict certain processing;
• object to processing based on legitimate interests;
• receive eligible data in a portable format;
• withdraw consent where processing is based on consent;
• lodge a complaint with the competent data protection authority.

Because extension data remains on the user's device and is not accessible to ViewStats, users can usually exercise deletion and control directly through the extension or Chrome.

Requests can be sent to playspansupport@gmail.com.

16. United States privacy rights

Residents of certain U.S. states may have rights to know, access, correct, or delete personal information and to receive information about how it is used or disclosed. Users may also have the right not to receive discriminatory treatment for exercising applicable privacy rights.

ViewStats does not sell personal information and does not share personal information for targeted or cross-context behavioral advertising. ViewStats therefore does not provide a separate "Do Not Sell or Share My Personal Information" mechanism.

Applicable requests may be submitted to playspansupport@gmail.com. ViewStats will respond as required by applicable law and may take reasonable steps to verify the request.

17. Automated decision-making

ViewStats automatically verifies license signatures, expiry information, revocation status, device-key possession, and the device baseline to determine whether Pro features are available. This process is necessary to provide and protect the purchased license, and it runs entirely on the user's own device.

ViewStats does not use personal data for profiling, advertising, credit scoring, lending, employment, insurance, or other decisions that produce legal or similarly significant effects.

18. Security

ViewStats limits data processing to information required for its functions. Extension data is stored using browser-provided storage facilities.

Pro licenses use digital signatures and are verified locally. The private signing key is never included in the published extension package; the package contains only the public verification key, which can check a signature but cannot create one. The device signing key is generated as non-exportable, so it cannot be copied out of the browser.

No method of electronic storage can be guaranteed to be completely secure. Users should protect access to their browser profile, device, purchase email account, and license key.

19. Children

ViewStats is a general-audience productivity tool and does not contain an integrated age restriction. It is not designed to solicit personal information from children or to provide child-directed advertising.

The extension does not transmit personal information to ViewStats. Pro purchases must be made by a person legally permitted to complete the transaction or by a parent or legal guardian where required.

If a parent or guardian believes that ViewStats holds purchase information relating to a child, they may contact playspansupport@gmail.com to request review or deletion.

20. Do Not Track and advertising identifiers

ViewStats does not use advertising identifiers, tracking cookies, analytics systems, behavioral advertising, or cross-site tracking. It does not respond differently to browser Do Not Track signals because it does not perform this tracking.

21. Hosting of this Privacy Policy

This Privacy Policy is hosted through GitHub Pages. When a person visits this page, GitHub may process technical information such as the visitor's IP address for security and website delivery purposes under the GitHub Privacy Statement. ViewStats does not receive or access GitHub's visitor logs.

22. Changes to this Privacy Policy

This Privacy Policy may be updated when ViewStats's functionality, legal obligations, or data practices change. The effective date at the top identifies the latest version.

If a future version introduces materially different data collection or transmission, the policy and Chrome Web Store disclosures will be updated before that version is published.

23. Contact

For privacy questions, data requests, deletion requests, purchase-record questions, and licensing support, contact:

playspansupport@gmail.com

YouTube and Google Chrome are trademarks of Google LLC. Twitch is a trademark of Twitch Interactive, Inc. ViewStats for YouTube & Twitch is an independent product and is not endorsed by, sponsored by, or affiliated with Google LLC or Twitch Interactive, Inc.
