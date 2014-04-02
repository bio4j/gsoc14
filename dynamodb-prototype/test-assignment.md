## DynamoDB-backed prototype test assignment

In both tasks we expect you to provide set of tables together with schemata (primary key type). 
In case when hash key calculated according to a hash function, the function should be also provided.

We suggest to carefully read DynamoDB documentation 
(especially [data model](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DataModel.html), 
[workload guideline](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GuidelinesForTables.html#GuidelinesForTables.UniformWorkload) and [API operations](http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_Operations.html)). We **don't** want _code_ at this stage; just a well-thought, detailed design. All the operations should only depend on the number of relationships/edges of the given node.

### Storing a tree

Develop model to store a (huge!) tree with assumptions that all nodes are labeled by numbers from 1 to N (N < 10 ^ 126).

#### Operations:

* get parent node for a node
* get list of descendants for a node

### Storing a twitter-like structure

Develop model to store database with users and relations between them. Every user has: id (a short string), list of blocked users, list of following users.

#### Operations:

* get list of followers of an user
* get list of followed users for an user
* get list of blocked users for an user
