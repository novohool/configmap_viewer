# configmap_viewer

>通过k8s api 读取对应cm,减少开发改造难度

- 安装rust
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

- windows下需要安装openssl
```
choco install -y openssl
```

- git clone 这个项目代码

```
git clone http://gitlab.itiaoling.com/novolunt/configmap_viewer.git
cd configmap_viewer
```

- 编译
```
cargo build --release --bin cv
target/release/cv #二进制文件可单独拷贝传到容器内执行
```

- 运行
```
#容器内部测试
export NAMESPACE=myns
./cv configmap_api      // configmap_api是指定的cm名
```
