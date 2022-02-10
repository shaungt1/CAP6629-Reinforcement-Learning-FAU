# Introduction
In this notebook we implement two examples of the Multi-Armed Bandit problem. The problem is defined as follows:

For a specified number of time steps, an agent is faced with a choice among k different actions. After each choice the agent receives a numerical reward value chosen from a stationary probability distribution corresponding to the action the agent selected. The agent's objective is to maximize the expected total reward over the number of time steps given.

We approximate the expected reward of an action  using a value , updating our estimate each time. At any given time step,  is given as the sum of the total reward received when taking action  over the number of times action  was taken. Computing  in this way assures that it will approximate the expected value of the reward distribution  of an action  over time.

At any time step , we can choose to take the action with the best q-value. This is called a greedy approach. However, until we have explored all the actions sufficiently, the best q-value may not represent the optimal action. So, we may choose to occasionally explore a random action, say with probability . This notebook will demonstrate the usefulness of the -greedy approach on the 10-armed testbed described in Chapter 2 of the Barto and Sutton Reinforcement Learning textbook (see references) using different  values. We will also explore this approach using a toy advertisement dataset.
