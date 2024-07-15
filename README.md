MULTIOBJECTIVE OPTIMIZATION LIBRARY
This page contains source codes and test problems for Multiobjective Optimization Problems.  



TEST INSTANCES FOR MULTIOBJECTIVE DISCRETE OPTIMIZATION PROBLEMS
Three classes of test problems are used to generate random instances for multiobjective discrete optimization (MODO) problems. The test problems are
	1.	Multiobjective knapsack problem 
	2.	Multiobjective assignment problem
	3.	Multiobjective integer linear programming problem. 
The multiobjective knapsack and assignment problems are generated in [Kirlik, G. and Sayın, S., A new algorithm for generating all nondominated solutions of multiobjective discrete optimization problems, European Journal of Operational Research, vol 232(3), 2014, pp. 479-488.] These test problems are used to compare different algorithms on generating nondominated solutions for MODO problems. The multiobjective integer linear programming problems test problems are created in  [Kirlik, G. and Sayın, S., Computing nadir point for multiobjective discrete optimization problems, Working Paper, 2014] to compare nadir point determination algorithms.
Multiobjective Knapsack Problems (download)
The multiobjective knapsack problem consists of $n$ objects, $r^{th}$ object in the knapsack has a positive integer weight $w_r$ and $p$ non-negative integer profits $v_{jr}$ where $p$ represents number of objective functions. The knapsack has a positive integer capacity $W$. Decision variable $x_r$ denotes whether item $r$ is selected for the knapsack or not.
\begin{align} \max & \sum_{r=1}^n v_{jr} x_r \quad j=1, \ldots, p \\ \mbox{s.t.} & \sum_{r=1}^{n} w_r x_r \le W \\ & x_r \in \{0, 1\} \quad r=1, \ldots, n \end{align} 
The multiobjective knapsack problem instances are generated for $p=3$, $4$ and $5$ cases, and $v_{jr}$ and $w_r$ are random integers drawn from the interval $[1, 1000]$ where $j \in \{1, \ldots, p\}$ and $r \in \{1, \ldots, n\}$. The capacity of the knapsack is calculated as $W = \left \lceil 0.5 \left(\sum_{j=1}^n w_j \right) \right \rceil$. The total number of data files for the multiobjective knapsack problem is $160$. $100$, $40$ and $20$ of the instances have $p=3$, $p=4$ and $p=5$ numbers of objective functions, respectively. The data file names are given in the following format, "KP_p-X_n-Y_ins-Z.dat." KP stands for the knapsack problem, X represents the number of objective functions, Y shows the number of objects, and Z is the instance number. The format of each data file is:
	•	Number of objective functions $(p)$.
	•	Number of objects $(n)$. 
	•	Capacity of the knapsack $(W \in \mathbb{Z})$.
	•	Profits of the objects in each objective function, $\mathbb{Z}^{p \times n}$.
	•	Weights of the objects $(w \in \mathbb{Z}^n)$.
 
Multiobjective Assignment Problems (download)
The assignment problem aims to obtain optimal assignments between a set of agents $r \in \{1,\ldots,n\}$ and a set of tasks $l \in \{1,\ldots,n\}$ where each assignment has a non-negative cost $c_{jrl}$.
\begin{align} \min & \sum_{r=1}^n \sum_{l=1}^n c_{jrl} x_{rl} \quad j=1, \ldots, p \\ \mbox{s.t.} & \sum_{l=1}^{n} x_{rl} = 1 \quad r=1, \ldots, n \\ & \sum_{r=1}^{n} x_{rl} = 1 \quad l=1, \ldots, n \\ & x_{rl} \in \{0, 1\} \quad r=1, \ldots, n; \; l=1, \ldots, n \end{align} 
Test problem instances for the multiobjective assignment problem are formed in sizes varying from $5$ to $50$ with increments of $5$ and $p=3$. The objective function coefficients are generated randomly in the interval $[1,20]$, and all are integers. The total number of data files for the multiobjective assignment problem is $100$. The data file names are given in the following format, "AP_p-X_n-Y_ins-Z.dat." AP stands for the assignment problem, X represents the number of objective functions, Y shows the number of tasks, and Z is the instance number. The format of each data file is:
	•	Number of objective functions $(p)$.
	•	Number of tasks $(n)$.
	•	Cost of the assignment $(c \in \mathbb{Z}^{p \times n \times n})$.
 
