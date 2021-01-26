利用开源项目 Kubernetes 以及 TensorFlow 构建一个深度学习平台在深度学习平台上利用识别数字算法进行样本数据训练和测试。
需求一：构建Kubernetes集群，并且通过Kubernetes自带的dashboard-UI能够管理Kubernetes里面的资源。节点的数量可以根据参赛者实际条件选择。Kubernetes可以从社区获取，版本要求>= 1.6.7。Kubernetes集群搭建可以参考https://kubernetes.io/docs/setup/ 
需求二：将TensorFlow部署到Kubernetes集群里面。根据 https://www.tensorflow.org/serving/serving_inception 中的教程，将TensorFlow深度学习框架部署到搭建的Kubernetes平台里面， TensorFlow可以使用社区提供，版本要求>=0.8
需求三：通过TensorFlow深度学习平台上测试识别数字算法， 完成对于样本数据的训练以及测试功能。能够查看到训练的过程以及测试的结果。
需求四：深度学习计算对于平台的计算/存储/网络资源要求比较高，但平台负载比较高的时候会影响到算法的运行以及准确性， Kubernetes对于容器平台的监控当前主要是针对cpu以及内存，并且监控的指标很有限， 开源项目prometheus主要可以采集更多的监控指标， 在深度学习平台中利用prometheus来丰富监控指标，并且在将其整合到Kubernetes原生提供的kubernentes-dashboard里面。可以直观的在kubernetes-dashboard上查看。 需要增加的监控指标包括：节点的本地存储使用率，本地硬盘的读写速率，节点网卡流入流出速率。prometheus参考:https://prometheus.io prometheus实现对Kubernetes的监控参考： https://github.com/kayrus/prometheus-kubernetes
