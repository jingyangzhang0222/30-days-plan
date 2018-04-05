# 20180405 DSA Lecture Notes
-----------

## REVIEW(cont'd):  ##

 - **DFS:acyclic directed graph yields no back edges**

DFS:acyclic directed graph yields no back edges
proof:
→: (u,v) is a back edge, v is  an ancestor of u, there is a path form v to u, the n there is a cycle;
←: suppose there is a cycle, v discovered first, at the time of d(v), all v in the cycle is white, from a white path from v to u, then u become a descendant of v, (u,v) is a back edge.

 - **Directed Acyclic Graphs**
 -A DAG is a directed graph that contains no directed cycles
 -A topological order/topological sort of a DAG G = (V, E) is an ordering of its nodes as v1, v2, …, vn so that for every edge (vi, vj) we have i < j.

 - **Precedence Constraints**
 -Edge (vi, vj) means task vi must occur before vj.

 - **Compute Topological Sort: Algorithm**
1. call DFS(G) to compute finishing times f(v) for each vertex v
2. as each vertex is finished, insert it onto the front of a linked list
3. return the linked list of vertices
 
 - **Analysis**
1. call DFS(G) to compute finishing times f(v) for each vertex v
2. as each vertex is finished, insert it onto the front of a linked list
3. return the linked list of vertices

- Running time for topological sort: Θ(V + E)
- depth-first search takes Θ(V + E) time‚
- it takes O(1) time to insert each of the |V| vertices onto the front of the linked list.

