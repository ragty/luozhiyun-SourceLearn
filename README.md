此仓库会归档所有一些我的源码学习文章。最新的文章会发布在我的博客中：https://www.luozhiyun.com
如果觉得不错的话，记得点个start，感谢~



## 深入k8s（kubernates）源码分析

一开始的时候并没有想过会写这么多，以及会有勇气去翻阅k8s写源码分析，毕竟k8s我们会使用就已经不错了，所以第二篇和第三篇没有加上源码分析，后面再补上。

[Docker容器实现原理](%E6%B7%B1%E5%85%A5k8s/Docker容器实现原理.md)

[1.深入k8s：在k8s中运行第一个程序](%E6%B7%B1%E5%85%A5k8s/1.%E6%B7%B1%E5%85%A5k8s%EF%BC%9A%E5%9C%A8k8s%E4%B8%AD%E8%BF%90%E8%A1%8C%E7%AC%AC%E4%B8%80%E4%B8%AA%E7%A8%8B%E5%BA%8F.md)

[2.深入k8s：Pod对象中重要概念及用法](%E6%B7%B1%E5%85%A5k8s/2.%E6%B7%B1%E5%85%A5k8s%EF%BC%9APod%E5%AF%B9%E8%B1%A1%E4%B8%AD%E9%87%8D%E8%A6%81%E6%A6%82%E5%BF%B5%E5%8F%8A%E7%94%A8%E6%B3%95.md)

[3.深入k8s：Deployment控制器](%E6%B7%B1%E5%85%A5k8s/3.%E6%B7%B1%E5%85%A5k8s%EF%BC%9ADeployment%E6%8E%A7%E5%88%B6%E5%99%A8.md)

[4.深入k8s：持久卷PV、PVC及其源码分析](%E6%B7%B1%E5%85%A5k8s/4.%E6%B7%B1%E5%85%A5k8s%EF%BC%9A%E6%8C%81%E4%B9%85%E5%8D%B7PV%E3%80%81PVC%E5%8F%8A%E5%85%B6%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90.md)

[5.深入k8s：StatefulSet控制器及其源码分析](%E6%B7%B1%E5%85%A5k8s/5.%E6%B7%B1%E5%85%A5k8s%EF%BC%9AStatefulSet%E6%8E%A7%E5%88%B6%E5%99%A8%E5%8F%8A%E5%85%B6%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90.md)

[6.深入k8s：守护进程DaemonSet及其源码分析](%E6%B7%B1%E5%85%A5k8s/6.%E6%B7%B1%E5%85%A5k8s%EF%BC%9A%E5%AE%88%E6%8A%A4%E8%BF%9B%E7%A8%8BDaemonSet%E5%8F%8A%E5%85%B6%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90.md)

[7.深入k8s：任务调用Job与CronJob及源码分析](%E6%B7%B1%E5%85%A5k8s/7.%E6%B7%B1%E5%85%A5k8s%EF%BC%9A%E4%BB%BB%E5%8A%A1%E8%B0%83%E7%94%A8Job%E4%B8%8ECronJob%E5%8F%8A%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90.md)

[8.深入k8s：资源控制Qos和eviction及其源码分析](%E6%B7%B1%E5%85%A5k8s/8.%E6%B7%B1%E5%85%A5k8s%EF%BC%9A%E8%B5%84%E6%BA%90%E6%8E%A7%E5%88%B6Qos%E5%92%8Ceviction%E5%8F%8A%E5%85%B6%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90.md)

[9.深入k8s：调度器及其源码分析](%E6%B7%B1%E5%85%A5k8s/9.%E6%B7%B1%E5%85%A5k8s%EF%BC%9A%E8%B0%83%E5%BA%A6%E5%99%A8%E5%8F%8A%E5%85%B6%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90.md)

[10.深入k8s：优先级及抢占机制源码分析](%E6%B7%B1%E5%85%A5k8s/10.深入k8s：优先级及抢占机制源码分析.md)

[11.深入k8s：kubelet工作原理及其初始化源码分析](%E6%B7%B1%E5%85%A5k8s/11.深入k8s：kubelet工作原理及其初始化源码分析.md)

[12.深入k8s：kubelet创建pod流程源码分析](%E6%B7%B1%E5%85%A5k8s/12.深入k8s：kubelet创建pod流程源码分析.md)

[13.深入k8s：Pod水平自动扩缩HPA及其源码分析](%E6%B7%B1%E5%85%A5k8s/13.深入k8s：Pod水平自动扩缩HPA及其源码分析.md)

[14.深入k8s：kube-proxy代理ipvs及其源码分析](%E6%B7%B1%E5%85%A5k8s/14.深入k8s：kube-proxy代理ipvs及其源码分析.md)

[15.深入k8s：Event事件处理及其源码分析](%E6%B7%B1%E5%85%A5k8s/15.深入k8s：Event事件处理及其源码分析.md)

[16.深入k8s：Informer使用及其源码分析](深入k8s/16.深入k8s：Informer使用及其源码分析.md)



