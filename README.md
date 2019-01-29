[//]: # (Image References)

[image1]: https://s3.amazonaws.com/video.udacity-data.com/topher/2018/June/5b1ea778_reacher/reacher.gif

# Deep Reinforcement Learning Continuous Control Example

### Introduction

This project is an example of deep reinforcement learning using a recurrent neural network (RNN). The coding framework was provided courtesy of Udacity's Deep Reinforcement Learning Nanodegree Program, with an environment created using Unity's ML-Agents plugin.

In the example, an agent is trained using Deep Deterministic Policy Gradient (DDPG) over a series of episodes. It begins with no knowledge of its environment, and first learns only by taking actions at random. The agent's experiences are catalogued and it gradually begins making decisions to maximize its reward instead of choosing random actions. The environment is solved once the agent achieves an average score of +30 over 100 consecutive episodes.

### How to Run

If you already have a working Python/ML-Agents environment, simply download all files in the p2-continuous-controlfolder open the attached workbook file named "Continuous_Control.ipynb" in Jupyter. After this, run the code cells in the workbook's first two sections to et up your own environment and its agent. After this is complete, you can train your own agent and save its weights to the checkpoint_actor.pth and checkpoint_critic_pth files by running the code in the third section.

### Environment

In this environment, a double-jointed arm can move to target locations.

![Trained Agent][image1]

A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

### Getting Started

To begin, you will need to set up your Python environment by following the instructions below.

1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```
	
2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.  
	- Next, install the **classic control** environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
	- Then, install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).
	
3. Clone this repository and navigate to the `python/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

### Instructions

Once all dependencies have been installed properly, you'll need to set up the environment.

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the file in the repository, in the `p1_navigation/` folder, and unzip (or decompress) the file. 

3. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

4. Before running code in a notebook, change its kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

Follow the instructions in `Navigation.ipynb` to get started with training your own agent!  
