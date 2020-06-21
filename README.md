# 云计算实践课程 

## 实验六-云上的应用开发、部署和运维

### 来源

修改自https://github.com/tjrone/example



### Metrics逻辑

类似实验五，使用CPU利用率和MEM利用率作为指标。

对比例程，修改了metrics.go。



### 目录结构

````
├── Dockerfile                   制作镜像所使用
├── README
├── deploy                       部署资源对象时使用的配置文件
│   ├── deployment.yaml          云服务的Deployment配置文件
│   ├── metrics_service.yaml     
│   ├── prometheus.config.yml    prometheus抓取目标配置文件
│   ├── prometheus.deploy.yml    prometheus部署所使用Deployment
│   ├── prometheus.rbac.yml      prometheus权限配置文件
│   └── service.yaml
├── go.mod                       依赖管理
├── go.sum                       依赖管理
├── metrics                      Exporter
│   └── metrics.go
├── metrics_version              第6小节参考本目录
│   └── main.go
└── without_metrics              除5，6小节外参考本目录
    └── main.go
````

