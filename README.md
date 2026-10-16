# GhostPixel — Bronx Edition

[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

A tiny browser-based recon/workshop tool that checks whether an image URL loads from the client and reports host, dimensions, and load time. The app is a single static HTML page with minimal JS — ideal for workshops or quick client-side checks.

## Demo

![Screenshot](assets/screenshot.svg)

## Features

- Enter an image URL and measure whether it loads, its size (width × height), and load time.
- Saves a local history of scans using localStorage (exportable JSON).
- Quick workshop buttons to set example image targets.
- Lightweight single-file UI (index.html).

## Getting started

1. Clone the repository:

   git clone https://github.com/droidjedininja/ghostpixel-recon-v2.git

2. Open index.html in your browser (or serve the directory with a static web server):

   - Example (Python 3): python -m http.server 8000
   - Then visit http://localhost:8000 in your browser.

3. Enter an image URL and click "Run Scan". Results and a preview appear on success.

## Implementation notes

- Primary file: `index.html` (UI, JS, and CSS in a single file).
- History is stored under localStorage key `ghostpixel-history` and capped to the most recent 50 records.
- The app uses the Image() API and `performance.now()` to measure load times. `img.crossOrigin = 'anonymous'` is set to reduce canvas tainting if extended later.

## Security & Privacy

- This tool runs entirely client-side in the user's browser. It triggers standard browser network requests to the target hosts.
- Do not scan targets you do not have permission to test.
- If you find a security issue, see SECURITY.md for reporting guidance.

## Contributing

See .github/CONTRIBUTING.md for contribution guidelines. Small improvements, bug fixes, and documentation updates are welcome — please open a PR.

## License

This project is licensed under the MIT License. See LICENSE for details.
