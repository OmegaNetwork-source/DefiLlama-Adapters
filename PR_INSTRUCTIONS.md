# Open the DefiLlama PR (do this from your side)

All code changes are **already done** in this clone and committed.

## 1. Fork DefiLlama-Adapters on GitHub

1. Go to https://github.com/DefiLlama/DefiLlama-Adapters
2. Click **Fork** (top right) to create a fork under your account.

## 2. Add your fork as a remote and push

```bash
cd DefiLlama-Adapters
git remote add myfork https://github.com/OmegaNetwork-source/DefiLlama-Adapters.git
git push myfork main
```

Or with SSH:

```bash
git remote add myfork git@github.com:OmegaNetwork-source/DefiLlama-Adapters.git
git push myfork main
```

## 3. Open the Pull Request

1. Go to **your fork** on GitHub: https://github.com/OmegaNetwork-source/DefiLlama-Adapters
2. You should see "main had recent pushes" with an option **Compare & pull request**. Click it.
3. Base: `DefiLlama/DefiLlama-Adapters` ← `main`, Compare: `OmegaNetwork-source/main`.
4. **Title:** `Add Omega Network chain and Olympus protocol`
5. **Description** (paste this):

```
## Add Omega Network chain and Olympus protocol

- **Chain:** Omega Network (chainId 1313161916, shortName `omega`)
  - RPC: https://0x4e4542bc.rpc.aurora-cloud.dev
- **Protocol:** Olympus — DEX + prediction markets on Omega
- **TVL:** PRE and mUSDC in the Olympus market maker wallet for the PRE/mUSDC pair

Changes:
- `projects/helper/chains.json`: added `"omega"` to chains list
- `projects/helper/tokenMapping.js`: added Omega token mappings (PRE, mUSDC)
- `projects/olympus/index.js`: Olympus adapter for Omega chain
```

6. Click **Create pull request**.

After the PR is merged, allow ~24 hours for the DefiLlama frontend to show Omega and Olympus.
