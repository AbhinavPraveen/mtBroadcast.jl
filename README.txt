A trivial implementation of multithreaded broadcasting in julia.


    mtB(f,x...[; n = Threads.nthreads()])

Applies the function 'f' to the varargs 'x...' using 'n' threads and returns the output.


    mtBcall(f,x...[; n = Threads.nthreads()])

Assigns 'n' threads to apply the function 'f' to the varargs 'x...' and returns the generated task objects. You may wait.() or fetch.() these objects. This is significantly faster than mtB() if the task objects can be handled efficiently.
