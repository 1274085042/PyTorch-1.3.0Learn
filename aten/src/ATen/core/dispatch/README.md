This folder contains the c10 dispatcher. This dispatcher is a single point
through which we are planning to route all kernel calls.
Existing dispatch mechanisms from legacy PyTorch or caffe2 are planned to
be replaced.
此文件夹包含c10 dispatcher，通过它路由所有的内核调用

This folder contains the following files:
- Dispatcher.h: Main facade interface. Code using the dispatcher should only use this.
                主要的接口文件
- DispatchTable.h: Implementation of the actual dispatch mechanism. Hash table with kernels, lookup, ...
                   dispatch机制的实现
- KernelFunction.h: The core interface (i.e. function pointer) for calling a kernel
                    调用kernel的核心接口（函数指针）
