# JVM

JVM（Java Virtual Machine）也叫Java虚拟机，它提供了Java运行时（严格来讲，能运行在JVM里面的不止是Java代码，我了解到的还有Kotlin、Groovy、Scala等）的环境来驱动Java代码或应用程序，它将Java字节码转为机器语言，它是Java运行时环境（JRE的一部分）</br>
按照《Java虚拟机规范》，Java虚拟机其实有很多的实现，我们最常见的就是HotSpot了，这也是目前官方默认的Java虚拟机。通过阅读周志明的《深入理解Java虚拟机》了解到HotSpot经过很多年的发展，吸收了很多其他虚拟机的优点，逐渐发展成为今天的默认虚拟机</br>
我们学到的JVM内存结构，其实就是在加载字节码的时候，在JVM里面划分了很多的区域，其中我们讨论最多的应该就是堆和栈；栈是线程私有的，堆是线程共有的，我们平时说的JVM调优其实主要调的就是JVM里面的堆，根据JVM里面的内存模型和各种GC收集器的特点，通过一些参数等控制垃圾回收的策略和行为等，来达到让我们的应用程序更加稳定健康的运行的目的。