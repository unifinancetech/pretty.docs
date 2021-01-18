An ERC-20 tokenm `FLAM` will be the governance token of *unifinancetech*.

`FLAM` will be gradually released to *unifinancetech* users following the pace of the flamingo token, with the distribution being weighted based on the amount of liquidity that each user has provided.

This token will in turn be used for the protocol's governance, which will be a compound-based DAO that falls back to a multisig for the cases where quorum is not reached.

In other words, unifinancetech's DAO will run all protocol changes through the following process:
1. Initially, parties that have had 1% or more of the total `FLAM` supply delegated to them will be able to make a new proposals
2. Proposals will be voted on through a period of ~3 days
3. Proposals that have more positive than negative votes and have had more than 30% of the total supply vote for them will be accepted
4. Proposals that have more positive than negative votes but which have not achieved a 30% quorum will be eligible to be accepted by a multisig through a ~3 day period after the end of the normal voting period
5. Once accepted, proposals will be added to a timelock queue from which they will be executed in ~1 day

## Rationale
we believe that, initially, when the total supply is low, if we set a low quorum requirement for proposals to pass, it might be economically rational to perform attacks based on buying up the required supply, offensively spamming the network with proposals and getting one of these accepted to steal all of the protocol's TLV.

To prevent this, we've set the required quorum to a relatively high value (30% of total supply) but this has the potential of getting the protocol stuck if participation is low, so we've added a fallback to a multisig held by multiple devs that will be used in the cases where a proposal has community approval but hasn't reached quorum.

As the community matures and becomes more resilient to these types of attacks we plan to burn the multisig and promote proposals that lower the required quorum. Note that none of this requires the devs' cooperation, as everything can be applied through a DAO vote.

Overall we believe that this system is better than the alternative's used by other protocols such as Compound, where the multisig holder's have the ability to ban all proposals and hold the protocol ransom.

## Risks

One possible attack on this kind of system would involve having the holders of the multisig spam the DAO with a bunch of malicious proposals, preventing the community from voting on each one of them, with the end goal of eventually getting one to have enough positives votes that it could be passed through the fallback mechanism.

This should be mitigated by the fact that the spammed proposals would need to go through a 4 day period that the community could use to prevent it.
