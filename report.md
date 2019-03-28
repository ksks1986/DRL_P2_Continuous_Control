# **Project2. Continuous Control** 

## Report

---

[//]: # (Image References)
[image1]: ./result.png "Visualization"


**Learning Algorithm**
* DDPG\
 This algorithm has four networks, actor target, actor local, critic target and critic local. Each target network is used for training, and is soft-updated by each local network.\
 
 This implementation is shown in model.py and ddpg_agent.py.

  My final actor network model consisted of the following layers:
  | Layer         		    |   Description	           		                      |
  |:----------------------|:--------------------------------------------------| 
  | (1)Input         		  |   33 dimensions states                            | 
  | (2)Batch Normalization|                                                   |
  | (3)Fully connected		|   input 33, outputs 400                           |
  | (4)ReLU		            |        									                          |
  | (5)Fully connected		|   input 400, outputs 300                          |
  | (6)ReLU		            |        									                          |
  | (7)Fully connected    |   input 300, outputs 4                            |
  | (8)tanh		            |                                                   |

  My final critic network model consisted of the following layers:
  | Layer         		    |   Description	           		                      |
  |:----------------------|:--------------------------------------------------| 
  | (1)Input         		  |   33 dimensions states                            | 
  | (2)Batch Normalization|                                                   |
  | (3)Fully connected		|   input 33, outputs 400                           |
  | (4)ReLU		            |        									                          |
  | (5)Concatinating		  |   input 400 + 4(action), outputs 404  				    |
  | (5)Fully connected		|   input 404, outputs 300                          |
  | (6)ReLU		            |        									                          |
  | (7)Fully connected    |   input 300, outputs 1                            |


* hyperparameter\
 Used hyperparameters are shown below. 

  - BUFFER_SIZE = int(2e6)  # replay buffer size
  - BATCH_SIZE = 128        # minibatch size
  - GAMMA = 0.99            # discount factor
  - TAU = 1e-3              # for soft update of target parameters
  - LR_ACTOR = 6e-4         # learning rate of the actor 
  - LR_CRITIC = 1e-3        # learning rate of the critic
  - WEIGHT_DECAY = 0        # L2 weight decay
  - LEARN_FREQ = 20         # how often to update the network
  - LEARN_NUM = 10          # the number of learning
  - theta = 0.15            # Ornstein-Uhlenbeck process parameter
  - sigma = 0.1             # Ornstein-Uhlenbeck process parameter
  - mu = 0.0                # Ornstein-Uhlenbeck process parameter



**Plot of Rewards**\
 The scores of DDPG show below.
 After 300 Episodes, average score exceeds 30.0. 

![alt text][image1]


The scores when the model learning is below.
Average window size is 100 episodes.\

* DDPG\
Episode 200	Average Score: 25.41\
Episode 300	Average Score: 34.11\
Episode 400	Average Score: 35.11\
Episode 500	Average Score: 34.02

**Ideas for Future Work**\
  In Addition to current learning algorithm, prioritized replay buffer should be implemented.\
  Probably, D4PG will get better result than current one.