Multiobjective Integer Linear Programming Problems (download)
In multiobjective integer linear programming (MOILP) problems, $m$ and $n$ represent the number of constraints and number of variables, respectively, and $x \in \mathbb{R}^n$ is the decision vector of the problem. Given coefficients of the objective functions $c_{jl}$, the technical coefficients $a_{rl}$, and right-hand side values $b_{r}$ where $r \in \{1,\ldots,m\}$, $l \in \{1,\ldots,n\}$ and $j \in \{1,\ldots,p\}$.
\begin{align} \max & \sum_{l=1}^n c_{jl} x_l \quad j=1, \ldots, p \\ \mbox{s.t.} & \sum_{l=1}^n a_{rl} x_l \le b_r \quad r=1, \ldots, m \\ & x_l \ge 0 \mbox{ and integer} \quad l=1, \ldots, n. \end{align} 
We consider MOILP problems with $p=3,4$ and $5$, $m=5,10,\ldots,50$ and $n=2m$ for each $m$. The coefficients of the objective functions $(c_{jl})$ are generated in the ranges $[-100,-1]$ with probability $0.2$ and $[0,100]$ with probability $0.8$. The technical coefficients $(a_{rl})$ are generated in the ranges $[-100,-1]$ with probability $0.1$, $[1,100]$ with probability 0.8, and $a_{rl}=0$ with probability 0.1. Right-hand side value of each constraint $(b_r)$ is generated randomly in the range of $100$ and $\sum_{l=1}^n a_{rl}$. The total number of data files for the MOILP is $220$. $100, 80$ and $40$ of the instances have $p=3$, $p=4$ and $p=5$ numbers of objective functions, respectively. The data file names are given in the following format, "ILP_p-U_n-X_m-Y_ins-Z.dat." ILP stands for the integer linear programming, U represents the number of objective functions, X and Y show the number of columns (decision variables) and rows (number of constraints) respectively, and Z is the instance number. The format of each data file is:
	•	Number of objective functions $(p)$.
	•	Number of columns $(n)$.
	•	Number of rows $(m)$.
	•	Coefficients of the objective functions $(c \in \mathbb{Z}^{p \times n})$.
	•	Technical coefficients, $(a \in \mathbb{Z}^{m \times n})$.
	•	Right-hand side values, $(b \in \mathbb{Z}^m)$.

Note: According to random MOILP generation scheme, it is possible for a generated MOILP instance to have an unbounded efficient set. Among all ILP instances, only the instance named "ILP_p-5_n-10_m-5_ins-1.dat" has an unbounded efficient set.
GENARATING ALL NONDOMINATED SOLUTIONS FOR MULTIOBJECTIVE DISCRETE OPTIMIZATION PROBLEMS
This method generates all nondominated solutions for multiobjective discrete optimization problems with any number of objective functions. In this algorithm, the search is managed over $(p-1)$-dimensional rectangles where $p$ represents the number of objectives in the problem. For each rectangle, two-stage optimization problems are solved such that the first-stage is well-known $\varepsilon$-constraint scalarization. It is showed that algorithm enumerates all nondominated solutions of MODO problems in finite number iterations [Kirlik, G. and Sayın, S., A new algorithm for generating all nondominated solutions of multiobjective discrete optimization problems, European Journal of Operational Research, vol 232(3), 2014, pp. 479-488]. 
Source code of the algorithm with Makefile and sample data files can be downloaded from this link (download) and used free of charge for academical purposes. The code utilize IBM ILOG's CPLEX solver for subproblems [web]. (Cplex 12.6.3 users should use this version of the source code download) Software documentation of the implemantation is generated by using Doxygen and avaiable in this link.
27 Mar 2014 23:20


GOKHANKIRLIK@GMAIL.COM © LAST UPDATED: OCTOBER 2016






