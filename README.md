# Blackbox Privacy Policy

The published policy is at https://limkxrby.github.io/blackbox-privacy/ and the source is in `index.html`.

Blackbox stores supported HTTP and HTTPS tab URLs and titles, tab order, pinned, active, discarded and last-accessed state, window membership and focus, tab-group names, colors, collapsed state and membership, and a broad category derived from each address. It stores idle-tab settings, seal names, times and counts, an optional passphrase hint, and an encrypted passphrase check. A keyed digest is used for duplicate detection. These data stay in `chrome.storage.local` on the device.

Session contents are encrypted with AES-GCM. The device key is stored unencrypted in `chrome.storage.local` so local restore can work without a passphrase; access to the Chrome profile may expose both the key and the seals. Seal names, times, counts, settings, and the optional hint remain readable locally.

New optional `.bbx` backups contain format and key-derivation parameters, random salt and IV, and ciphertext. Session contents, hint, creation time, and counts are encrypted. New backups use PBKDF2-SHA-256 with 600,000 iterations; older backups remain importable and may have a readable hint and counts. Blackbox does not upload backups or session data, and it has no account, analytics, telemetry, advertising, or extension-initiated network requests. Restoring a web address causes Chrome to load that page normally.

Blackbox's use of information received through Chrome APIs follows the Chrome Web Store User Data Policy, including its Limited Use requirements. It uses browsing activity only for the user-facing session and tab features.

Contact: open an issue in this repository.
