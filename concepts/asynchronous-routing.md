# Asynchronous Routing

ION Finance uses a unique system for routing, a staple in most AMM Dex platforms. This method allows the system to determine the most efficient pathway for a token swap, even if it means routing through multiple pools to get the best rate.

Given the asynchronous nature of TON, a perfect rollback isn’t feasible. If a swap gets interrupted midway because of excessive slippage, the system will yield an intermediate result.

**Example:** Suppose you want to swap token A for token C, but there's no direct pool for A to C. The system might route your swap from A to B and then B to C. However, if the A to B step faces too much slippage, the swap might stop there, and you'll receive token B instead of C.
