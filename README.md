# Reinforcement-Learning-Final-Project
https://www.youtube.com/watch?v=jkV-lQlrISA&amp;t=314s

Project Assumption:
Zhang San is a bookstore owner. He plans to open several bookstores in Macao. After investigation, it is found that the people who love reading in Macao mainly live in the 50 buildings selected above. Zhang San should consider where the bookstore would be most conducive to the operation of the bookstore in Macao. Therefore, the number of bookstores and the location relationship between bookstores and buildings can effect the operation of the bookstores. At the same time, he has two trucks for incoming goods, and needs to design an optimal distribution route.

# The Challenges of this project and the main solutions
This experiment solves these problems through clustering and path planning.

# Clustering
Select the number of cluster centers according to the number of bookstores, and each bookstore serves the users of buildings belonging to the cluster. The project using Kmeans algorithm to divided 50 buildings into 5 categories. Therefore, the 5 cluster centers are the location of bookstores.

# Path planning
Intra-class
The location of each bookstore should consider the shortest path of such buildings. The TSP problem implemented by greedy algorithm is used for path planning. The buildings in each category will be formed into a shortest route.

Inter-class
This project entails transporting goods from the port of entry to each bookstore. It will be solved by ortools library. The output is the weight to be carried by each vehicle and the distribution routes.

# Conclusion
From the configuration results, it is clear that there are two trucks here, each with a loadable capacity of 60, and the amount of goods demanded by each bookstore is 20.
Starting from the port of entry, the two trucks distribute the goods according to the routes of (0->1->3->2->0) and (0->5->4->0) respectively. The first truck is loaded with 60 capacity and send goods to the 1st, 3rd and 2nd bookstores in turn. The total distance of route is 26733m. The second truck is loaded with 40 capacity and send goods to the 5th and 4th bookstores in turn. The total distance of route is 4288m.
