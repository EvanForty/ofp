# OFP — Launch a coin. Route the flow.

Static website for OFP, the Solana launchpad where every coin opens with its own order flow routing agent.

Follow: https://x.com/OFPagent

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole site: styles, 3D routing floor, Solana wallet connect, agent launcher |
| `favicon.png` | Browser tab icon |
| `ofp-logo.png` | Router chip logo artwork |
| `vercel.json` | Vercel config (clean URLs, security and cache headers) |

There is no build step and nothing to install. Three.js r128 loads from cdnjs and `@solana/web3.js` 1.95.3 from jsDelivr.

## Deploy on Vercel

1. Push these files to the root of a GitHub repo.
2. In Vercel, choose **Add New → Project** and import the repo.
3. Leave Framework Preset as **Other**, Build Command empty and Output Directory empty.
4. Click **Deploy**.

## Run locally

Wallet extensions don't connect to pages opened as files, so serve the folder:

```bash
npx serve .
```

## Configuration

- **RPC:** in `index.html`, set `RPC_URL` to a dedicated Solana RPC (Helius, Triton, QuickNode). The public endpoint is rate limited.
- **Wallets:** Phantom, Solflare and Backpack are detected automatically.
