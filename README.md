# UPi (UPI intent-checkout demo)

A single-file demo of a **UPI Intent** checkout flow. It builds a UPI deep link
(`upi://pay?...`) for a merchant, shows a QR code for the same link, and lets you
open it in a UPI app on mobile or copy the link.

## What it does

- Merchant / amount / transaction-note form with validation.
- Generates a standard UPI intent URI (`pa`, `pn`, `am`, `cu`, `tn`, `tr`).
- Renders a scannable QR code with `qrcodejs`.
- “Pay with UPI” button that hands off to the installed UPI app.
- Responsive, dependency-free styling.

## Run

Open `upi_checkout_demo.html` in a browser. For mobile testing, serve it over
HTTPS or your LAN:

```bash
npx serve .
```

> This is a front-end demo only — no payment is captured or verified. A real
> integration must validate the transaction server-side (PSP webhook / UPI
> status API) before fulfilling an order.
