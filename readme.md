# **Project2. Continuous Control** 

## Readme

---

In this project, we will train an agent to maintain a double jointed arm hand's position at the goal location for as many time steps as possible.

**Project Environment Details**

* Chosen Option\
  I choose option2.
  Option2 contains 20 identical agents, each with its own copy of the environment. 
  After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different scores. We then take the average of these 20 scores. This yields an average score for each episode (where the average is over all 20 agents).

* The state\
  The state has 33 dimensions and contains the arm's position, rotation, velocity, and angular velocities.

* The action space\
  The action space is continuous, and has 4 actions, torque applicable to two joints.
  
* when the environment is considered solved\
  This task is non-episodic. A reward of +0.1 is provided for each step that agent's hand is in the goal location.
  When the average score of +30 over 100 consecutive episodes, the environment is considered solved.


**Getting Started**

* Instructions for installing dependencies or downloading needed files\

  __Step 1: Activate the Environment__\
    If you haven't already, please follow the [instructions in the DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning#dependencies) to set up your Python environment. These instructions can be found in `README.md` at the root of the repository. By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.
    
    (For Windows users) The ML-Agents toolkit supports Windows 10. While it might be possible to run the ML-Agents toolkit using other versions of Windows, it has not been tested on other versions. Furthermore, the ML-Agents toolkit has not been tested on a Windows VM such as Bootcamp or Parallels. 

  __Step 2: Download the Unity Environment__

    For this project, you will not need to install Unity - this is because Udacity have already built the environment for you, and you can download it from one of the links below. You need only select the environment that matches your operating system:

    Version1: One Agent
    Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)\
    Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)\
    Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)\
    Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

    Version2: Twenty Agents
    Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)\
    Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)\
    Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)\
    Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

    Then, place the file in the `p2_continuous-control/` folder in the DRLND GitHub repository, and unzip (or decompress) the file.

    (For Windows users) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (For AWS) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip) (version1) or [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip) (version2) to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the Linux operating system above.)

**Instructions**

* How to run the code\
  Open the "Continuous_Control.ipynb", and run all cells.
