```
eInvoice Viewer 1.10.0 — application package

Drop in an e-invoice - a ZUGFeRD / Factur-X PDF, or CII / UBL XML - and read it. The
document is read in your browser and sent nowhere.

The view shows every field of EN 16931, the empty ones included, and marks amounts that do
not add up from their parts. Below the invoice, its attachments can be viewed and saved.
The app does not check whether an invoice is valid; that is for a validator to judge. A PDF
without embedded invoice data, such as a scan, cannot be read.

Put this folder anywhere and open einvoice-viewer.html. That is all: no server, no installation, no
outbound connection. It also runs straight from a hard disk or a USB stick.

Settings: config.js. That is the only file you need to touch.

WHEN UPDATING: a new package brings a fresh config.js. Overwriting yours blindly loses your
settings.

Embedding into an existing page (TYPO3, Drupal, SharePoint, your own):
  examples/embed.html shows it in full. Two things are easy to miss:

  1. assets/css/fonts.css belongs in the <head> of the page. Font declarations only take
     effect in the document; declared inside the shadow root they load not a single font.
  2. The element's data-css names three files, in this order: the tool's stylesheet, the
     kit's token file (*.tokens.css) and the kit. Without the token file the view has no
     colours.

Printing: assets/css/kit-print.css is included and deliberately NOT registered. It sets the page
up for paper - white background, no toolbar, signal edges as a line instead of a shadow. If you
want that, add this to the <head> of einvoice-viewer.html, after the kit:
  <link rel="stylesheet" href="assets/css/kit-print.css" media="print">
The order matters: after the kit, otherwise the screen rules win.

Deleting assets/fonts/ gives you a fully styled view in system fonts. That is not an error,
only a different look — and often enough for an intranet.

Licence: GPL-2.0-or-later, see LICENSE. A tool by invoicePress.
```
