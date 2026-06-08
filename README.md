# Incrementum Weather

Live read-only cockpit for the Polymarket Weather Trading System (PWTS).

**→ [incrementumx.github.io/weather](https://incrementumx.github.io/weather/)**

Shows screened opportunities, executed orders (with tx hash), open positions &
live P&L, plus the methodology and risk gates behind them.

- **Self-contained:** `index.html` carries all data inline (`window.PWTS_DATA`),
  so it opens from anywhere with no server.
- **Read-only:** this page only displays results. Execution is governed by the
  PWTS execution chokepoint under hard caps (NO-only, ≤$1/order, ≤$10 open) and
  lives in the private `weather-model` repo — never here.
- **Updated by the agent** each cycle via `scripts/publish_weather.sh`
  (regenerate → commit → push). Generator: `scripts/build_weather_dashboard.py`.
