# Parallelization-of-FLoyd-Warshall-Algo-using-MPI
Parallel and Distribute Computing Project 
Floyd Warshall algorithm is All Pair Shortest Path finder. It is mainly used to overcome the drawbacks of Dijkstra’s and Bellman Ford Algorithms. 
It considers negative weight present in the graph. In the Floyd Warshall algorithm every node of the graph is visited and the shortest path is computed.
Calculatee intermediate vertex.
If the direct distance from the source to the destination is greater than the path through the vertex, then the distance through the vertex will be considered.
Let k be the intermediate vertex. And i,j be the source and the destination respectively.
Then A[i][j] if filled with:
   (A[i][k]+A[k][j]) if (A[i][j]> A[i][k]+A[k][j] )
When calculating the distance from source to all the other vertices through a certain vertex, they are independent of the other sources.
Hence, for every intermediate vertex matrix,  open MPI is applied  from every source vertex to their respective destinations parallelly.
For large data sets, the parallel version of Floyd-Warshall Algorithm could have huge speed up benefits over the sequential one.

