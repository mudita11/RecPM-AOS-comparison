# RecPM-AOS-comparison

Comparison of three Adaptive Operator Selection methods within Differential Evolution, RecPM-AOS, PM-AdapSS and F-AUC.

Algorithms are tested on BBOB test suite on dimension 20.

**Notations** 

DE-RecPM-AOS or RecPM: Recursive Probability Matching Adaptive Operator Selector within Differential Evolution

DE-F-AUC(-R) or FAUC(-R): Bandit with Area Under the curve within Differential Evolution without replication(best replication from thesis: Adaptive Operator Selection for Optimisation)

PM-AdapSS-DE(-R) or AdapSS(-R): Probability Matching Adaptive Operator Selector within Differential Evolution without replication(best replication from thesis: Fialho, Álvaro. Adaptive operator selection for optimization. Diss. Université Paris Sud-Paris XI, 2010.)

CMAES: Covariance Matrix Adaptation Evolution Strategy

JADE: Adaptive Differential Evolution With Optional External Archive

RecPM, FAUC and AdapSS have three versions (Please note in the following "Algo" can be replaced by name of the algorithm): 

Algo1: Parameters of AOS and DE are tuned using IRACE.

Algo2: Parameters of only AOS method are tuned; Parameter values for DE algorithm: CR (Crossover rate) = 1.0, F (Mutation rate) = 0.5, NP (Population size) = 200

Algo3: Parameter values for DE algorithm: CR (Crossover rate) = 1.0, F (Mutation rate) = 0.5, NP (Population size) = 200; Parameter values for AOS method: alpha (Adaptation rate) / gamma (Discount factor) = 0.6, p_min (Minimum probability attainable by any operator) = 0.0, W (Window size) = 50, C (Scaling factor) = 0.5


**Folder description**

- Replicated

Shows data generated by various algorithms on BBOB test suite: CMAES, JADE, DE-RecPM-AOS and replicated versions of DE-F-AUC and PM-AdapSS-DE denoted as DE-F-AUC-R and PM-AdapSS-DE-R respectively. Data to generate results (graphs and tables) for CMAES and JADE algorithm is taken from coco website (http://coco.gforge.inria.fr/doku.php?id=algorithms-bbob). 

Three algorithms with AOS method (DE-RecPM-AOS, DE-F-AUC and PM-AdapSS-DE) are tuned and each of their three variants are presented.

output-all contains all the ECDFs and tables for all algorithms mentioned in this folder whereas output-AOS only compares algorithms involving AOS methods that is there is no CMAES and JADE results.

The purpose of output-AOS folder is to clearly give the reader a comparison between the convergence speeds (aRT shown in table)of algorithms involving AOS methods.


- Existing

Shows data generated by various algorithms on BBOB test suite: CMAES, JADE, DE-RecPM-AOS, DE-F-AUC and PM-AdapSS-DE. Data for CMAES, JADE and latter two algorithms is taken from coco website (http://coco.gforge.inria.fr/doku.php?id=algorithms-bbob).   

Only DE-RecPM-AOS algorithm is tuned and its three variants are presented. 

## Reference
If you use this repository, please cite the following paper:
```
@inproceedings{sharma2018performance,
  title={Performance Assessment of Recursive Probability Matching for Adaptive Operator Selection in Differential Evolution},
  author={Sharma, Mudita and L{\'o}pez-Ib{\'a}nez, Manuel and Kazakov, Dimitar},
  booktitle={International Conference on Parallel Problem Solving from Nature},
  pages={321--333},
  year={2018},
  organization={Springer}
}
```
