# homebrew-ww3tool

Homebrew tap 仓库，提供 [WW3Tool](https://github.com/ZxyGch/WW3Tool) 的 formula。

## 使用（macOS / Linux 均可用）

```bash
brew tap ZxyGch/ww3tool
brew trust zxygch/ww3tool        # Homebrew 6+ 首次使用第三方 tap 需信任（一次性）
brew install ww3tool
```

或一步到位（自动 tap）：

```bash
brew install ZxyGch/ww3tool      # 首次仍需执行上面的 brew trust
```

安装后验证：`ww3tool --help`。

## 要求

- Homebrew（macOS 自带安装方式；Linux 可装 [Homebrew on Linux](https://docs.brew.sh/Homebrew-on-Linux)）
- Python 3.9+（formula 构建使用 Homebrew 的 `python@3.12`）
- 首次运行会自动创建虚拟环境并安装依赖，需几分钟，请保持网络畅通

## 升级 / 维护

formula 的 `url` 固定指向 WW3Tool 的**版本 tag**（当前 `v0.1.0`），日常 push 不影响。
发布新版本时：

```bash
# 1. 主仓库打新 tag 并推送
cd WW3Tool && git tag v0.1.1 && git push origin v0.1.1

# 2. 重算 sha256
curl -sL https://github.com/ZxyGch/WW3Tool/archive/refs/tags/v0.1.1.tar.gz | shasum -a 256

# 3. 更新本仓库 ww3tool.rb 的 url / sha256，推送（默认分支 main）
```
