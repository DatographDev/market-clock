# market-clock

World trading clock: live open/closed status, next open/close countdowns, and a session timeline mapped to local time. Nine exchanges: NYSE/Nasdaq, TSX, LSE, XETRA, Nasdaq Stockholm, HKEX, Tokyo, Seoul, ASX.

- Single self-contained file: `index.html`. No build, no dependencies, no network calls. Open it in any browser.
- Hosted (no login, phone, any device): https://datographdev.github.io/market-clock/ via GitHub Pages from main; pushes go live in about a minute.
- Claude artifact copy (login-gated, kept as backup): https://claude.ai/code/artifact/88a78765-ba7c-4af3-8c31-87a9d78cfa7b
  The artifact is `index.html` minus the doctype/head wrapper (regenerate: `tail -n +9 index.html | grep -vx '</head>' | grep -vx '<body>' | grep -vx '</body>' | grep -vx '</html>'`), republished to the same URL.
- Holiday and half-day calendars hardcoded through 2027. Sources: friend's verified file (NYSE, TSX, LSE, XETRA, Tokyo, KRX incl. CSAT delayed open, ASX), gov.hk gazette (Hong Kong), Nasdaq Stockholm rules (13:00 early closes, Midsummer Eve closure). Refresh calendars in late 2027.
- Test any moment: `index.html?at=2026-12-24T14:00:00`.
