# 关于 JVM

JVM 是整个 Java 平台的基石，实现硬件与操作系统无关，编译代码后生成出极小体积，保障用户机器免于恶意代码损害。

JVM 可以看作是一台抽象的计算机。跟真实的计算机一样，它有自己的指令集以及各种运行时内存区域。使用虚拟机来实现一门程序设计语言有许多合理的理由，业界中流传最为久远的虚拟机可能是 UCSD Pascal 的 P-Code 虚拟机。

第一个 JVM 的原型机是由 Sun 公司实现的，它被用在一种类似 PDA（Personal Digital Assistant，俗称掌上电脑）的手持设备上仿真实现 JVM 指令集。时至今日，Oracle 已有许多 JVM 实现应用于移动设备、桌面电脑、服务器等领域。JVM 并不局限于特定的实现技术、主机硬件和操作系统。它不强求使用解释器来执行程序，也可以通过把自己的指令集编译为实际 CPU 的指令来实现，它可以通过微代码来实现，或者甚至直接实现在 CPU 中。

JVM 与 Java 语言并没有必然的联系，它只与特定的二进制文件格式 class 文件格式所关联。class 文件中包含了 JVM 指令集（或者称为字节码、bytecodes）和符号表，还有一些其他辅助信息。

基于安全方面的考虑，JVM 要求在 class 文件中使用了许多强制性的语法和结构化约束，但任一门功能性语言都可以表示为一个能被 JVM 接收的有效的 class 文件。作为一个通用的、机器无关的执行平台，任何其他语言的实现者都可以将 JVM 作为他们语言的产品交付媒介。

这里指定的 JVM 是与 Java SE 8 平台兼容，并支持 [《Java 语言规范（Java SE8版）》](http://docs.oracle.com/javase/specs/jls/se8/html/index.html)中指定的 Java 编程语言。