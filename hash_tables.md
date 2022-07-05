## Hash Tables
1. Key:Value pairs
    - Value is stored at a memory address generated by running the key through a hash function
    - Both key and value are stored in same memory address
2. Hash Function
    - A function that generates a value of fixed length for each input it is given
    - 'One-way'
	* When a hash is created, it cannot be reverse engineered to get the original key
    - Idempotence
	* When given the same input, the function will ALWAYS return the same output
	* '1234' =[HASH]> '4321' x 1000 => '4321'
    - Speed depends on computational difficulty to use hash function
	* The more computation is needed to generate a hash, the more secure that hashing is. 
	* The more computation needed, the slower the hash, so usually reserved for encryption, security, etc. 
3. Performance
    - Insert
	* O(1)
    - Lookup
	* O(1)
    - Delete
	* O(1)
    - Search
	* O(1)
    * Since items are stored based on a simple hash of a key, no iteration is needed to locate them, add them, or remove them
4. Hash Collisions
    - Since computer memory is limited, it is possible for a hash function to generate the same memory address twice, thus storing 2 or more things in the same space
    - Key and value are stored in memory in 'buckets'
    - When two pieces of data are added to a memory space, a linked list is formed: MEMORY[item1 => item2]
    - Collisions can cause lookups / search to become O(n) operations, given a linked list may need to be traversed