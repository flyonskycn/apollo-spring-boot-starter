# apollo-spring-boot-starter

## 项目依赖
apollo-spring-boot-starter依赖于[autoconfigure项目](https://github.com/flyonskycn/autoconfigure)

## 使用步骤
### 引入依赖
```xml
<dependency>
    <groupId>org.flyonsky.boot</groupId>
    <artifactId>apollo-spring-boot-starter</artifactId>
</dependency>
```
### 基本配置
#### app.id: apollo中分配的对应项目ID
#### apollo.meta: apollo meta地址
#### apollo.bootstrap.enabled: 设置为true
为何如此设置参见[apollo项目](https://github.com/ctripcorp/apollo/wiki/Java%E5%AE%A2%E6%88%B7%E7%AB%AF%E4%BD%BF%E7%94%A8%E6%8C%87%E5%8D%97)
#### apollo.bootstrap.namespaces: 设置配置的命名空间，多个多间之间用","分隔
### apollo-spring-boot-starter增加对了对archaius的支持
