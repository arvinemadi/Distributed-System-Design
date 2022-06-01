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

