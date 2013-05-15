Graph Algorithm:

In this problem we are solving the single-source all pairs shortest path using MapReduce using parallel Breadth-First Search (BFS) in an iterative manner. The source node is '1'. The source node is processed first, then the nodes connected to the source node are processed and so on.

Input format :
source<tab>adjacency_list:distance_from_the_source:

Termination Condition:
Check the output value with the previous input if any of the distance is still infinity(125 in our code) the continue else convergence is reached and stop

Algorithm:
Step1: Input file having structure as node id and corresponding adjacency list
Step2: Mapper read the file line by line and emit distance of corresponding adjacency list nodes from this node.
Step3: Reducer find the minimum of the distance of all the distances of a given node.
Step4: This output file is again read and stored in the map function to check if convergence is reached.
	   if convergence is reached
			stop;
	   else
			repeat step1 with this output file as input file.
			