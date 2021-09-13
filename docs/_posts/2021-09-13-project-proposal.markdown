---
layout: post
title:  "Project Proposal"
date:   2021-09-13 16:52:45 -0700
---
# Using Generative Adversarial Networks to Simulate and Train against Adversarial Attackers.

Neural Nets are increasingly being used in higher and higher risk scenarios. See: self driving cars. This means the need for Neural Nets' to be robust against malicious actors will only continue to increase. Currently, even state of the art models can be tricked using relatively modest means. For example, in 2018 Eykholt et. al. were able to get models to misclassify stop signs using only a few small square stickers [(source)](https://arxiv.org/pdf/1707.08945.pdf). I propose using a Generative Adversarial Network to, on one side, simulate the actions of a malicious actor, and, on the other side, create a model that is more robust against adversarial attacks. Malicious actions will be simulated via data augmentation. 

![Example from aforementioned paper of using stickers to trick a Neural Net](https://labs.sogeti.com/wp-content/uploads/2020/05/Stop.jpg)

Here is an example from the aforementioned paper of using stickers to trick a Neural Net.

## Goals:
1. Create a method of data augmentation that simulates the actions of real world adversaries on deployed models.
2. Use this data augmentation to create a GAN that will simulate and train a model against these attacks.
3. Compare the resilience of the post GAN model with a model trained on the same set of images but without the GAN/data augmentation.
