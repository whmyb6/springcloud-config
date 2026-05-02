# springcloud-config

Spring Cloud Config 配置中心的远程配置文件仓库。

## 配置列表

| 文件 | 环境 |
|------|------|
| config-dev.yml | 开发环境 |
| config-test.yml | 测试环境 |
| config-prod.yml | 生产环境 |

## 使用方式

在 Spring Cloud Config Client 中配置：

```yaml
spring:
  application:
    name: config
  cloud:
    config:
      uri: http://config-server:3344
      label: main
```

客户端通过 `/{application}/{profile}/{label}` 拉取对应配置。
