# ssrf-fixtures

Static test pages for the SSRF acceptance test of a private web-fetch service (`ssrf-test.sh`, sections 2b and 5b).
They contain links, images, iframes, fetch/WebSocket calls and redirects towards private, loopback and link-local
addresses. The service under test must refuse every one of them; a normal browser on the public internet reaches
nothing (the addresses are not routable from outside).

- `crawl.html` – crawl start page with hostile links and two cross-host redirects (via httpbingo.org to example.*)
- `browser.html` – page whose scripts try to reach internal targets from a headless browser

No data, no tracking, no secrets. Do not link to these pages.
