# Deploying TREE

## How to deploy TREE

### 1. Stage 1

Stage 1 of deployment will deploy all of the contracts and burn the admin keys.

UniswapOracle will be left uninitialized after this stage, because initialization requires existing liquidity in the TREE-yyCRV UNI-V2 pool.

The LP reward pool and the forests (initial distribution pools) will be activated 24 hours after deployment.

This stage is when the TREE initial distribution & price discovery happens. Rebasing is not enabled.

#### Command

```bash
npx buidler deploy --network [networkName] --tags stage1
```

### 2. Stage 2

Stage 2 of deployment will initialize UniswapOracle. Before stage 2 there must be existing liquidity in the TREE-yyCRV UNI-V2 pool.

Rebasing will be enabled 12 hours after UniswapOracle is initialized.

#### Command

```bash
npx buidler deploy --network [networkName] --tags stage2
```