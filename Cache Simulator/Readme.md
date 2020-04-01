Cache is a special type of memory providing very small latency for accessing. The basic idea of using cache is to keep recently used data close to processors. So, modern processors use small cache along with large main memory. Program performance depends on the cache performance. If data is found in cache (Hit), execution can proceed normally. On the other hand if data is not found in cache, execution stalls until that data is fetched from main memory. Computer architects always looks for miss rate of cache (# of misses per 100 accesses). When a miss occurs, the new data is kept in the cache and some existing data is removed from cache. There are several policies to select which one to evict. A common technique used in any computer systems is LRU (Least Recently Used). According to this scheme, the data that has not been used for longest time is evicted. Let us explain how this scheme works Assume a cache with 4 entries. So, if the processor accesses data 1, 2, 3, 4, 5, 2, 3, 99, 2, 5, 4 the following things will occur
Here for 11 data references, we have 7 misses. In this problem you have to find the number of misses for different cache sizes. You will be given data references in several ways

a) ADDR x: Processor will access data x

b) RANGE b y n: Processor will access all data references in the form b + y ∗ k, where k is 0 to n − 1

Your will also be given commands STAT to print the number of misses for each cache (excluding the misses occurred before last STAT command).