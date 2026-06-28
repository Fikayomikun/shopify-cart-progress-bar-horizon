# Cart Progress Bar — Horizon Theme

A free-shipping progress bar for the Shopify Horizon theme. Shows customers how close they are to qualifying for free shipping, with dynamic colour changes when the threshold is reached.

## What it does

- Calculates progress from the current cart total against a configurable threshold
- Progress bar fills dynamically as items are added
- Colour and messaging change when the threshold is reached
- All settings configurable in the Shopify theme editor — no code needed

## Files

| File | Purpose |
|------|---------|
| `snippets/cart-progress-bar.liquid` | Main progress bar logic and HTML |
| `snippets/shipping-progress-icon.liquid` | Reusable SVG truck icon |
| `assets/cart-progress-bar.css` | All styling |
| `config/settings_schema.json` | Theme editor settings |

## Theme settings

Configurable under **Theme settings** in the Shopify theme editor:

| Setting | Description |
|---------|-------------|
| `minimum_free_shipping_amount` | Free shipping threshold in euros |
| `shipping_progress_bar_text` | Message shown below the bar |
| `background_bar_color` | Track background colour |
| `progress_bar_color` | Fill colour before threshold |
| `completed_bar_color` | Fill colour after threshold |
| `progress_message_color` | Text colour before threshold |

## How it works

Liquid calculates the percentage of the cart total against the threshold at page render. The fill width is set inline as a style attribute — no JavaScript required. A CSS class (`is-complete`) is toggled when progress hits 100%, switching colours for both the bar and the message.

## Dev store

Live preview available at the dev store — password on request.
