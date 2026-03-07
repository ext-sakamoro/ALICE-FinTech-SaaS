# ALICE-FinTech

Financial trading, settlement, and risk management platform

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum |

## ALICE Crate Integration

alice-fix, alice-ledger, alice-settlement, alice-risk, alice-crypto

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/v1/order` | FIX注文送信 |
| `POST` | `/api/v1/settle` | 決済処理 |
| `GET ` | `/api/v1/risk` | リスク分析レポート |
| `GET ` | `/api/v1/ledger` | 台帳エントリ取得 |
| `GET ` | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
