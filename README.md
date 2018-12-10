# Udacity Deep Reinforcment Learning Nanodegree - Project 2 - Continuous Control  

This github repository contains a possible solution for the scond project of the Udacity Deep Reinforcment Learning Nanodegree program. It is based on a Unity environment. The solution described in this repository is based on DDPG (Deep Deterministic Policy Gradient) architecture.

The foundation for the solution was provided in the Udacity repository for the Deep Reinforcement Learning Nanodegree [Udacity Deep Reinforcement Learning Nanodegree](https://github.com/udacity/deep-reinforcement-learning/tree/master/p2_continuous-control)


You can find the detailled information on the exercise [here](https://github.com/udacity/deep-reinforcement-learning/tree/master/p1_navigation).

Find details on the Unity Reacher evnironment [here.](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher)

## The task

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.


The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes. In this solution multiple agents are used (contains 20 identical agents, each with its own copy of the environment) there the environment is solved, if an average score of +30 (over 100 consecutive episodes, and over all agents) is achieved.

Aproach:

* After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores.
* This yields an average score for each episode (where the average is over all 20 agents).

## Prerequisites

In order to run the code in this repository, it is required to follow the instructions as porvided in the Udacity Deep Reinforcment Learning Nanodegree repository. In order to install all required dependencies, please follow the instructions provided [here](https://github.com/udacity/deep-reinforcement-learning#dependencies).


Unity provides a prebuild simulator for multiple plattforms of the banana navigation environment. It is required to be installed and an environment need to be up and running to train and run the agent in scope of the exercise. Instructions on how to obtain it can be found in the 'Getting started' section in the following [README file](https://github.com/udacity/deep-reinforcement-learning/tree/master/p2_continuous-control/README.md)


## Instructions

1. Download the environment that matches your environment (I used the AWS setup for best perfromance). See Udacity's instruction on obtaining the right environment [here.](https://github.com/udacity/deep-reinforcement-learning/tree/master/p2_continuous-control/README.md) 
2. Place the file in your copy of the [DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning), in the p2_continuous-control/ folder, and unzip (or decompress) the file.
3. Copy the files model.py and agent.py as well as the Continuous_Control.ipynb into the same folder. Replace Udacity's version of the Continuous_Control.ipynb file with the version from this repo.

Run the notebook file Continuous_Control.ipynb in this repository to further setup the notebook according to your environment, to train the agent, and to run the agent.

The training will generate the file checkpoint_actor.pth and checkpoint_critic.pth with the learned model weights. You can use this to simulate how your trained agent is behaving in the Unity environment.
