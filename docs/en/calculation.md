---
description: Откуда появилось 200 IO
icon: calculator
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# How the Stake is Calculated

To receive block rewards, you need to stake a certain amount of IO tokens. The required amount can be seen next to your worker on the [staking page](https://worker.io.net/worker/integrated-staking) or in the [documentation](https://docs.io.net/docs/proposed-device-block-reward-multiplier).

Here’s how it’s calculated:

1. The minimum stake amount is 200 IO per multiplier.
2. Each device has a specific multiplier (M), ranging from 1 to 10.
3. If the GPU multiplier is less than 1, it will be rounded up to 1.
4. For devices with multiple GPUs (N), the total stake value is calculated as: M \* N \* 200 IO.

<details>

<summary>Examples</summary>

* For a worker: 1 x H100 GPUs (multiplier 10), the minimum stake will be 1 \* 10 \* 200 = 2,000 IO
* For a worker with multiple cards: 8 x H100 GPUs (multiplier 10), the minimum stake will be 8 \* 10 \* 200 = 16,000 IO
* For a worker: 4 x 4070 GPU (multiplier 0.25, rounded up to 1), the minimum stake will be 4 \* 1 \* 200 = 800 IO

</details>
