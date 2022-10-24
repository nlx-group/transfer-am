# Transferring Confluent Knowledge to Argument Mining

This page is still **under development**.

This repository contains the code and materials to reproduce the experiments for the [paper](https://aclanthology.org/2022.coling-1.597/):

```
Transferring Confluent Knowledge to Argument Mining
João A. Rodrigues and António Branco, 2022
Proceedings of the 29th International Conference on Computational Linguistics
```

## Abstract

> Relevant to all application domains where it is important to get at the reasons underlying sentiments and decisions, argument mining seeks to obtain structured arguments from unstructured text and has been addressed by approaches typically involving some feature and/or neural architecture engineering.
>
> By adopting a transfer learning methodology, and by means of a systematic study with a wide range of knowledge sources promisingly suitable to leverage argument mining, the aim of this paper is to empirically assess the potential of transferring such knowledge learned with confluent tasks. 
>
> By adopting a lean approach that dispenses with heavier feature and model engineering, this study permitted both to gain novel empirically based insights into the argument mining task and to establish new state of the art levels of performance for its three main sub-tasks, viz. identification of argument components, classification of the components, and determination of the relation among them.

## Data

To proceed with our systematic study of transfer learning for argument mining on a mainstream pipeline of sub-tasks, which includes identifying argument components, classifying their clausal roles and determining the relational properties among them, we resorted to the [Argument Annotated Essays (version 2)](https://tudatalib.ulb.tu-darmstadt.de/handle/tudatalib/2422).

For the tasks that are the source of knowledge to be transferred to argument mining models, we resorted to a vast array of [annotated data sets](https://github.com/nyu-mll/jiant/blob/master/guides/tasks/supported_tasks.md).


## Code

All the experiments, namely single-step and multi-step transfer, were performed with the NLP toolkit [jiant](https://github.com/nyu-mll/jiant) and the [RoBERTa](https://arxiv.org/abs/1907.11692) model.

For the fine-tuning of the target tasks, we performed a hyperparameter search with three learning rates (1e<sup>-5</sup>, 3e<sup>-5</sup> and 5e<sup>-5</sup>) and three random seeds on the target task development set, creating a total of 396 models.
