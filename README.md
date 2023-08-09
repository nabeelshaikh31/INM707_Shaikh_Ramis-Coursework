# INM707: DEEP REINFORCEMENT LEARNING COURSEWORK

Nabeel Shaikh - 210006323 - nabeel.shaikh@city.ac.uk

## Basic Task:
### 1. Define a domain and the task:

The goal is to use Q-learning algorithm to solve a reinforcement learning task in this paper. We use Q-learning to define and solve a reinforcement learning task. Given a current state, Q-Learning is a model-free reinforcement learning policy that will determine the next best action. It selects this action at random with the goal of maximising the reward.
The OpenAI Gym offers wide variety of simulated environments. Predefined states and actions are presented by OpenAI Gym, which reduces the complexity of their use. Therefore, in this paper, the goal is to find an approach to use Q-learning algorithm to solve OpenAI Gym’s ‘Taxi-v3’ problem.
The 5 * 5 grid environment can be seen in Fig. 1, and the goal of the agent (i.e. Taxi driver) is to pick up a passenger from one location and drop the passenger off at their destination successfully in shortest number of moves possible. The four letters R, Y, B, and G identify the only tiles that allow the passenger to be picked up and dropped off. One is the passenger's location, while the other is the destination. The yellow tile represents the starting position of the taxi, blue represents the position of the passenger, purple represents the destination and green represents the position of taxi with the passenger. A pillar ‘ | ’ separates two tiles, preventing the taxi from travelling from one tile to the other.
The agent can achieve optimal policy when it maximises total rewards by reaching the destination in least number of steps.
Another thing to keep in mind is that the observation space is much broader than 25 (5*5) because we must additionally consider the passenger's position and destination, as well as whether the cab is empty or full. As a result, the observation space should be 25 * 5 (4 potential passenger locations or already in taxi) * 4 (destinations) = 500 dimensions.

## Advanced Task:
### 2. Define a domain and the task:

For the advance task Cartpole_v1 environment provided by OpenAI gym has been chosen. The environment consists of a pole, a cart, the joint attaching the pole to the cart, and a track. The main aim of cartpole or as some may call it the inverted pendulum is for the cart to maintain the balance of the unstable pole by controlling velocity and the applied force applied on the cart while remaining in center. The game has two actions: left and right, represented as: +1, -1. The episode is terminated in two cases: when the pole is tilted more than 15 degrees from the vertical axis, or when the cart moves 2.4 units away from the center. It gains a reward of +1 with every timestep passes with the pole positioned upright. The maximum steps per episode is 500 while the maximum reward obtained in an episode is 475.

Deep Q learning is applied best due to its utilization of function approximation when the state-action space is large or continuous that it would be inconvenient to use Q-learning as it would require large Q table resulting in long time and large amount of memory to run, and inaccuracy. The function approximation learns the value function in neural networks predict the Q value for a state given as an input. It stores all the past experiences in the memory and then it determines the coming action from the Q network by the maximum output. DQN has techniques that improve its performance further. This coursework highlights two of these improvements: Experience replay, Double DQN, and Dueling DQN.
