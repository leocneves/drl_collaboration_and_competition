[//]: # (Image References)

[image1]: ./imgs/tennis.gif "Trained Agent"


# Collaboration and Competition Project - Using DDPG Algorithm to play Tennis!

### Introduction

This repository explain how to train your own intelligent agents to play Tennis with each other ([HERE IS THE ENV](https://github.com/Unity-Technologies/ml-agents/blob/main/docs/Learning-Environment-Examples.md#tennis)). It's a project part of [Udacity Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893) in Deep Reinforcement Learning.

The task selected to train our agents is Collaboration and Competition in a simple game of Tennis. Basically, we have a 3d environment with two agents and yours rackets and the objective is keep the ball in play. The image bellow illustrate this environment

<center>

![Trained Agent][image1]

</center>

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

To remember, the task is episodic and in order to solve the environment, your agents **must get an average score of +0.5 over 100 consecutive episodes, after taking the maximum over both agents**!

### Getting Start

For first, let's clone this repository... \
(Let's assume that you are executing this on Linux OS)

1. Create a path to clone the project

```bash
mkdir NAME_OF_PROJECT & cd NAME_OF_PROJECT
```

2. Clone the project

```bash
git clone https://github.com/leocneves/drl_collaboration_and_competition & cd drl_collaboration_and_competition
```

3. Follow instructions in **Dependencies** from [THIS](https://github.com/udacity/deep-reinforcement-learning#dependencies) repository

4. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip) to obtain the "headless" version of the environment.  You will **not** be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (_To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above._)

5. Place the file in the DRLND GitHub repository, in the `drl_collaboration_and_competition/` folder, and unzip (or decompress) the file.

6. Done! In this repository we've 4 main files:

 - Tennis.ipynb: Notebook with train/test code;
 - ddpg_agent.py: Code with all structure of our agent (Parameters, functions to step, select actions, update rules, etc...);
 - model.py: Contains the architecture of Neural Net applied to our agent;
 - Report.mb: Contains the description of code and results.


5. To train the agent just open the notebook **Tennis.ipynb** and execute all cells! At final of training step *(mean of last 100 rewards are more than +0.5 or episode are greater than 2000)* we can see *'checkpoint_actor.pth'* / *'checkpoint_critic.pth'* created where contains the weights of neural nets from training step and in *'results/'* we can see graph generated to illustrate convergence in learning by plotting scores for each 100 episodes.

### What's next?

* Go to the [main notebook](https://github.com/leocneves/drl_collaboration_and_competition/blob/master/Tennis.ipynb) and try to execute by yourself!

* Visit Report.md file for more details about the code and results.

---
