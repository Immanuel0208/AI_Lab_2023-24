# Ex.No: 1  Implementation of Breadth First Search 
### DATE:                                                                            
### REGISTER NUMBER : 212221060230
### AIM: 
To write a python program to implement Breadth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function bfs and take the set “visited” is empty and “queue” is empty
4. Search start with initial node and add the node to visited and queue.
5. For each neighbor node, check node is not in visited then add node to visited and queue list.
6.  Creating loop to print the visited node.
7.   Call the bfs function by passing arguments visited, graph and starting node.
8.   Stop the program.
### Program:
```
graph = {
  '2': ['3', '4'],
  '3': ['5'],
  '4': ['6', '7'],
  '6': [],
  '5': ['6'],
  '7': ['8'],
  '8': []
}

visited = []  
queue = []    

def bfs(visited, graph, node): 
    visited.append(node)
    queue.append(node)

    while queue:  
        m = queue.pop(0)
        print(m, end=" ")

        for neighbour in graph[m]:
            if neighbour not in visited:
                visited.append(neighbour)
                queue.append(neighbour)


print("BFS order is")
bfs(visited,graph,'2')
```
### Output:
<img width="100" alt="Screenshot 2024-02-17 210240" src="https://github.com/DrUmaRaniV/AI_Lab_2023-24/assets/123659657/3040ea67-f9cc-456e-89cb-7da10a83a100">



### Result:
Thus the breadth first search order was found sucessfully.
