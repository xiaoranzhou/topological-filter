# topological-filter
convert 2 way connections to a more structural representation.
__convert 2 way connections to a more structural representation. 
Imagine there is a branched strucutre, you only know there are a lot of points and each points have at least connected to another point. This structure is represented by segment-lines by default, each sement-lines contains connected point1 and point2. Now, you would like to know__ 

**1. how many unique points are there,
2. how many connection each point has,
3. which point is one connected with.

input is a list of two-element-lists. The two-element-lists are consist of node-1 and node-2
output is a tuple, every element of the tuple are id of node, the other node id it connects, the connection id
For example:

input:   
\[  

[1,2],  
[2,3],  
[3,4],  
[3,5],  
[3,6],  
[2,7],  

\]

output:

\[  

[  
[1, 2, 0],  
[4, 3, -2],  
[5, 3, -3],  
[6, 3, -4],  
[7, 2, -5]  
],

[  
[2, 1, 0, 3, 1, 7, 5]  
],

[  
[3, 2, -1, 4, 2, 5, 3, 6, 4]  
]

\]
