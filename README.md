# Pairs of Crypto Exchanges

![Refresh cadence](https://img.shields.io/badge/refresh-weekly-brightgreen)

**Pairs of Crypto Exchanges** automatically fetches and updates **TradingView-importable** watchlists for BTC-, USD- and USDT-quoted **spot** pairs. The project gathers fresh exchange data and publishes plain-text symbols lists for easy TradingView import.

The lists are refreshed **weekly** using [ccxt](https://github.com/ccxt/ccxt) and GitHub Actions.

---

## 📦 Project release

- **v1.0.0** — initial import to `OdynBrouwer/pairs-of-crypto-exchanges`
- Added support for **Bybit** and **WOO**
- Supports BTC, USD, and USDT watchlists across multiple exchanges
- Switched CI to `npm` and removed old `pnpm` metadata

---

## 📂 Outputs

-   **BINANCE**
-   **OKX**
-   **MEXC**
-   **COINBASE**
-   **KUCOIN**
-   **BYBIT**
-   **WOO**

The lists are refreshed **weekly** using [ccxt](https://github.com/ccxt/ccxt) and GitHub Actions.

---

## 📂 Outputs

| File pattern                          | Description                                 |
| ------------------------------------- | ------------------------------------------- |
| `lists/ALL_<QUOTE>_PAIRS.txt`         | Combined quote watchlist, grouped by exchange |
| `lists/<EXCHANGE>_<QUOTE>_PAIRS.txt`  | Exchange-specific quote watchlist           |
| `META.json`                           | Metadata (timestamp, exchanges, quotes, file list) |

---

## ✨ Features

-   **Weekly auto-updates** via GitHub Actions
-   **Multiple exchanges** (BINANCE, OKX, MEXC, COINBASE, KUCOIN, BYBIT, WOO)
-   **TradingView-ready format** (`EXCHANGE:BASE<QUOTE>`)
-   **Plain text output** (no JSON/CSV parsing needed)
-   **Open source** & easy to extend
-   **Metadata file** for programmatic use

---

## 📥 How to import into TradingView

1. Open TradingView → **Watchlist** panel.
2. Click **⋮** (More) → **Import watchlist**, or use **Add symbol → Paste**.
3. Paste the contents of one of the files in [`lists/`](./lists/), e.g., [`ALL_BTC_PAIRS.txt`](./lists/ALL_BTC_PAIRS.txt).
4. Confirm.

---

## 🛠 Local build

```bash
git clone https://github.com/OdynBrouwer/pairs-of-crypto-exchanges.git
cd pairs-of-crypto-exchanges
npm install
npm run generate
# Outputs in lists/*.txt
```
