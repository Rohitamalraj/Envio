# PermiPay Analytics Indexer

This is an Envio HyperIndex indexer for the PermiPay Analytics platform.

## What it indexes

- **PermissionGranted**: Tracks when users grant spending permissions
- **ServiceExecuted**: Records each service usage and payment
- **PermissionRevoked**: Tracks when users revoke permissions

## Contract

- **Network**: Ethereum Sepolia (Chain ID: 11155111)
- **Contract**: `0x6B3c3435DfC8dE86018dC311915E8D7af826c3Fa`
- **Start Block**: 7337440

## Services Tracked

1. Contract Inspector ($0.05)
2. Wallet Reputation ($0.10)
3. Wallet Audit ($0.15)

## GraphQL Endpoint

After deployment, you'll get a GraphQL endpoint like:
```
https://indexer.envio.dev/YOUR_PROJECT_ID/v1/graphql
```

Add this to your Next.js app's `.env.local`:
```
NEXT_PUBLIC_ENVIO_GRAPHQL_URL=https://indexer.envio.dev/YOUR_PROJECT_ID/v1/graphql
```

## Deployment

This indexer is deployed via Envio's hosted service through GitHub integration.

## Local Development

To run locally (requires Docker):

```bash
pnpm install
pnpm codegen
pnpm dev
```
