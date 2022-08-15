## Udacity Deep Reinforcement Learning Nanodegree 
## Project 2: Continuous Control

### Description of Environment

In this project, 2 identical agents must be trained to play a game of tennis against each other. The agents must use rackets to bounce a ball over a net for as long as possible without letting the ball hit the ground or hitting it out of bounds. To encourage this behaviour, each agent receives a reward of +0.1 each time it hits the ball over the net, and a reward of -0.1 if it lets the ball hit the ground or hits it out of bounds.

The state space for each agent comprises eight 3-dimensional vectors (a total of 24 dimensions) corresponding to the position and velocity of the ball and tennis racket. At each time step, each agent observes its own realisation from this state space. The action set contains two continuous numbers that indicate the movement toward or away from the net, and jumping, respectively. These were constrained to lie between -1 and +1.

The task is episodic and an episode terminates when an agent either drops the ball or hits it out of play. At the end of each episode, the total reward for each agent was returned and the maximum of the two was stored. The environment was considered solved when the average maximum reward over the last 100 consecutive episodes was greater than +0.5.


### Installation Instructions and Dependencies

The code is written in PyTorch and Python 3.6. I trained the agents using the Udacity workspace with GPU enabled. To run the code in this repository on a personal computer, follow the instructions below:

1. Create and activate a new environment with Python 3.6
    
   ###### Linux or Mac:
   
    `conda create --name drlnd python=3.6`
    
    `source activate drlnd`

   ###### Windows:

    `conda create --name drlnd python=3.6`
    
    `activate drlnd`

1. Install of OpenAI gym in the environment

   `pip install gym`
 
1. Install the classic control and box2d environment groups

   `pip install 'gym[classic_control]'`
   
   `pip install 'gym[box2d]'`

1. Clone the following repository and install the additional dependencies

   `git clone https://github.com/udacity/deep-reinforcement-learning.git`
   
   `cd deep-reinforcement-learning/python`
   
   `pip install .`

1. Download the Unity environment (available [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip) for macOS)


### Code Description

The environment described above was solved using an actor-critic algorithm, specifically the multi-agent deep deterministic policy gradient (DDPG) method. All of the files below can be found in the code folder.

#### Module Descriptions

- `model.py` defines the actor and critic networks
- `ddpg_multiple_agents.py` defines the DDPG agents

#### Training the Agents

- `Tennis.ipynb` is a Jupyter notebook that can be used to train the multi-agent DDPG model

#### The Trained Actor and Critic Networks

- `checkpoint_actor_best.pth` contains the weights of the best actor network (see Report.md)
- `checkpoint_critic_best.pth` contains the weights of the best critic network (see Report.md)
- `trained_agents.py` loads the optimised network weights and runs the trained agents for 1 episode

   

