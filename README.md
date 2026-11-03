# WalletBar v1.0.0

A standalone, offline-capable Progressive Web App for generating printable folded loyalty barcode cards, inspired by the user's old KeyRingThing printout. Not affiliated with KeyRingThing.

## Features
- Separate family profiles, each with its own loyalty cards
- Add/edit/remove/reorder cards
- Code 128 subset B, UPC-A, EAN-13 with check digit validation
- First six cards printed on a 6.75 × 2.125 inch strip; fold in half to 3.375 × 2.125 inches
- Local browser storage, JSON export/import
- Offline cache and installable PWA

## Run locally
Serve this folder using a static HTTP server, for example `python -m http.server 8000`, and open `http://localhost:8000`. Opening `index.html` directly may work for editing but does not enable service workers or PWA installation.

## Publish on GitHub Pages
Create a new repository, upload all files from this folder to the repository root, then go to **Settings > Pages > Build and deployment > Deploy from a branch > main / (root)**. Open the Pages URL on Android or Windows and use the browser's Install/Add to Home Screen option.

## Printing
Use Letter paper, **actual size / 100%**, and disable browser print headers/footers. The preview is 6.75 inches wide by 2.125 inches tall. Cut around it, fold on the center dashed line, and optionally laminate. Verify a test print scans at the relevant retailer before relying on it.

## Barcode notes
- Code 128 B supports printable ASCII characters and is appropriate for many loyalty numbers. The app does not automatically detect the barcode format from a photo.
- UPC-A and EAN-13 require complete numbers including valid check digits.
- QR, Code 39, ITF, Codabar, and dynamically generated barcodes are **not supported in v1.0.0**.
- Some store scanners reject copied barcodes or require a particular format. A printed account number may not be the encoded barcode number.
- A backup contains sensitive loyalty identifiers. Store it securely.
- Local browser storage is not synced between devices; browser data clearing can erase it.

## Future enhancements
Support more barcode formats, camera scanning/import, multi-page print sheets, card colors, and optional Google Drive sync.
