


***Overview of Model

DQN differs from ordinary reinforcement learning in that a neural network is used for function approximation.  In particular,
it returns all the actions that can be taken from each state, along with a corresponding probability.

The navigation.ipynb shows the results of the implementation.  The agent.py module contains q-learning for fixed targets and the 
experience replay code. The latter buffers the transitions that the agent observes, allowing it to be used later. 
Specifically,by sampling from it randomly the transitions that build up a batch are decorrelated. This can stabilize
and improve the DQN training procedure. The decaying epsilon procedure allows for more exploration early in the processing, with 
more exploitation taking place later in the episode.

The model.py module contains the neural network architecture, 3 layers (2 hidden).

***Hyperparameters

1.  The RELU activation function is used with 64 nodes at each layer, excepting output, which uses logit.

2.  Replay buffer size = int(1e5)

3.  Minibatch size = 64

4.  Discount factor = 0.99

5.  Learning rate = 5e-4

6.  Number episodes = 1000

7.  Maximum timesteps each episode = 1000

8. Eps start = 1.0, eps end = 0.012, eps decay rate = 0.994

***Results

The reward improvement is shown below, followed by a chart (I couldn't get the chart to paste, so I have put a link.)

Episode 100	Average Score: 0.53

Episode 200	Average Score: 3.49

Episode 300	Average Score: 6.70

Episode 400	Average Score: 9.30

Episode 493	Average Score: 14.08

Environment solved in 393 episodes!	Average Score: 14.08


