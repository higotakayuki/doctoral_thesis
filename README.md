#Doctor thesis about evolutionary algorithms

This project contains tex files of my doctor thesis.

#Summary of the doctor thesis
Evolutinary algorithms (EAs) are algorithms inspired by biological system. EAs are considered to be a kind of optimization methods, but there exists more practical optimization methods, i.e., simplex method, branch and cut algorithm (Gurobi is extremly excellent), and so on. EAs are, however, still important because EAs are based on sampling approach which is dafferent from the above methods and also EAs can approach multi-armed bandit problems, which are the basic of reinforecement learning and also A/B tests.
 
I have tried to mathematically improve EAs, especeially Genetic Algorithms. First of all, I proposed a basic mathematical model of EAs. This model can be new but is similar to the cross entropy method, proposed by Reuven Rubinstein. This point is not important because the basic mathematical model is just the start point of my research.
 
In my Doctor thesis, there are three contributions. First one is a mathematical derivation of the population mechanism, which allows us to reuse past generated solutions. In the basic mathematical model, generated solutions are used only once (for crossover) and are imediately discarded like UMDA while genetic algorithms keep promising solutions as the population. Simply saying, my proposed method is just a mathematical derivation of genetic alogrithms. However, there exists one interesting and novel feature, which is that kept solutions are weighted.
 
Second one is hierarchical mechanism, which is also mathematically derived from the basic model. In EAs, random sampling is carried out in the early stage of optimization and the sampling is concentrated on promising area in the final stage. This is called convergence and this convergence process can be called annealing because the process is related to that of simulated annealing (SA). Annealing is unstable or said to be one directional because if we back to random search from the concentrated search, promising solutions are tend to be discarded in practice like SA. Simply saying, my proposed method, hierarchical importance sampling, is more stable than annealing. The proposed mechanism provides the optimal solution of the 2D Ising model with 400 variables where all variables with the same spin direction is the optimal. I think this setting is more difficult  Ising setting than RANDOM Ising model as optimization problems for EAs and conventional EAs cannot find the optimal solution of this problem as far as I know.
 
Third one is an optimal convergence speed, which is also mathematically derived from the basic model. An interesting point is that entropy is used for an idicator of the search range. An optimal convergence spped can be obtained by Linear reduction of the entropy. Surely, this convergence speed can be directly applied to reinforcement learning and also A/B test algorithms.
 
All the details are described in my doctor thesis. The source code of the algorithms is available from [my github repository](https://github.com/higotakayuki/evolutionary_algorithm)

##Reference to the doctor thesis
Takayuki Higo, "Research on the Importance Sampling Method for Evolutionary Algorithms Based on Probability Models", Doctor Thesis, Tokyo Institute of Technology, 2008.
