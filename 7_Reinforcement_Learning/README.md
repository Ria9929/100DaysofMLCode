## Reinforcement Learning

Reinforcement learning is the training of machine learning models to make a sequence of decisions. The agent learns to achieve a goal in an uncertain, potentially complex environment. In reinforcement learning, an artificial intelligence faces a game-like situation. The computer employs trial and error to come up with a solution to the problem. To get the machine to do what the programmer wants, the artificial intelligence gets either rewards or penalties for the actions it performs. Its goal is to maximize the total reward.
Although the designer sets the reward policy–that is, the rules of the game–he gives the model no hints or suggestions for how to solve the game. It’s up to the model to figure out how to perform the task to maximize the reward, starting from totally random trials and finishing with sophisticated tactics and superhuman skills. By leveraging the power of search and many trials, reinforcement learning is currently the most effective way to hint at a machine's creativity. In contrast to human beings, artificial intelligence can gather experience from thousands of parallel gameplays if a reinforcement learning algorithm is run on a sufficiently powerful computer infrastructure.


[1. Upper Confidence Bounds](Upper_confidence_Bound)

- Greedy Action: When an agent chooses an action that currently has the largest estimated value. The agent exploits its current knowledge by choosing the greedy action.
- Non-Greedy Action: When the agent does not choose the largest estimated value and sacrifice immediate reward hoping to gain more information about the other actions.
- Exploration: It allows the agent to improve its knowledge about each action. Hopefully, leading to a long-term benefit.
- Exploitation: It allows the agent to choose the greedy action to try to get the most reward for short-term benefit. A pure greedy action selection can lead to sub-optimal behaviour.

A dilemma occurs between exploration and exploitation because an agent can not choose to both explore and exploit at the same time. Hence, we use the Upper Confidence Bound algorithm to solve the exploration-exploitation dilemma
Upper-Confidence Bound action selection uses uncertainty in the action-value estimates for balancing exploration and exploitation. Since there is inherent uncertainty in the accuracy of the action-value estimates when we use a sampled set of rewards thus UCB uses uncertainty in the estimates to drive exploration.
The Upper Confidence Bound follows the principle of optimism in the face of uncertainty which implies that if we are uncertain about an action, we should optimistically assume that it is the correct action.

The Steps are followed in this tutorial are given below:

[!Image](../master/7_Reinforcement_Learning/Upper_confidence_Bound/UpperConfidenceBound.png)

[2. Thompson Sampling](Thompson_Sampling)

An algorithm that follows exploration and exploitation to maximize the cumulative rewards obtained by performing an action. Thompson Sampling is also sometimes referred to as Posterior Sampling or Probability Matching. An action is performed multiple times which is called exploration and based on the results obtained from the actions, either rewards or penalties, further actions are performed with the goal to maximize the reward which is called exploitation. In other words, new choices are explored to maximize rewards while exploiting the already explored choices. It addresses the exploration-exploitation dilemma in multi-armed bandit problem.

Multi-armed Bandit is synonymous to a slot machine with many arms. Each action selection is like a play of one of the slot machine’s levers, and the rewards are the payoffs for hitting the jackpot. Through repeated action selections you are to maximize your winnings by concentrating your actions on the best levers. Each machine provides a different reward from a probability distribution over mean reward specific to the machine. Without knowing these probabilities, the gambler has to maximize the sum of reward earned through a sequence of arms pull. If you maintain estimates of the action values, then at any time step there is at least one action whose estimated value is greatest. We call this a greedy action.

