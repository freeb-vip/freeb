# 说明
飞比智能官网网页代码

## 部署
```
#打包镜像
podman build -t registry.freeb.vip/freeb/freeb:dev -f Dockerfile .
#调试
podman run --rm -p 8080:80 -v `pwd`/resource:/usr/share/nginx/html registry.freeb.vip/freeb/freeb:dev
```

### Helm部署测试
```
helm template shopxo shopxo/ -n freeb > test.yaml
```

## 生产
```
podman build -t registry.freeb.vip/freeb/shopxo:latest -f Dockerfile .
```

### helm部署