Memory:
1 bit takes 6 transistors
1 byte = 48 transistors
So to support 1MB of memory, it requires 48,000,000 transistors. That's why the closer cache is to the core, the smaller the size is; L1 is being the smallest as it's closest.


Depending on the architecture, but everytime a core is interacting with main memory, it is fetching 64 byte at a time. Hence even the loop is 1/8th of the other, it's still traversing the same number across the Northbridge to the memory and back. 
ONLY when it's 1/32nd of the other that you can see the difference as it's fetching data from and to the memory less.

Conclusion:
1) Java environment is a very noisy env. This is the consequence of a managed system (with JVM)
2) You need to be aware of the actual work is when you're measuring performance. In this case, the real work is not the number of iteration, but the travel time to and from the main memory.

