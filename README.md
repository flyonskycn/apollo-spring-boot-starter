# apollo-spring-boot-starter

## 简介
> 在项目中快速引入apollo配置中心,  [apollo项目详细信息](https://github.com/ctripcorp/apollo)

## 项目依赖
apollo-spring-boot-starter依赖于[autoconfigure项目](https://github.com/flyonskycn/autoconfigure)

## 使用步骤
### 引入依赖
```xml
<dependency>
    <groupId>org.flyonsky.boot</groupId>
    <artifactId>apollo-spring-boot-starter</artifactId>
    <version>2.0.7.RELEASE</version>
</dependency>
```
### 基本配置
在bootstrap.yml文件下增加如下配置
1. app.id: apollo中分配的对应项目ID
2. apollo.meta: apollo meta地址
3. apollo.bootstrap.enabled: 设置为true
**为何如此设置参见[apollo项目](https://github.com/ctripcorp/apollo/wiki/Java%E5%AE%A2%E6%88%B7%E7%AB%AF%E4%BD%BF%E7%94%A8%E6%8C%87%E5%8D%97)**
4. apollo.bootstrap.namespaces: 设置配置的命名空间,多个多间之间用","分隔
5. apollo.cluster: 设置应用部署所在集群,默认为default

由于apollo对不同的环境需要配置不同的apollo meta地址,推荐两种方式:
1. 在resources新建apollo-env.properties,分别设置不同环境的apollo meta 地址.
```properties
dev.meta=http://1.1.1.1:8080
fat.meta=http://apollo.fat.xxx.com
uat.meta=http://apollo.uat.xxx.com
pro.meta=http://apollo.xxx.com
```
> 在启动参数中增加-Denv=YOUR-ENVIRONMENT
2. 直接在启动参数中增加-Dapollo.meta=http://config-service-url

### apollo-spring-boot-starter增加对了对archaius的支持

## 样例
[样例参见](https://github.com/flyonskycn/micro-service-study/tree/master/apollotimeserver)