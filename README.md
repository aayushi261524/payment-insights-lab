# Payment Insights Lab

Public prototype: https://aayushi-payment-insights.vercel.app/payment-guide.html

## Provenance
Forked from [lana-k/sqliteviz](https://github.com/lana-k/sqliteviz), Apache-2.0 licensed. SQL execution, data imports, charts, pivot tables, graphs and the offline workspace are upstream features. The original LICENSE is retained.

## Added here
public/payment-guide.html adds a sample-first payment analysis journey, eight clearly fictional attempts, a validated browser-only CSV summary, gateway/failure breakdowns, CSV download and guided SQL examples. It connects by a navigation link to the separate upstream workspace; there is no automatic data transfer.

Success rate is succeeded attempts / all attempts, including pending. Failure shares use failed attempts only. Amounts are stored in integer paise; succeeded amount is not unique-order revenue or settlement. Retry attempts count separately and need unique IDs. No live gateway, bank connection, AI decision engine or business-results claims.

## Validation and hosting
Vercel production build passed. The live guide loaded and sample totals checked: 8 attempts, 50.0% success, INR 4,700 succeeded amount. Further file/SQL/mobile checks are documented separately. Changes to master deploy automatically through Vercel’s GitHub app.

## Development / updates
See package.json. npm run build emits dist. vercel.json selects Vite and the payment guide landing route. Edit public/payment-guide.html for the guide; src/ contains the retained upstream workspace. Preserve original licence and third-party notices.
