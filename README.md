# Wallet App: balance view

Shows ETH and ERC-20 balances for an address or ENS name, using your Alchemy Ethereum endpoint.

## Setup
1. Install Node 22 or newer.
2. Copy `.env.example` to `.env` and put your Alchemy key after the `=` (no quotes, no spaces).
   `.env` is in `.gitignore`, so git will not upload it.
3. Run:

```
node portfolio.mjs vitalik.eth
node portfolio.mjs 0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045
```

`node get-balance.mjs` is the original single `eth_getBalance` call.

## Tests (offline, stubbed RPC)
```
npm test
```

## Known limits
- ENS names are only lowercased, with no full ENS normalization.
- The spam filter is a heuristic and can hide an odd real token.
- Not yet tested against live Alchemy responses.
