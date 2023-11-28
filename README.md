# Temporal Difference Learning: SARSA vs Q-Learning, TD fixed point

TD[0] update for the value-function:

$$V(s) \leftarrow V(s) + \alpha[\overbrace{r+\gamma \underbrace{V(s')}_{\text{bootstrapping}}}^{\text{TD target}}-V(s)]$$

# TD[0] for q-functions: on-policy VS off-policy

The on-policy and off-policy versions of this algorithm are called respectively **SARSA** and **Q-learning**.

**Game**: _Cliff Walking_ environment. This is a grid world environment, with
a standard undiscounted ($\gamma = 1$) episodic task, in which there are 2 different regions:
- Walking region: any transition ending in one of the states in this region results in a reward of $-1$. Two states of
this region are marked as "start" and "goal": it is there that the episode _always_ begins and ends, respectively.
- The Cliff: any transition ending in one of the states in this region results in a reward of $-100$ and sends the agent
back to the "start" state.


