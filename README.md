# datafoundry部署案例说明 
　　为了方便datafoundry用户理解平台的使用，我们收集了一些基于容器、后端服务来部署大数据分析服务的场景，具体如下：  
##  datafoundry使用基础
####  docker-2048  
　　由于PAAS的火热带动了一个游戏的普及，那就是2048，详见[在datafoundry平台上运行docker-2048](https://github.com/DataFoundry/docker-2048)
####  wordpress绑定mysql后端服务   
　　在2048出现前，在各个平台上部署的第一个应用通常是wordpress，好看又实用，这回我们通过后端服务给这个经典案例带来一些[新玩法](https://github.com/DataFoundry/wordpress)
####  通过tensorflow nodejs api完成神经网络模型训练   
　　2016年alphaGo成了mechine界和人间界的明星，我们也来膜拜一下[tensorflow playground](https://github.com/DataFoundry/tensorflow-playground)
  
##  大数据分析、应用场景  
####   Rstudio绑定mongodb后端服务  
　　在这个案例中我们通过datafoundry平台后端服务功能生成一个有共享数据的mongodb数据库后端服务，然后绑定到一个RstudioServer中，这样就可以通过Rstudio来对mongodb中的共享数据进行分析，详见[R数据分析场景](https://github.com/DataFoundry/R) 
####   Jupyter绑定mongodb后端服务  
　　在这个案例中我们通过datafoundry平台后端服务功能生成一个有共享数据的mongodb数据库后端服务，然后绑定到一个Jupyter notebook中，这样就可以通过Jupyter来对mongodb中的共享数据进行分析，详见[Jupyter数据分析场景](https://github.com/DataFoundry/jupyter)
####   Caravel绑定mysql服务，完成数据可视化  
> [Caravel](https://github.com/airbnb/caravel)是airbnb开源的一个数据可视化分析工具可以很方便的和mysql、postgresQL、Druid进行整合完成数据可视化分析。

  在这个案例中我们使用容器分别启动Caravel和mysql，并通过Caravel初始化mysql数据库中的数据，完成Caravel的demo应用,详见[Caravel集成MySQL数据库](https://github.com/DataFoundry/Caravel)  
  
####   运行openRefine进行数据探索  
> [openRefine](https://github.com/OpenRefine/OpenRefine) is a power tool that allows you to load data, understand it, clean it up, reconcile it, and augment it with data coming from the web. All with the comfort and privacy of your own computer.   

  　　在这个案例中我们使用容器启动openRefine，并通过openrefine下载从aws 送s3上下载[bank.csv](https://s3.cn-north-1.amazonaws.com.cn/bank.csv/bank.csv)中的数据然后进行数据探索相关任务   

#### zeppelin绑定spark后端服务   
 zeppelin是功能非常强大的数据分析和可视化工具，可以非常方便的与多种数据源，特别是spark，进行整合。本案例演示了如果通过datafoundry平台[部署zeppelin并集成spark后端服务](https://github.com/DataFoundry/zeppeline)  

##  大数据调度工具  
####   运行apache nifi ETL工具
>  [Apache NiFi](https://github.com/apache/nifi) is an easy to use, powerful, and reliable system to process and distribute data.

  通过容器运行一个[apache NiFi服务](https://github.com/DataFoundry/apache-nifi)，进行大数据服务调度和编排  
  NiFi资源列表：[https://github.com/jfrazee/awesome-nifi](https://github.com/jfrazee/awesome-nifi)
####   运行kettle ETL工具
>  Pentaho Data Integration ( ETL ) a.k.a [Kettle](https://github.com/pentaho/pentaho-kettle). With an intuitive, graphical, drag and drop design environment and a proven, scalable, standards-based architecture, Data Integration is increasingly the choice for organizations over traditional, proprietary ETL or data integration tools.   

  通过容器运行一个kettle应用后端服务服务，并绑定mysql和postgreSQL后端服务进行ETL，详见[通过kettle实现ETL服务](https://github.com/DataFoundry/kettle-service)  

## 机器学习
