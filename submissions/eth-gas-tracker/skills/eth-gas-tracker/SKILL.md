---
name: eth-gas-tracker
description: "Track Ethereum gas prices and estimate transaction costs"
version: "1.0.0"
author: "yz06276"
tags: [ethereum, gas]
---
# ETH Gas Tracker
## Overview
Track Ethereum gas prices and estimate transaction costs.
## Pre-flight Checks
1. onchainos CLI installed
## Commands
### Check Gas Price
```bash
onchainos gateway gas --chain ethereum
```
**When to use**: When the user asks about gas prices.
**Ask user to confirm** before executing.
## Error Handling
| Error | Cause | Resolution |
|-------|-------|------------|
| "Chain not supported" | Wrong chain | Use --chain ethereum |
## Skill Routing
- For swaps → use okx-dex-swap
