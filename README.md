# Overview
Punisher is a DRL without expeitation value. It used the same number and size of networks, the same loss function, and the same optimizer as DQN. The experimental results show that Punisher has obvious advantages regarding the average time-consuming per action, the number of episodes required to complete training, and the stability after training. 

# Code
using python jupyter notebook. In Punisher file there are 4 things could be adjusted:
1. state-critic policy score value
2. random action frequency
3. state-cretic network data normalization
4. policy network data normalization

# Examination data
name formate：
Ciaa_Cnbb_Pnbb_Tee_d

Ci: Critic network score;
Cn: Cretic network normalization;
Pn: Policy network normalization;
T: train process;

i: score = i;
ii: score = i  x i;
iii: score = i x i x i;
i10: score = i x 10;

n0: no noize;
n1: noize = norm(0, 0.01);
n5: noize = -0.25 ~ 0.25;

T0: no random action;
T10: 1 random action per 10 actions;
T20: 1 random action per 20 actions;

d: the d-th number of examination

For example: Cii_Cn0_Pn5_T20_3 means using Critic network score ixi, no Cretic network normalization, Policy network normalization noize = -0.25 ~ 0.25, and 1 random action per 20 actions. It is the 3rd times examination.

In each single examination data, there is a csv file and a png file. The csv file has 3 columns, store each episod's score, start time, and end time. The png file shows the examinatin result visually.

The examination data.xlsx file collects all data in one file, then analize them together.
