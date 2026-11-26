# RR Accounts — Offline-first app

A standalone accounting ledger based on the structure of `[History Version]Book1 new.xlsx`.

## Included
- Default accounts: Jio, AT, Star, IndusInd, CC, Gold, KVB, UPI Lite, Cash
- Opening balances and live running balances
- Money in / money out
- Transfers between accounts (debit one account, credit the other)
- Separate `I Want to Pay` and `Credit to Collect` entries
- `Total Having` and net balance summary
- Cash Required target
- Search/filter ledger, edit/delete transactions
- Daily totals and account report
- JSON backup/restore and CSV export
- Offline cache as an installable PWA when hosted over HTTPS

## Run
Open `index.html` in a browser for local testing. For install/offline PWA behavior, deploy the folder to a static HTTPS host such as GitHub Pages, open the URL once, then use the browser's **Add to Home screen / Install app** option.

## Data storage
App records are stored in the browser's localStorage on that device. They are not cloud-synced. Export JSON backups regularly. Clearing browser site data or uninstalling the browser/app can remove records.

## Accounting notes
- `Total Having` = sum of current balances of all accounts.
- Transfer changes the two account balances but does not change Total Having.
- `I Want to Pay` = sum of payable entries.
- `Credit to Collect` = sum of receivable entries.
- `Net Balance` = Total Having − I Want to Pay + Credit to Collect.
- Cash Required is a separate manually set target because the source workbook has it as its own column.
- The original workbook is not imported; this app starts with zero opening balances to avoid silently importing old/uncertain history. Enter each opening balance yourself.


## App logo
The app logo is included in `icons/icon-192.png` and `icons/icon-512.png`, and is configured as the browser favicon, Apple touch icon, and installable PWA icon.
