# SLAB-ALLOCATOR SUPPORTING PARALLEL ALLOCATIONS
The design of the slab allocator is referred from the linux slab allocator.
The slab allocator supports parallel allocations using semaphores. Semaphores are used to allow mutual exclusive access to the buckets of required sizes. 
Two threads can allocate a memory size of two different bucket types parallely.

The buckets range from 4 bytes to 8196 bytes increasing with multiple of 2.

Best fit algorithm is used to search for buckets that can suppot  the memory size requirement 
