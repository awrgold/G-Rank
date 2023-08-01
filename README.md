# G-Rank
G-Rank - Unsupervised Continuous Learn-to-Rank for Edge Devices in p2p Networks. 

- Paper: https://arxiv.org/pdf/2301.12530.pdf

## Abstract

*Ranking algorithms in traditional search engines are powered by enormous training data sets that are meticulously engineered and curated by a centralized entity.
Decentralized peer-to-peer (p2p) networks such as torrenting applications and Web3 protocols deliberately eschew centralized databases and computational architectures when designing services and features. 
As such, robust search-and-rank algorithms designed for such domains must be engineered specifically for decentralized networks, and must be lightweight enough to operate on consumer-grade personal devices such as a smartphone or laptop computer. 
We introduce G-Rank, an unsupervised ranking algorithm designed exclusively for decentralized networks. We demonstrate that accurate, relevant ranking results can be achieved in fully decentralized networks without any centralized data aggregation, feature engineering, or model training. 
Furthermore, we show that such results are obtainable with minimal data preprocessing and computational overhead, and can still return highly relevant results even when a user's device is disconnected from the network. 
G-Rank is highly modular in design, is not limited to categorical data, and can be implemented in a variety of domains with minimal modification. 
The results herein show that unsupervised ranking models designed for decentralized p2p networks are not only viable, but worthy of further research.*


---

## Outline

This repository contains a Jupyter Notebook file containing all data sets, methods, and functionality to experiment with G-Rank.
No setup is required beyond installing the proper libraries is required. Required libraries are: `Pandas`, `Numpy`, `Plotly-express`, and `Matplotlib`. 
Versions of these libraries should not matter and should be intercompatible.
Each cell represents a simulation module, including the Node object, Network object, and each of G-Rank's core functions.
Below the break is the simulation loop, including all simulation parameters and evaluation metrics.
Anyone can comment out or augment the simulation parameters to hone in on specific simulations, or run all simulations consecutively.

The simulation is based on discrete time steps.
Depending on parameters, each time step takes anywhere from 30 milliseconds to 2000 milliseconds, with the highest performance impact stemming from three features:
- The gossip protocol, *i.e.* how many peers request and receive gossip, and
- The frequency with which nodes update their local information, and
- The type of adversarial attack, *i.e.* simulations with many adversaries OR a high degree of adversarial interference strongly impact simulation time.

Small simulations (10 nodes, 1000 time steps) can take anywhere from 2-10 minutes (on a modern desktop PC with 16GB RAM).
Large simulations (100+ nodes, 10000+ time steps) can take anywhere from 30-1000 minutes (on a modern desktop PC with 16GB RAM).


