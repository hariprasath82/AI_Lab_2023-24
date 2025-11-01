# Ex.No: 3  Implementation of Minimax Search
### DATE:1.11.2025                                                                            
### REGISTER NUMBER :212223060082 
### AIM: 
Write a mini-max search algorithm to find the optimal value of MAX Player from the given graph.
### Algorithm:
1. Start the program
2. import the math package
3. Specify the score value of leaf nodes and find the depth of binary tree from leaf nodes.
4. Define the minimax function
5. If maximum depth is reached then get the score value of leaf node.
6. Max player find the maximum value by calling the minmax function recursively.
7. Min player find the minimum value by calling the minmax function recursively.
8. Call the minimax function  and print the optimum value of Max player.
9. Stop the program. 

### Program:
 # Using a Python dictionary to act as an adjacency list
 
 
 graph = {
 
 '5' : ['3','7'],
 
 '3' : ['2', '4'],
 
 '7' : ['8'],
 
 '2' : [],
 '4' : ['8'],
 
 '8' : []
 
 }
 
visited = set() # Set to keep track of visited nodes of graph.

 def dfs(visited, graph, node): #function for dfs
 
 if node not in visited:
 
 print (node)
 
 visited.add(node)
 
 for neighbour in graph[node]:
 
 dfs(visited, graph, neighbour)
 
 # Driver Code
 print("Following is the Depth-First Search")
 dfs(visited, graph, '5')
 
outtput: 

<img width="852" height="281" alt="image" src="https://github.com/user-attachments/assets/22c73b6b-e82c-4679-978d-89bcf150d5da" />



### Result:
Thus the optimum value of max player was found using minimax search.
