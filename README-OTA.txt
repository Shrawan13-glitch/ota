# AuraMusic OTA Artifacts

Generated files:
- metadata.json (from expo export)
- assetmap.json (from expo export)
- manifest.android.json (update manifest object)
- manifest-response.android.json (example API response envelope)
- no-update-response.json (example no-update API response)

Next edits you must do:
1. Replace https://<your-gh-pages-domain>/ota in manifest*.json with your real GitHub Pages base URL.
2. Keep runtimeVersion aligned with app.json expo.version (currently 3.0).
3. Host the entire /ota folder on GitHub Pages so bundle and assets URLs resolve.
4. Make your manifest API return manifest-response.android.json for matching requests.

Important:
- GitHub Pages alone cannot do runtime/channel/platform matching reliably. Use a tiny Worker/Function for manifest routing.
