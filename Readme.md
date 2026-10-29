# Apex Edge

A system prompt that turns an AI assistant with web access into a disciplined sports-betting decision-support tool. It reads your bet-slip screenshots, compares your prices to sharp-book fair value, and says "No Bet" most of the time.

**It is not a tipster and does not guarantee profit.** Most bettors lose over time.

## What it does
- Extracts teams, markets, and prices from screenshots (and asks you to confirm doubtful reads)
- Fetches reference prices from sharp books or exchanges when available
- Calculates overround, de-vigged fair probability, and EV% at your exact price
- Stress-tests every edge against a 2-point probability error
- Flags stale or soft prices at your book
- Passes on most markets in a compact one-line format

## What it will not do
- Invent prices or metrics it cannot verify (they are labelled **Unverified**)
- Infer "sharp money" from a single price snapshot
- Recommend bets just to fill a card

## How to use
1. Copy the contents of `apex-edge-prompt.md`.
2. Paste it as the system prompt or custom instructions (Claude Project, ChatGPT custom GPT, or any API system field).
3. Make sure web search/fetch is enabled. Without live data the prompt will return mostly "No Bet (insufficient data)", by design.
4. Send screenshots or type your prices, and tell it which books you can access and your bankroll or unit size.

## Known limitations
- Pinnacle, Betfair, and many odds sites block scrapers or are geo-restricted, so live data will sometimes be missing.
- Screenshot reading can misread odds. Always confirm the extracted table.
- Beating a soft book's stale number is plausible. Beating the sharp closing line with public stats is hard. Track closing line value (CLV) over 100+ bets before trusting any edge.

## Contributing
Issues and pull requests welcome, especially: de-vig method comparisons, extra sports (tennis, NFL, MLB), test boards with known answers, and CLV tracking templates.

## Disclaimer
For information and education only. Not financial or betting advice. You are responsible for following the laws in your location. Must be 18+ (or the legal age where you live). If gambling is causing harm, contact a local problem-gambling helpline.

## License
MIT
