# Reinforcement Learning to OpenAI Gym Space Invaders

This is on-going personal project which implements reinforcement learning to Space Invaders.

## Environment
State space is game screen images of height 210 by width 160 with 3 color channel like below from [OpenAI Gym](https://gym.openai.com/envs/SpaceInvaders-v0/), and action space is 6 discrete values of doing nothing, going right, going left, fire, going right and fire, and going left and fire. In an evaluation environment, the agent has 3 life values to survive. The higher scores you have, the better.

![alt text][screen]

## Task list
* Implement every C step update to target neural network parameter (Done 2020-01-08).
* Mimic model architecture of DeepMind human level control paper (Done 2020-01-08).
* Change input as m most recent frames stacking input (Looks like done 2020-01-09).
* Clip rewards as 1, -1, and 0 (Done 2020-01-09).
* frame-skipping technique, or selecting action on every kth frame, and repeat the same actions on skipped frames (Done 2020-01-09).
* Make stop training and restart training logic (Done 2020-01-09).

## Methodology
* Deep Q Network
* Double Deep Q Network

## Random agent

https://youtu.be/Pdfk7O5VqW0

## DQN agent

v1: https://youtu.be/LdUbFA8g3_Q

v2: https://youtu.be/PkfWF2rSZDI

![alt text][dqn_reward]

## Terminology
* model-free, reinforcement learning is model-free because it does not use transition probability distribution and reward function, which are called the model in Markov Decision Process. In contrast, model-free reinforcement learning is called trial-and-error algorithm.
* off-policy, q-learning is off-policy because it updates q values using q values of the next state and greedy action. But for example SARSA is on-policy because it updates q values using q values of the next state and current policy of an action.

## Reference
Github
* https://github.com/phossen/reinforcement-learning-2/blob/master/taxi_agent.py
* https://github.com/lilianweng/deep-reinforcement-learning-gym/blob/master/playground/policies/dqn.py

Blog
* https://hackernoon.com/how-i-trained-an-ai-to-play-atari-space-invaders-b3e8756ef026
* https://lilianweng.github.io/lil-log/2018/05/05/implementing-deep-reinforcement-learning-models.html
* https://becominghuman.ai/lets-build-an-atari-ai-part-1-dqn-df57e8ff3b26

CrossValidated
* "What is the difference between off-policy and on-policy learning", https://stats.stackexchange.com/questions/184657/what-is-the-difference-between-off-policy-and-on-policy-learning

Wikipedia
* "Model-free (reinforcement learning)", https://en.wikipedia.org/wiki/Model-free_(reinforcement_learning)

Paper
* https://nihit.github.io/resources/spaceinvaders.pdf

Colab code
* https://colab.research.google.com/drive/1DggF1gE3FjRu4ftYhYoxQCxLIOaxwVyw

[screen]: https://github.com/yukikitayama/space_invaders_reinforcement_learning/blob/master/images/space_invader_image.jpg
[dqn_reward]: https://github.com/yukikitayama/space_invaders_reinforcement_learning/blob/master/images/dqn_reward.png
