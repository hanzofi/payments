# Hanzo Fi Payments Connectivity

Payment provider connectors. Unified interface across Stripe, Adyen, Wise, Modulr, MangoPay, and more.

## Supported Connectors

| Provider | Type |
|----------|------|
| Stripe | Cards, wallets |
| Adyen | Cards, local methods |
| Wise | International transfers |
| Modulr | Banking-as-a-service |
| MangoPay | Marketplace payments |
| CurrencyCloud | FX & cross-border |
| Banking Circle | B2B payments |
| Moneycorp | FX |
| Atlar | Open banking |
| Generic | Custom connector |

## Quick Start

```bash
docker compose up -d

curl -X POST http://localhost:8080/v2/payments/connectors/stripe/install \
  -H "Content-Type: application/json" \
  -d '{"apiKey": "sk_..."}'
```

## API

- `POST /v2/payments/connectors/{name}/install` — Install connector
- `GET /v2/payments` — List payments
- `POST /v2/payments/transfer-initiations` — Initiate transfer

## License

MIT — see [LICENSE](LICENSE)

