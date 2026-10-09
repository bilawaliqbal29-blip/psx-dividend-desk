# PSX Dividend Desk

A personal planner for building a long-term dividend portfolio on the Pakistan Stock Exchange: save a little every day, buy once a week, and track the dividends that come in.

**Web app:** https://bilawaliqbal29-blip.github.io/psx-dividend-desk/

## What it does

- **This week:** mark what you set aside each day. The app turns the cash you have ready into a buy slip, with whole shares spread across the stocks on your target list that are most underweight. It skips orders too small to be worth the trading costs.
- **Rankings:** every share gets a score out of 100. The score weighs dividend yield (30%), whether profits cover the payout (20%), price against earnings (15%), how steadily it has paid (15%), growth (10%) and how easy it is to trade (10%). You can switch to Shariah-compliant shares only (KMI-listed), and include or leave out ETFs.
- **Holdings:** your shares, gains, dividends received after tax, and a projection of where steady saving could take you.

## Weekly routine

1. Open https://dps.psx.com.pk/screener, copy the whole results table and paste it into **Import & settings**.
2. On **This week**, place the orders on the buy slip with your broker, then press **Mark as bought**.
3. When a dividend reaches your bank, record it under **Holdings**.

To refresh prices on their own, you can also load PSX's daily closing-rates `.Z` file from the Downloads page.

## Data and sync

Data is saved in the browser. When you sign in, it also syncs to the `psx` schema of the shared Supabase project, where each user can read and write only their own rows.

## Publishing

Every push to `main` publishes `www/` to GitHub Pages through `.github/workflows/web.yml`. This needs **Settings → Pages → Source: GitHub Actions** turned on once.

This tool ranks shares with a fixed formula on data you import. It is not investment advice.
