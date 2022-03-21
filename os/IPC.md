**管道：~~管道这种通讯方式有两种限制，一是半双工的通信，数据只能单向流动，二是只能在具有亲缘关系的进程间使用。进程的亲缘关系通常是指父子进程关系。~~**


匿名管道使用标准输入和标准输出，单向IPC，父进程打开匿名管道，子进程在管道另一端。双向通信需要两个匿名管道。命名管道以磁盘文件的方式存在，可以在进程生命周期之外持续存在。

~~管道可以分为两类：匿名管道和命名管道。匿名管道是单向的，只能在有亲缘关系的进程间通信；命名管道以磁盘文件的方式存在，可以实现本机任意两个进程通信。~~

**信号**：异步异步地向其他进程或者是同一进程内的线程发送通知。常见的用法是中断、挂起、终止、杀死一个进程。

**~~信号量：信号量是一个~~**~~计数器**，可以用来控制多个进程对共享资源的访问。它常作为一种**锁机制**，防止某进程正在访问共享资源时，其他进程也访问该资源。因此，主要作为进程间以及同一进程内不同线程之间的同步手段。**~~

**消息队列：**（IPC/ITC）允许多个进程读写队列而不需要直接联系其他进程，发布者/订阅者模式的一个变体。

~~消息队列是消息的链接表，包括Posix消息队列和System V消息队列。有足够权限的进程可以向队列中添加消息，被赋予读权限的进程则可以读走队列中的消息。消息队列克服了信号承载信息量少，管道只能承载无格式字节流以及缓冲区大小受限等缺点。~~

**共享内存：**从地址空间中要一块内存，实现进程间的同步和通信。

**~~~~共享内存就是映射一段能被其他进程所访问的内存，这段共享内存由一个进程创建，但多个进程都可以访问。共享内存是最快的 IPC 方式，它是针对其他进程间通信方式运行效率低而专门设计的。它往往与其他通信机制，如信号量，配合使用，来实现进程间的同步和通信。~~~~**

Socket：与其他通信机制不同的是，它可用于不同机器间的进程通信。