# [ad] Watermark v1.2

Fixed text watermark for chart screenshots, e.g. a social media handle or a short tagline. The text is anchored to the screen (it does not move with the candles) and shows on every symbol and timeframe where the indicator is added.

It does not analyze price, draw levels, generate signals or create alerts.

## Installation

1. TradingView → **Pine Editor** → create a new indicator.
2. Paste the whole `sk-watermark.pine` file, click **Save**, then **Add to chart**.
3. Open the indicator settings (Inputs tab) and type your text.
4. Optional: hide indicator titles in the status line (chart settings → Status line) so only the watermark is visible.

## Settings

| Group | Setting | Effect |
|---|---|---|
| Main text | Text | Main line, default `IG: @nickname`. Emoji are supported. |
| Main text | Font | System, Monospace or a decorative Unicode style (Serif, Serif Italic, Sans, Sans Italic, Script, Fraktur, Double-struck). |
| Main text | Bold / Italic | Independent toggles, rendered by TradingView's text formatting. |
| Main text | Line | None, Underline or Strikethrough (Unicode combining marks). |
| Main text | Size (pt) / Color | Default 14 pt, dark grey with 25% transparency. |
| Second line | Same options | Smaller optional line under the main text. Empty = hidden. |
| Position | Location | Any corner, top or bottom center, or the chart center. Default: top right. |
| Position | Edge offset | Default 7% of the pane height, so the text is not covered by the floating drawing toolbar. |

## Behavior and limits

- Pine Script only offers the default and monospace font families. Decorative styles are built from Unicode letters and convert A–Z, a–z and 0–9 only; accented letters, emoji and punctuation stay in the system font.
- Underline and strikethrough are combining characters, so their look depends on the device font.
- The offset is a percentage of the pane height, so on a very short window the text moves down proportionally.
- The table is redrawn on the last bar only; there is no repainting logic because nothing is calculated from price.

## Version

Install it from this repository (see Installation). For TradingView updates use Pine Editor → Publish script → "Update existing script".

- v1.2-ad — prefix renamed from [SK] to [ad] (title "[ad] Watermark v1.2"); no behavior changes.
- v1.2 — whole script in English (title, inputs, options, tooltips, comments) for public publication.
- v1.1 — two lines with separate font, bold, italic, underline/strikethrough, size and color; decorative Unicode fonts.
- v1.0 — first version: single styled text with position and edge offset.

Not financial advice.
