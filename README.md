# Bibliography

> Model-based Optimization, see for more detail notes on [Reading_Notes](./Reading_Notes.md)

Contributed by Genghui Li, Fei Liu and Liang Zhao.




# Table of contents

- [Sruvey about Simulation-based Optimization ](#Survey paper)







## [Sruvey about Simulation-based Optimization](#Table-of-contents)

### Survey

- **`Open Issues`** [Open Issues in Surrogate-Assisted Optimization](https://link.springer.com/chapter/10.1007/978-3-030-18764-4_10), J. Stork **`(2020)`** **`[Book:High-Performance Simulation-Based Optimization ]`**


This chapter discusses some open issues in surrogate-assisted optimization.  The main open issues are:

1.Construct an adequate set of Benchmark or test functions 

2.Constraint handling 

3.Surrogate ensemble

**`4.Combinatorial/discrete search space`**

5.Multiobjective optimization problems

6.Dynamic problems

7.Noisy problems

8.High dimensional problems

To the best of my knowledge, there are only a few algorithms to solve expensive discrete optimization problems (EDOPs). However, EDOPs frequently arise in real-world applications. Therefore, developing effective algorithms to deal with EDOPs is an interesting research direction.   

### Methods 

- **`IOU-C`** [Input-output Uncertainty Comparisions for discrete Optimization via Simulation](https://pubsonline.informs.org/doi/pdf/10.1287/opre.2018.1796), E. Song**`(2019)`** **`[Operations Research]`**

A new concept: input model risk that when we make decisions based on the simulation outputs, we are subject to the risk of making suboptimal decisions when the input models do not faithfully represent the real-world stochastic process.

This paper aims to compare $k$ systems, where the $i$-th system's performance measure is its simulation output mean ($E[\Upsilon_{i}(F^{c}_{i})]$) , under real-world input distribution $F^{c}_{i}$($c$ mean correct), where $\Upsilon_{i}()$ is the output performance that depends on the chosen input distribution.  The specific goal is to find $\arg \min_{i}E[\Upsilon_{i}(F^{c}_{i})]$ with a statistical guarantee (e.g., 95%) that the selected system is the real-would optimal. 

However, in most cases $F^{c}_{1},\cdots, F^{c}_{k} $ are unknown, which force to use $\hat{F_{1}},\cdots,\hat{F_{k}}$ to run simulations and use $E[\Upsilon_{i}(\hat{F_{i}})|\hat{F_{i}}]$ instead of $E[\Upsilon(F^{c}_{i})]$ to evaluate the $i$-th system's performance. Typically, $\hat{F_{i}}$ is estimated from finite real-world observations from $F^{c}_{i}$ and therefor is subject to estimation error. Thus, the conditional optimal $\arg\max_{i}E[\Upsilon_{i}(\hat{F_{i}})|\hat{F}_{i}]$ may not be the same as $\arg\max_{i}E[\Upsilon_{i}(F^{c}_{i})]$. 

This paper shows that it is possible to provide a meaningful statistical guarantee with respect to the real-world optimal, rather than the conditional optimal.

