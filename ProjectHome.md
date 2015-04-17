# LibPG #

The PG library was intended to be a high-performance policy-gradient
reinforcement learning library. Since the first version it has been
extended to a number of value based RL algorithms, so the name is only
historical. It is now a general RL library which implements, for example, natural actor critic, and least squares policy iteration.  It has been designed with
large distributed RL systems in mind. It's not perfect, but it is
pretty fast. API documentation and examples are provided.

What libpg does NOT provide is model based planning algorithms such as
value iteration, or real-time dynamic programming, or exact policy
gradient. There is limited support for belief state tracking in the
simulators/Cassandra/ directory (named because we use the POMDP file
format created by Anthony Cassandra).  One day I'd like to extend it
to these situations, but that will require some uptake of the library.

## Project goals ##

  * Provide easy to use implementations of state-of-the-art RL algorithms
> for the non RL savvy, allowing immediate application to difficult industry
> problems.
  * High performance, especially on multi-agent RL problems
  * Extensible plug'n'play algorithms for research purposes

## Main algorithms implemented ##

RL algorithms:
  * SARSA
  * QLearning
  * Vanilla Policy-Gradient (online or batch, including line search)
  * Natural actor-critic
  * Least Squares TD-Q(\lambda) (for LSPI)
  * Least Squares Policy Iteration

Misc supporting algorithms:
  * Line searches for batch mode
  * Tikhonov Regularisation
  * HMM based POMDP state estimation
  * Finite history transformation