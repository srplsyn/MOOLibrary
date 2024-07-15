MULTIOBJECTIVE OPTIMIZATION LIBRARY

This page contains source codes and test problems for Multiobjective Optimization Problems, originally shared at http://home.ku.edu.tr/~moolibrary.  

TEST INSTANCES FOR MULTIOBJECTIVE DISCRETE OPTIMIZATION PROBLEMS

Three classes of test problems are used to generate random instances for multiobjective discrete optimization (MODO) problems. The test problems are

	1.	Multiobjective knapsack problem 
 
	2.	Multiobjective assignment problem
 
	3.	Multiobjective integer linear programming problem. 
 
Refer to the publications cited below for the details of the data generation scheme. The document testproblems.pdf also contains a brief summary.

The multiobjective knapsack and assignment problems were first generated and used in Kirlik, G., & Sayın, S. (2014). A new algorithm for generating all nondominated solutions of multiobjective discrete optimization problems. European Journal of Operational Research, 232(3), 479-488.

The multiobjective integer linear programming problems test problems were first generated and used in  Kirlik, G., & Sayın, S. (2015). Computing the nadir point for multiobjective discrete optimization problems. Journal of Global Optimization, 62, 79-99.


GENARATING ALL NONDOMINATED SOLUTIONS FOR MULTIOBJECTIVE DISCRETE OPTIMIZATION PROBLEMS

The method given in Kirlik, G., & Sayın, S. (2014), "A new algorithm for generating all nondominated solutions of multiobjective discrete optimization problems," European Journal of Operational Research, 232(3), 479-488,  generates all nondominated solutions for multiobjective discrete optimization problems with any number of objective functions. The 
source code of the algorithm with Makefile are available and can be  used free of charge for academical purposes. The code utilize IBM ILOG's CPLEX solver for subproblems.




