# AlienFamilyHub Helm Repo

哎！是 helm repo。

## 添加仓库

要使用这个 Helm 仓库，请先添加仓库到你的 Helm 客户端：

```bash
helm repo add alienfamilyhub https://alienfamilyhub.github.io/charts
helm repo update
```

## 从仓库安装

### 查看可用的 Charts

```bash
helm search repo alienfamilyhub
```

### 安装

以 hello-world chart 为例：

```bash
# 安装到默认命名空间
helm install my-hello-world alienfamilyhub/hello-world

# 安装到指定命名空间
helm install my-hello-world alienfamilyhub/hello-world -n my-namespace --create-namespace

# 使用自定义 values
helm install my-hello-world alienfamilyhub/hello-world -f my-values.yaml

# 安装指定版本
helm install my-hello-world alienfamilyhub/hello-world --version 0.1.0
```

### 升级

```bash
helm upgrade my-hello-world alienfamilyhub/hello-world
```

### 卸载

```bash
helm uninstall my-hello-world
```

## 提交 Chart

在仓库根目录下创建你的 chart：

```bash
helm create my-new-chart
```