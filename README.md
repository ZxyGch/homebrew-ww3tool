# homebrew-ww3tool

Homebrew tap 仓库，提供 [WW3Tool](https://github.com/ZxyGch/WW3Tool) 的 formula。

## 使用

```bash
brew tap ZxyGch/ww3tool
brew install ww3tool
```

或一步到位（自动 tap）：

```bash
brew install ZxyGch/ww3tool
```

## 升级

formula 的 `url` 指向 WW3Tool 的 master tarball。更新 WW3Tool 代码后重新计算 sha256：

```bash
curl -sL https://github.com/ZxyGch/WW3Tool/archive/refs/heads/master.tar.gz | shasum -a 256
```

然后更新本仓库 `ww3tool.rb` 的 `sha256` 并推送。
