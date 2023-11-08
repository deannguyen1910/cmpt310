# Markov Decision Processes
* An MDP is defined by:
    * A set of s  S
    * A set of actions a 
    * A transition function T(s, a, s')
        * Probability that a from s leads to s’, i.e., P(s’| s, a)
        * Also called the model or the dynamics

        * a: action
        * s: state 
![](../images/MDPs_equation.png)
## Example 1:
![](../images/MDPs_carExample.png)
* Iteration 0 
    * ![](../images/MDPs_carExample0.png)
* Iteration 1
    * At Cool
        * Q*(Cool, slow)
            * 1.0 (1 + 0) = 1, s' = Cool
        * Q*(Cool, fast)
            * 0.5 (2 + 0) = 1, s' = Warm
            * 0.5 (2 + 0) = 1, s' = Cool
            * Sum -> 2
        * --> 2, fast At Cool, V1 
    * At Warm 
        * Q*(Warm, Slow)
            * 0.5 (1 + 0) = 0.5, s' = Warm
            * 0.5 (1 + 0) = 0.5, s' = Cool
            * Sum -> 1
        * Q*(Warm, fast)
            * 1.0 (-10 + 0) = -10, s' = Overheated
        * --> 1, slow At Warm V1
    * At Overheated
        * No action -> 0
    * ![](../images/MDPs_carExample1.png)
* Iteration 2
    * At Cool
        * Q*(Cool, slow)
            * 1.0 (1 + 2) = 3, s' = Cool
        * Q*(Cool, fast)
            * 0.5 (2 + 1) = 1, s' = Warm
            * 0.5 (2 + 2) = 1, s' = Cool
            * Sum -> 3.5
        * --> 3.5, fast At Cool, V2
        * At Warm 
            * Q*(Warm, Slow)
                * 0.5 (1 + 1) = 1.0, s' = Warm
                * 0.5 (1 + 2) = 1.5, s' = Cool
                * Sum -> 2.5
            * Q*(Warm, fast)
                * 1.0 (-10 + 0) = -10, s' = Overheated
            * --> 2.5, slow At Warm V2
        * At Overheated
            * No action -> 0
        * ![](../images/MDPs_carExample2.png)
        * 
        * 
        * Sum up,
        * ![](../images/MDPs_carExample0-2.png)
## Example 2:
