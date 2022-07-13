## Examples of distributed system design solution

### Ride sharing App
Additional note:
- the map could be created with a tree. This will be needed to make the size of each cell of area adaptive.
- Two type of persistent connections: 1- long polling 2- web sockets

### Top K heavy hitters
- This is a general problem that can be stated in different system design questions. For example, desiging a spam detection system, or most traded stocks.
- Depending on more specific requirements, different paths to the DB can be included or removed.

More information:
- https://www.americanscientist.org/article/the-britney-spears-problem
- https://www.youtube.com/watch?v=kx-XDoPjoHw

### Design Twitter:
The focus of this system design was on NewsFeed generation and scalibility for a read heavy system. Trending topics is covered in 'Top-K heavy hitters' and search for key word would be added separately.

### Time Series DB:
Functional and non-Functional requirements can vary. The focus was on the concept of hot to store so that both write and reads can be done efficiently. The concept is similar to LSM (Log-Structured Merge Tree) but instead of arranging/sort based on the key, we can arrange/sort based on time.

- Intro to LSM based DBs: https://www.youtube.com/watch?v=P2xtlLymqqI
- InfluxDB lecture with more details: https://www.youtube.com/watch?v=2SUBRE6wGiA

### Global Distributed Counter:
Example of Functional and non-Functional requirements are shown in the final. 
The simple proposed system design based on Conflict-Free Replicated Data Type (CRDT).
CRDT can be used in other similar problems:
- Counting with both increments and decrements (need one array for increment and one for decrements)
- Distributed leader-less key-value stores
- Sets (a bit more tricky)
- Sequences

More info: https://arxiv.org/pdf/1307.3207v1.pdf

### Data Control and Retrieval System
We have a big cluster with thousands of machines each of which is emitting hundreds of statistics per second.
You can think that each statistic is represented by the tuple [host-name, metric-name, value].
We want to be able to collect and aggregate those tuples in a scalable manner. The main consumers for this system are:
- A graphing system - For a certain metric-name, plot a set of host-names from time t1 to t2
e.g. Memory usage of host-1, host-2, host-3 for the past week
- An alerting system- Issue an alert (email, etc) when a certain metric-name goes above/below a certain threshold
e.g. Memory usage for host-1 goes above 70% for 5 minutes

The system uses concepts from time series DB and also top heavy hitters.

### WhatsApp system design
The diagram shows high level system design for any chat system.

### Cloud storage system design
Design a system similar to AWS S3 with these requirements:

● Durability: 11 - 9 (99.9999..%)

● Availability 99.99%

● multi-tendency 

● Scalable

● Region Specific Bucket




