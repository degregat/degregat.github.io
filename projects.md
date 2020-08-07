---
layout: page
title: Projects
---

# Current

## Robust Mechanism Learning

Recent advances in [Mechanism Learning](https://econcs.seas.harvard.edu/files/econcs/files/duetting_fed19.pdf), as well as the availability of readily usable [frameworks for differentially private learning](https://github.com/tensorflow/privacy) make it feasible to apply the following [result](http://kunaltalwar.org/papers/expmech.pdf) to mechanism learning: Differential privacy "can ensure that participants have limited effect on the outcome of the mechanism, and as a consequence have limited incentive to lie." 

I am currently working on making a [learner](https://github.com/degregat/deep-opt-auctions) for optimal combinatorial auctions approximately truthful, while removing the requirement to know the valuation distributions of the agents a priori.

## Distributing the Central Model for Differential Privacy (towards a practical Somewhat Trustworthy Curator)

When differential privacy in the local model is used as a data privacy technique in a distributed computation, participants guard their own privacy when executing a DP mechanism correctly, thus they have a strong motivation to do so.

When differential privacy is used in [mechanism design](http://kunaltalwar.org/papers/expmech.pdf), it usually bounds the influence of each participant on the outcome, thus they have a motivation to *not* execute it correctly. Using a trusted curator (central model) leads to the issues that come with having a single trusted node.

A solution to this issue can be to [distribute](https://www.iacr.org/archive/eurocrypt2006/40040493/40040493.pdf) the execution of the central model of differential privacy. Using secure multiparty computation, the curator gets distributed over multiple computational entities, of which some can be compromised, while still keeping certain integrity guarantees.
This way, neither the clients need to be trusted, nor does the mechanism rely on a single trusted party.

I am currently working on integrating the [secure summation of libprio](https://github.com/mozilla/libprio/) with the [discrete gaussian of googles differential privacy library](https://github.com/google/differential-privacy) to provide this. Most of the research problems have been solved, this project aims to achieve a robust, scalable and secure implementation.

# Past

## TCN Protocol

[TCN](https://github.com/TCNCoalition/TCN) is an open protocol for decentralized, privacy preserving contact tracing. It is developed by the [TCN Coalition](https://tcn-coalition.org/). I contributed to the analysis of its threatmodel and scaling behaviour.

