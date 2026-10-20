# Lift Memo

Turn the results of a holdout test into a one-page memo a finance lead would believe. Enter the treated and control counts, the spend, revenue per conversion and margin, and get a plain-English bottom line, a results table with ranges, and the caveats, ready to copy or print.

Open `index.html` in any browser. No build step and no dependencies.

- **Verdict:** `lift proven`, `lift not proven` or `ads lost sales`, from whether the range of the lift excludes zero.
- **Memo:** bottom line first, then the test table, then results with ranges (lift in points, relative lift, extra conversions, extra revenue, incremental ROAS, profit after spend, cost per extra conversion), how sure we are, and what the test does not show.
- **Checks:** sample ratio mismatch against your planned control share (flagged when p < 0.001), and a warning when control has under 50 conversions.
- **Method:** Wilson intervals per group combined with Newcombe's method for the lift, the log rate ratio for relative lift, and the lift range scaled by group size, revenue per conversion, margin and spend.
- **Output:** copy as plain text, print, or download a card. The URL hash carries your numbers.

Assumes random assignment and no leakage, and covers the test window only. Revenue per conversion and margin are inputs, not measured by the test. Pairs with holdout-sizer, which plans the test.

## License

Code is MIT licensed ([LICENSE](LICENSE)). The bundled fonts (Bricolage Grotesque, Archivo) are SIL OFL 1.1, with licenses in `fonts/`. The ben.j.ads wordmark and footnote mark in `logo/` are Ben Johnston's brand assets and are not covered by the MIT license.
