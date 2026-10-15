# ExposedAPI iOS — native starter

A small SwiftUI iPhone app that performs one authorized HTTPS GET check, shows HTTP status, content type, and CORS headers, and prevents cross-host redirects. No Kali or server is required to perform this check.

## Build on macOS
1. Install Xcode.
2. Create a new iOS App project named `ExposedAPI` (SwiftUI, Swift).
3. Replace the generated `ExposedAPIApp.swift` and `ContentView.swift` with the files in `ExposedAPI/`.
4. Set your signing team under Signing & Capabilities.
5. Connect your iPhone and select it as the run destination, then press Run. Developer Mode may need to be enabled on the phone.

## Limitations
- This is source code, not an installable .ipa.
- A Mac with Xcode or a configured remote macOS build service is needed to compile/sign a native iOS app.
- Only a single HTTPS GET request per scan; no crawling, authentication, subdomain enumeration, or automated vulnerability exploitation.
- Host must match the explicitly entered allowed hostname exactly. Redirects are not followed.
- A reflected Origin header is only a review candidate, not proof of a vulnerability.
- No persistent scan history in this starter.
