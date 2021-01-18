# Introduction
> the most efficient farmer on [*flamingo*](https://flamingo.finance)

[*unifinancetech*](https://unifinancetech.github.io) farms on [*flamingo*](https://flamingo.finance) and earn profits.

```
users -------+                        +-> flamingo wrapper
             |                        |-> flamingo vault
strategists ---> vaults ---> actions ---> flamingo swap
             |                        |-> flamingo perp
governances -+                        +-> other productions
```

Users deposit (or withdraw) tokens to (or from) unifinancetech vaults, where they are allocated to different DeFi protocols/pools with the goal of maximizing their APY.

This optimized allocation of tokens will be done through an strategist, a party that's heavily restricted in what it can do, as it can only take actions from a whitelisted set that is directly encoded in the contract, which will initially be a chosen operator that will be transitioned into a smart contract.

The strategist will then use the tokens present in the vaults to farm the several [*flamingo*](https://flamingo.finance) protocols (as well as others) in an optimal way.

See [Strategies](/strategies) for a list of all whitelisted actions available to the strategist.

This whole protocol will then be managed in a decentralzied way through a DAO, which will have access to all vaults, and will be able to change the strategist or the actions it is capable of performing.