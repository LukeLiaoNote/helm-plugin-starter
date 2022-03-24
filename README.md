# helm-plugin-starter

用于管理[helm starters](https://helm.sh/docs/developing_charts/#chart-starter-packs)的helm3插件. 
Helm starters使用`helm create`命令来创建自定义默认chart.

helm starters示例:
* <https://github.com/LukeLiaoNote/helm-starter-demo.git>

## 安装

```sh
helm plugin install https://github.com/LukeLiaoNote/helm-starter.git
```

## 用法

* `helm starter fetch GITURL`: Clones a bare helm starter repo into `$HELM_HOME/starters`
* `helm starter list`: Lists all the starters in `$HELM_HOME/starters`
* `helm starter update NAME`: Refresh an installed Helm starter
* `helm starter delete NAME`: Delete `name` from `$HELM_HOME/starters`
* `helm starter inspect NAME`: Print out a starter's readme
* `helm starter --help`: print help

使用starter:

```sh
helm create NAME --starter STARTERNAME
```

## 示例

```sh
helm starter fetch https://github.com/LukeLiaoNote/helm-starter-demo.git
helm create demo --starter helm-starter-demo
```
